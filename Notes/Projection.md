
# Orthogonal matrix
## Def:
$Q$ is orthogonal if $Q^TQ=QQ^T=I$ 
### Prop.
If $Q$ is orthogonal: $<Q\vec{x},Q\vec{y}>=<\vec{x},\vec{y}>$

# Orthogonal complement
## Def:
Two subspace $W_1$,$W_2$ of $\mathbb{R}^n$ are said to be orthogonal if $<\vec{w_1},\vec{w_2}>=0$ for any $\vec{w_1}\in W_1,\vec{w_2}\in W_2$ .

$U\subseteq \mathbb{R}^n$ be a subspace. $U^\bot =\{\vec{w}\in\mathbb{R}^n\ |<\vec{v},\vec{w}>=0\}$ 
## Prop.
If $\vec{v_1},\cdots,\vec{v_k}$ are non-zero vector in $\mathbb{R}^n$ , s.t $<\vec{v_i},\vec{v_j}>=0$ for $i\neq j$ , they are linear independent.
    **Proof:** 
        Assuming $c_1\vec{v_1}+\cdots+c_n\vec{v_n}=0$ ,then $<\vec{v_i},c_1\vec{v_1}+\cdots+c_n\vec{v_n}>=c_i<\vec{v_i},\vec{v_i}>=0$ 
        so $c_i=0$ for any $c_i$ .
$V^\bot$ is a subspace.
    **Proof:**
        1. $<0,\vec{v}>=0$ 
        2. $<\vec{w_1}+\vec{w_2},\vec{v}>=<\vec{w_1},\vec{v}>+<\vec{w_2},\vec{v}>=0+0=0$ 
        3. $<c\vec{w_1},v>=c<\vec{w_1},\vec{v}>=0$ 
 $V^\bot \cap V=\{\vec{0}\}$.
    **Proof:** 
        For any $\vec{v}\in V\cap V^\bot$ ,$<\vec{v},\vec{v}>=0 \implies \vec{v}=\vec{0}$
 $V^\bot + V=\mathbb{R}^n$
    **Proof:**
        **Lemma:** Let $V\subseteq \mathbb{R}^n$ be a subspace with $\vec{v_1},\cdots,\vec{v_k}$ , then $w\in V^\bot \iff \vec{w} \bot \vec{v_i} \text{ for all } i=1,2,\cdots,k$ 
            $<\vec{w},\vec{v}>=<\vec{w},a_1\vec{v_1}+\cdots+a_k\vec{v_k}>$ , so $\vec{w}\in V^\bot$ .
        So we can write:$$A=\begin{bmatrix}\vec{v_1}^T\\ \vec{v_2}^T\\\vdots\\\vec{v_k}^T\end{bmatrix}$$ So, $V^\bot=N(A)$ , $C(A^T)=V$ , $V^\bot+V=N(A)+C(A^T)=\mathbb{R}^n$  
    So for any $\vec{v}\in \mathbb{R}^n$ ,$\vec{v}=\vec{v_1}+\vec{v_2}$ , the composition is unique.
$(V^\bot)^\bot=V$
    **Proof:** 
        $V^\bot+V=\mathbb{R}^n$, $V^\bot+(V^\bot)^\bot=\mathbb{R}^n$.
        So $dim\ V=dim\ (V^\bot)^\bot$ .
        By def $V\subseteq (V^\bot)^\bot \implies V=(V^\bot)^\bot$ .
# Projection
## Def:
For $\vec{v}\in V^n$ ,$\vec{v}=\vec{v_1}+\vec{v_2},\vec{v_1}\in U,\vec{v_2}\in U^\bot$ ,$P(\vec{v})=\vec{v_1}$ is a projection to $U$.
We can see that:
1. P is a linear transformation.
2. $P^2=P$
3. $\tilde{P}(\vec{v})=\vec{v}-P(\vec{v})$ is a projection to $V^\bot$ 
## How to find the projection matrix
### Method 1
Say: We want to project onto a hyperplane $V$ , choose a new basis $\{\vec{v_1},\cdots,\vec{v_k}\} \in V \{\vec{v_{k+1}},\cdots,\vec{v_n}\}\in V^\bot$ 
Say $k=2,n=4$ :$$P=\begin{bmatrix}1&0&0&0\\0&1&0&0\\0&0&0&0\\0&0&0&0\end{bmatrix}$$
$$\begin{split}\text{The transformation we need is:}\\ \ _{e_i}[id]_{v_i}\ _{v_i}[P]_{v_i}\ _{v_i}[id]_{e_i}=A\\_{e_i}[id]_{v_i}=[\vec{v_1}\ \vec{v_2}\ \vec{v_3}\ \vec{v_4}]\end{split}$$

So $A=VPV^{-1}$ $(V=[\vec{v_1}\ \vec{v_2}\ \vec{v_3}\ \vec{v_4}])$ 
### Method 2 
**Def:** $\vec{q_1},\cdots,\vec{q_n}$ are orthonormal if $<\vec{q_i},\vec{q_j}>=0$ if $i\neq j$ , $<\vec{q_i},\vec{q_j}>=1$ if $i=j$ .
Say give $V$ and a orthonormal basis $\vec{q_1},\cdots,\vec{q_n}$ , so $P=q_1q_1^T+\cdots+q_nq_n^T$ 
How to find orthonormal basis?
*Gram-Schmidt Method* :
Take $v_1\in V$ , $q_1=\frac{v_1}{||v||}$  , $v_2=\tilde{v_2}+v_2^\prime$ , $v_2^\prime=v_2-<v_2,q_1>q_1 \implies q_2=\frac{v_2^\prime}{||v_2^\prime||}$ 
$v_3^\prime=v_3-<v_3,q_1>q_1-<v_3,q_2>q_2 \implies q_3=\frac{v_3^\prime}{||v_3^\prime||}\cdots$  
### Method 3
Given: $\vec{v_1},\cdots,\vec{v_n}$ a basis of $V$.
Write $A=[\ v_1,\ v_2, \ \cdots,\ v_n]$ 
Claim: $M=A(A^TA)^{-1}A^T$ is the projection matrix.
Write: $v=v_1+v_2\ (v_1\in C(A), v_2\in N(A^T))$ 
So, $M(v)=M(v_1)+M(v_2)$, $M(v_2)=A(A^TA)^{-1}A^Tv_2=0$ 
$M(v_1)=M(Ax)=A(A^TA)^{-1}A^TAx=Ax=v_1$ , so $M$ is a projection matrix.

# Transpose again
If $<Ax,y>=<x,By>$ , B is the adjoint operator of $A$.
On $\mathbb{R}^n$ , $B=A^T$ is  the only matrix satisfy this equation.
$$\begin{split}&<Ax,y>-<x,By>=x^TA^Ty-x^TBy=x^T(A^T-B)y=0\\&\implies C=A^T-B\\&\text{Let x=Cy:}\\\\&(Cy)^TCy=0\implies Cy=0 \quad \text{for all y} \implies C=0\end{split}$$
That is why $(AB)^T=B^TA^T$ .
