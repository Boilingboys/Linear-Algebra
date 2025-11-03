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

# 3
**If $\mathbf{nullC=nullA\cap nullB}$, prove that $\mathbf{rkA+rkB\geq rkC\geq max\{rkA,rkB\}}$.**
**Proof:** 
First prove $rkC\geq max\{rkA,rkB\}$:$$\begin{split}&dim\ nullC\leq dim\ nullA\\&dim\ nullC\leq dim\ nullB\\\implies &rkC\geq max\{rkA,rkB\}\end{split}$$**Lemma 1:**
If $S_1,S_2$ are 2 finite-dimension subspaces:$$dim(S_1+S_2)=dimS_1+dimS_2-din(S_1\cap S_2)$$
Proof: Take $s_1,s_2,\cdots ,s_k$ as a basis in $S_1\cap S_2$ , extend $u_1,u_2,\cdots ,u_m$ to a basis of $S_1$, extend $v_1,v_2,\cdots ,v_n$ to a basis of $S_2$.
$dim(S_1+S_2)=m+n+k=(m+k)+(n+k)-k=dimS_1+dimS_2-din(S_1\cap S_2)$ 
**Lemma2:**
Def Orthogonal complement: $W^{\bot}=\{v\ |\ v\in V w\in W, <v,w>=0\}$ 
Finite dimension subspace exist one unique orthogonal complement.$\iff V=U\oplus U^{\bot}$  
proof:
$\iff$ 1. for any $\alpha \in V$ , $\alpha =\alpha_1 \oplus \alpha_2$ , $\alpha_1 \in U ,\alpha 2 \in U^{\bot}$ 
      2. $U\cap U^{\bot}=\{0\}$ 
1: Take $\eta_1,\eta_2,\cdots,\eta_n$ as standard orthonormal basis of $V$, for subspaces we can find $\eta_{i_1},\eta_{i_2},\cdots,\eta_{i_k}$ as standard orthonormal basis of $U$, so rest of them are the basis of $U^{\bot}$ ,
$\alpha=\underbrace{c_1\eta_{i_1}+\cdots+c_k\eta_{i_k}}_{\alpha_1}+\underbrace{d_1\eta_{j_1}+\cdots+\eta_{j_{n-k}}}_{\alpha_2}$  $\alpha_1\in U,<\alpha_1,\alpha_2>=0$, so $\alpha_2 \in U^{\bot}$ .
2： If $v\in U\cap U^{\bot}$ ,$<v,v>=0$, so $v=0$ .

If $Cx=0$, then $Ax=0,Bx=0$. So $null\ C$ is orthogonal to $range\ A^T+range\ B^T$.
$range\ C^T= (null \ C)^{\bot}= range\ A^T+range\ B^T$ 
So:$dim\ range\ C^T =dim\ range\ (range\ A^T+range\ B^T)=dim\ range\ A^T+dim\ range\ B^T -dim\ (range\ A^T\cap range\ B^T)$ $\iff$ $rkC\leq rkA+rkB$ 
# 4
Let $AB=BA$ in #3, prove that $rkA+rkB\geq rkC+rkAB$ .
**Proof:** 
If $AB=BA$, then $\overbrace{AB\vec{x}}^{\in C(A)}=\overbrace{BA\vec{x}}^{\in C(B)}$ , so $C(AB)=C(BA)=C(A)\cap C(B)$ . Also $AB=BA \implies B^TA^T=A^TB^T$ , so $C(A^TB^T)=C(A^T)\cap C(B^T)$. Take orthogonal complement:
$(C(A^TB^T))^\bot = N(A)+N(B)=N(BA)=N(AB)$ . So from #1, $N(A)\subseteq C(B)$ ,$rkA+rkB=rkAB+n$ .
Obviously, $n\geq rkC$ .

