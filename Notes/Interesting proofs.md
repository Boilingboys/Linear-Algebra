# 1
**If $\mathbf{W_1,W_2\in V}$ are subspaces of $\mathbf{V}$, then $\mathbf{W_1\cap W_2}$ is also a subspace.** 
**Proof:** 
    For any $\vec{w_1},\vec{w_2}\cdots\vec{w_n}\in W_1\cap W_2$ , the linear combination of them are both in $W_1$ and in $W_2$ . So they are in $W_1\cap W_2$ .
    Obvious, $\vec{0}$ is in $W_1\cap W_2$ .
    So $W_1\cap W_2$ is a subspace.

# 2
$\mathbf{rankA+rank{B}-n\leq rankAB}$ **for p\*n matrix $\mathbf{A}$ and n\*q matrix $\mathbf{B}$ .
Proof:** 
    $rkA=dimC(A)=n-dimN(A)$ ,so $rank(A)+rank{B}-n=rkB-dimN(A)$ .
    $rkAB=dimC(AB)=q-dimN(AB)$ , and for $\vec{x}\in N(AB)$ :$$\begin{split}&1.\vec{x}\in N(B)\\&2.B\vec{x}\in N(A)\implies\vec{v}\in C(B)\cap N(A)\end{split}$$
    So $dimN(AB)\leq dimN(A)+dimN(B)$ .
    $$\begin{split}&rkAB\\&=q-dimN(AB)\geq q-dimN(B)-dimN(A)\\&=dimC(B)-dimN(A)=dimC(B)+dimC(A)-n\\&=rkA+rkB-n\end{split}$$ 
    When and only when $C(B)\cap N(A)=N(A)\implies N(A)\subseteq C(B)$ the symbol is equal. 