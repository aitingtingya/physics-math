(* 
```mathematica
写了个小包简化mathematica里的张量计算，后面附了一些用例
几个重要的函数
defTensor[name_, rank_Integer, dim_Integer, vars_List]
定义一个dim维流形上的名字为name，阶数为rank，依赖坐标vars的抽象张量，张量对 vars 的依赖不是抽线而是显式的，可以不用该函数
所有参数都要填，如果是常张量，则 vars={}
tensor[expr_,index_List]
计算表达式expr，返回的结果中指标的顺序为index
tensorPrint[args__,coords_List]
在终端简化张量定义函数定义的张量的打印结果，如果不是抽象张量可以不用该函数，args可以按照Print来用，但是要把采用的坐标coords填入
*)
(* 
开始实现抽象张量定义函数
*)
  defTensor[name_, rank_Integer, dim_Integer, vars_List] := 
  Array[
    Symbol[StringJoin[ToString[name],ToString /@ {##}]][Sequence @@ vars] &,ConstantArray[dim, rank]
  ];
(* 
结束抽象张量定义函数
*)

(* 
开始实现核心的张量计算函数
*)
tensorTime[expr_, tabIndex_List] := Module[
  {tensorParts, dimIndex, sumIndex, getDimForIndex, sumDim, tabDim},
  tensorParts = Cases[
    expr,
    TPart[t_, indices__] :> {t, {indices}},
    {0, Infinity}
  ];
  dimIndex = Map[{Dimensions[#[[1]]], #[[2]]} &, tensorParts];
  sumIndex = Cases[Tally[Flatten[dimIndex[[All, 2]]]], {idx_, 2} :> idx];
  getDimForIndex[idx_] := Module[{match, pos},
    match = SelectFirst[dimIndex, MemberQ[#[[2]], idx] &];
    pos = First[First[Position[match[[2]], idx]]];
    match[[1]][[pos]]
  ];
  sumDim = Map[{#, 1, getDimForIndex[#]} &, sumIndex];
  tabDim = Map[{#, 1, getDimForIndex[#]} &, tabIndex];
  If[tabDim === {},
    If[sumDim === {},
       expr /. {TPart -> Part, tempD -> D},
       Sum[expr /. {TPart -> Part, tempD -> D}, Evaluate[Sequence @@ sumDim]]
    ],
    If[sumDim === {},
       Table[expr /. {TPart -> Part, tempD -> D}, Evaluate[Sequence @@ tabDim]],
       Table[Sum[expr /. {TPart -> Part, tempD -> D}, Evaluate[Sequence @@ sumDim]], Evaluate[Sequence @@ tabDim]]
    ]
  ]
];
SetAttributes[tensor, HoldAll]; 
tensor[expr_, tabIndex_List] := Block[{expandedExpr},
  expandedExpr = Expand[Unevaluated[expr] /. {Part -> TPart, D -> tempD}];
  If[Head[expandedExpr] === Plus,tensorTime[#, tabIndex] & /@ expandedExpr,
    tensorTime[expandedExpr, tabIndex]
  ]
]; 
(* 
结束张量计算函数
*)
(* 
开始实现张量打印函数
*)
tensorPrint[args__,coords_List] := Block[{str},
formatExpr[expr_] := Block[{safeExpr,tempD},
  If[StringQ[expr], Return[expr]];
  safeExpr = expr /. Derivative[orders__][f__][vars__] :> Block[
     {},
     tempD[f,Sequence@@Flatten[MapThread[ConstantArray, {{vars},{orders}}]]]
  ];
  safeExpr = safeExpr /. f_Symbol[vars__] :>f/;SubsetQ[coords, {vars}];
  (* 如果要用花括号括起被求导的坐标，则用safeExpr = safeExpr /.tempD[f__,args__]:>tempD[f,{args}]; *)
  StringReplace[ToString[safeExpr, InputForm],"tempD" ->"D"]
];
  Apply[Print,formatExpr[#] & /@ {args}];
];
(* 
结束张量打印函数
*)
(* --------------------------------------------------------- *)
(* 3. 全面测试 *)
(* --------------------------------------------------------- *)
coords={t,x,y,z};
X = {{X11, X12}, {X21, X22}}; 
Y = {{Y11, Y12}, {Y21, Y22}};
Z = {{Z11, Z12}, {Z21, Z22}}; 
M = {{M11, M12}, {M21, M22}};
f[x_] := x^2;
result = tensor[
  s*X[[i,j]]Y[[j,k]] + Z[[i, k]] + f[s] M[[j, i]] Z[[j, l]] X[[l, k]], 
  {i, k}
];
Print["result=",result];
T=defTensor[T,2,4,{t,x}]
Print["T=",T];
tensorPrint["T=",T,coords];

 result=tensor[f[s]^2X[[i,j]]+X[[i,k]]Z[[k,j]]/(tensor[Y[[m,n]]M[[n,m]],{}]),{i,j}]
Print["result=",result];

X = {{X11, X12}, {X21, X22}}; 
Y = {{Y11, Y12}, {Y21, Y22}};
v = {v1, v2};
u = {u1, u2};
s = Symbol["s"]; 

Print["C_ik = X_ij Y_jk"];
res1 = tensor[X[[i, j]] Y[[j, k]], {i, k}];
Print[res1 // MatrixForm];

Print["tr = X_ii"];

res2 = tensor[X[[i, i]], {}]; 
Print["Result: ", res2];

Print["dot = u_i v_i"];
res3 = tensor[u[[i]] v[[i]], {}];
Print["Result: ", res3];

Print["val = s + X_ii"];
res4 = tensor[s + X[[i, i]], {}];
Print["Result: ", res4];

Print["R_ik = s * X_ik + (u_j v_j) * Y_ik"];
res5 = tensor[s * X[[i, k]] + u[[j]] v[[j]] Y[[i, k]], {i, k}];
Print[res5 // MatrixForm];
coords = {t, x}; 
dim = {2, 2};
g = {{- (1 + x), 0}, {0, t^2}};
gInv = Inverse[g]; 
A = {Sin[t], Cos[x]};

Print[" g_uv = ", g ];
Print[" g^uv = ", gInv ];
K = tensor[A[[i]] A[[j]] g[[i, j]], {}]; 
Print["K = ", K];
dKdt = D[K, t];
Print["dK/dt = ", dKdt];
Print[" ", Simplify[dKdt == D[-(1 + x) Sin[t]^2 + t^2 Cos[x]^2, t]]];
Christoffel = tensor[
  1/2 * gInv[[l, s]] * (
      D[g[[n, s]], coords[[m]]] 
    + D[g[[m, s]], coords[[n]]] 
    - D[g[[m, n]], coords[[s]]]
  ),
  {l, m, n} 
];
Print["Christoffel=",Christoffel];
ChristoffelTable = Table[
  Sum[
    1/2 * gInv[[l, s]] * (
        D[g[[n, s]], coords[[m]]]
      + D[g[[m, s]], coords[[n]]]
      - D[g[[m, n]], coords[[s]]]
    ),
    {s, 2}
  ],
  {l, 2}, {m, 2}, {n, 2}
];
Print["ChristoffelTable =",ChristoffelTable];
Print["Diff=",Christoffel == ChristoffelTable];

Clear[S];
Clear[T];
T = defTensor["T", 3, 2, coords];
S = defTensor[S, 2, 2, coords];

Print["T  = ",T];
Print["S  = ",S]; 

ResultAbstract = tensor[
  T[[m, n, s]] * S[[m, n]], 
  {s} 
];

Print["ResultAbstract=",ResultAbstract];

DerivResult = tensor[
  D[T[[m, n, s]] * S[[m, n]], coords[[2]]], 
  {s}
];

Print["DerivResult=",DerivResult];

DivS = tensor[
   gInv[[l, m]] * D[S[[m, n]], coords[[l]]],
   {n}
];
Print["DivS =",DivS]; 



