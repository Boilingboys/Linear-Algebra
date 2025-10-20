# Vector space
## Def:
A vector space is a set of $V$ (elements of $V$ are called vectors), equipped with 2 operation:
    $$\begin{split}&\text{1. scalar multiplication}\cdot\text{ :}\mathbb{R}\times V\longrightarrow V \\ &\text{2. addition}+:V\times V\longrightarrow V \end{split}$$
    They satisfy 8 capability conditions.
        $$\begin{split} &\text {1. }a+b=b+a \\&\text{2. }a+(b+c)=(a+b)+c\\&\text{3. There exist 0 that a+0=0}\\&\text{4. There exist -a that a+(-a)=0 }\\&\text{5. for }c_{1},c_{2}\in\mathbb{R}, (c_1+c_2)a=c_1a+c_2a \\&\text{6. for }c_1,c_2\in\mathbb{R},c_1(c_2a)=c_1c_2a\\&\text{7. There exist 1}\in V,1\cdot a=a\\&\text{8. for c}\in\mathbb{R }\text{ },c(a+b)=ca+cb\end{split}$$
        [[Lecture 5.pdf#page=26&rect=30,24,828,535|Lecture 5, p.26]]
## Prop:
**1. 0 is unique.**
    **proof:**
        Suppose there are two 0, $0_1 ,0_2$ .
        $0_1+0_2=0_2=0_2+0_1=0_1$, so $0_2=0_1$ .
         
**2. For any $\mathbf{\vec{v} \in V}$, $-\vec{v}$ is unique.**
    **proof:** suppose there are $-\vec{v_1},-\vec{v_2}\in V,v+(-\vec{v_1})=v+(-\vec{v_2})=0$
        $-\vec{v_1}+(v+-\vec{v_2})=-\vec{v_1}=(-\vec{v_1}+v)+-\vec{v_2}=-\vec{v_2}$ 
**3. $\mathbf{0\cdot \vec{v}=\vec{0}}$ for any $\vec{v}$**
        **proof:**
        $$\begin{split}&0\vec{v}+0\vec{v}=(0+0)\vec{v}=0\vec{v}\\ &\Rightarrow0\vec{v}+0\vec{v}+(-0\vec{v})=\vec{0}\\&\Rightarrow0\vec{v}=\vec{0}\end{split}$$ **4. For any $\mathbf{\vec{v} \in V, (-1\vec{v})=-\vec{v}}$.**
        **proof:**
        $\vec{v}+(-1)\vec{v}=(-1+1)\vec{v}=0\vec{v}=\vec{0}$ 
## Example:

Take $V=\mathbb{R_+}$ , we can construct:
$$\begin{split}&\circ:\mathbb{R\times R_+}\longrightarrow\mathbb{R_+}\\&+:\mathbb{R_+\times R_+\longrightarrow R_+}\\&\text{We can define:}c\circ x=x^c,x+y=xy.\end{split}$$
We can check that it satisfied the 8 rules. So $\mathbb{R_+}$ is a vector space under these operations. The dimension of $\mathbb{R,R_+}$ are both 1 dimensional, and we can construct a map from $\mathbb{R\text{ to }R_+}$ :$$\begin{split}&\mathbb{R\longrightarrow R_+}\\&v\longrightarrow e^v\\&log(w)\leftarrow w\end{split}$$ We can say $\mathbb{R\text{ and }R_+}$ are isomorphic(同构).
    
       

# Null space and column space

## Def:
### Subspace:
We say W, a subset of V is a subspace of V if:$$\begin{split}&1)c\vec{x}\in W,\text{ if }\vec{x}\in W\\&2)\vec{x}+\vec{y}\in W,\text{if }\vec{x},\vec{y}\in W\end{split}$$ 
### Null space:

The null space of m\*n matrix A is given by the following definition:$$N(A)=\{\vec{x}\text{ }|\text{ }\vec{x}\in\mathbb{R}^n\text{ }A\vec{x}=\vec{0}\}$$

### Column space:
The column space of m\*n matrix A is:$$\begin{split}&\text{Let }\vec{a_i}\text{be the ith column of A}\\&C(A)=\{\vec{v}\text{ | }c_i\in\mathbb{R},\vec{v}=c_1\vec{a_1}+c_2\vec{a_2}+\dots+c_na_n\}\end{split}$$

## Prop:
**If W is the subspace of V, $\mathbf{\vec{0_v}}$ is the zero vector of V, then $\mathbf{\vec{0_v}=\vec{0_w}}$ .** 
    **proof:**
        Take $\vec{v}\in W$, then$0\cdot\vec{v}=\vec{0_v}=\vec{0_w}$ (because $\vec{v}$ is both in V and W)
# Solving $A\vec{x}=\vec{b}$ 
## Def:
### Span:
 We say $V$ is the span of $\vec{v_1},\vec{v_2},\vec{v_3},\dots,\vec{v_n}$ , for $c_1,c_2,c_3,\dots,c_n\in \mathbb{R}$ , if any $\vec{v}\in V, \vec{v}=c_1\vec{v_1}+c_2\vec{v_2}+c_3\vec{v_3}+\dots+c_n\vec{v_n}$ .
 Noted as: $V=\text{Span}\{\vec{v_1},\vec{v_2},\vec{v_3},\dots,\vec{v_n}\}$ 

## Process of finding the solution of $A\vec{x}=\vec{b}$ 
1. Do the elimination.
    We can show that  for $A=LDE\tilde{U}=LDEE^{'}R$ ,$N(A)=N(U)=N(\tilde{U})=N(R)$ :
        **proof:** 
        $A\vec{x}=\vec{0} \Rightarrow LDU\vec{x}=\vec{0}$  
        So $N(A)=N(U)$ . 
   Solving $R\vec{x}=\vec{0}$ ,find $N(A)$
2. Describe $N(A)$ using the span, write as $\vec{x_n}\in N(A)$ .
    In $R\vec{x}=\vec{0}$ , set the first free variable as 1, and the left are all 0's,solve the equation, write as $\vec{x_1}$ . Then we do the same for the remaining free variable, to find $x_2,\dots,x_k$ . Then: $N(A)=Span\{\vec{x_1},\vec{x_2},\dots,\vec{x_k}\}$ 
    **note:** [[An interesting insight from the method of finding the null space of A]]
3. Set all the free variable as 0, solve $\vec{x_p}$ .
4. The solution of $A\vec{x}=\vec{b}$ is $\vec{x}=\vec{x_p}+\vec{x_n}$ 
    [[Lecture 7.pdf#page=52&rect=46,90,805,326|Lecture 7, p.52]]

# Rank 
## Def:
The rank of A is the number of pivots in its row echelon form, it is written as rank(A).
## Prop.
$\mathbf{rank(A)\leq min\{m,n\}}$ **for m\*n matrix A.** 

**For n\*n matrix A:  $\begin{split}\text{A is non-singular}\Longleftrightarrow \text{A is invertible}\Longleftrightarrow rk(A)=n\end{split}$ 

$\mathbf{rank(AB)\leq min\{rk(A),rk(B)\}}$ 

# Linear independence

## Def: 
Vectors $\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$  are said to be linear independent, if $c_1\vec{v_1}+c_2\vec{v_2}+\cdots+c_n\vec{v_n}=\vec{0}$ only when $c_1=c_2=\cdots=c_n=0$ .
[[Lecture 7.pdf#page=83&rect=34,290,807,530|Lecture 7, p.83]]
**note:** The meaning of linear independence [[Lecture 7.pdf#page=98&rect=58,320,818,537|Lecture 7, p.98]]
## Prop:
$\vec{a_1},\vec{a_2},\cdots,\vec{a_n}$ are column vectors of $A$  in $\mathbb{R}^n$ , then$$\vec{a_1},\vec{a_2},\cdots ,\vec{a_n}\text{ are linear dep.}\Longleftrightarrow A\vec{x}=\vec{0}\text{ has non-zero solution. }$$
    **Proof:** if they are dep. , then $c_1\vec{v_1}+c_2\vec{v_2}+\cdots+c_n\vec{v_n}=\vec{0}$ has non-zero solution, which means $$A\begin{pmatrix}c_1\\c_2\\\vdots\\c_n\end{pmatrix}=\vec{0}$$ has non-zero solution.
    
$\vec{a_1},\vec{a_2},\cdots ,\vec{a_n}\text{are l.i.}\Longleftrightarrow Q\vec{a_1},Q\vec{a_2},\cdots ,Q\vec{a_n}\text{ are l.i}$ , if $Q$ is a invertible matrix. 
    **Proof:** invertible matrix $Q$ can be express as multiplication of Elementary matrices, it doesn't change the number of pivots, so they are linear independent.[[Lecture 7.pdf#page=124&rect=30,5,827,129|Lecture 7, p.124]] 
    
Orthogonal vectors are linear independent.
    **Proof：** $$c_1\vec{v_1}+c_2\vec{v_2}+\cdots+c_n\vec{v_n}=\vec{0}\Longrightarrow \vec{v_j}^T(c_1\vec{v_1}+c_2\vec{v_2}+\cdots+c_n\vec{v_n})=c_j\vec{v_j}^T \vec{v_j}=0\Longrightarrow c_j=0$$ 
Any vector $\vec{v}$ in $span\{\vec{v_1},\vec{v_2},\cdots,\vec{v_n}\}$ can be express uniquely by linear combination of $\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$ if they are l.i.
**Proof:** let:$$\begin{split}&c_1\vec{v_1}+c_2\vec{v_2}+\cdots+c_n\vec{v_n}=\vec{v}=d_1\vec{v_1}+d_2\vec{v_2}+\cdots+d_n\vec{v_n}\\&\Rightarrow (c_1-d_1)\vec{v_1}+(c_2-d_2)\vec{v_2}+\cdots+(c_n-d_n)\vec{v_n}=\vec{0}\end{split}$$ So $c_1=d_1,c_2=d_2,\cdots,c_n=d_n$ , they are unique.
# Basis
## Def
$\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$ is called a basis of $V$ if:
1.$\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$ are linear independent.
2.$span\{\vec{v_1},\vec{v_2},\cdots,\vec{v_n}\}=V$ 
[[Lecture 8.pdf#page=30&rect=67,307,804,532|Lecture 8, p.30]]
## Prop.
$\mathbf{\vec{v_1},\vec{v_2},\cdots,\vec{v_n} \textbf{ basis for }V\Longleftrightarrow E\vec{v_1},E\vec{v_2},\cdots,E\vec{v_n} \textbf{ basis for }E(W) \textbf{ for invertible matrix E}}$ 
**Proof:** 
Let say a 7 columns matrix $A$ with 4 pivots in $U$ . 
$$\begin{split}&\text{pivot columns of U: }[\vec{u_1},\vec{u_2},\vec{u_4},\vec{u_6}]\\&\text{columns of A : }[\vec{a_1},\vec{a_2},\vec{a_3},\vec{a_4},\vec{a_5},\vec{a_6},\vec{a_7}]\end{split}$$
Take $\vec{v}\in C(A), E\vec{v} \in C(U)$ :
$E\vec{v}=c_1\vec{u_1}+c_2\vec{u_2}+c_4\vec{u_4}+c_6\vec{u_6}$ , so $\vec{v}=c_1E^{-1}\vec{u_1}+c_2E^{-1}\vec{u_2}+c_4E^{-1}\vec{u_4}+c_6E^{-1}\vec{u_6}=c_1\vec{a_1}+c_2\vec{a_2}+c_4\vec{a_4}+c_6\vec{a_6}$ ,so $\vec{a_1},\vec{a_2},\vec{a_3},\vec{a_4}$ is also a basis of $C(A)$ .
Note: $E(W)=\{E\vec{v}\text{ | }\vec{v}\in W\}$ , it is true for invertible matrix E.

**If $V$ is finite dimensional, then $V$ has a basis.**
**Proof:** 
finite dimensional
*Def:* $V$ is finite dimensional if there exist finite number of vectors $\vec{v_1},\vec{v_2},\vec{v_3},\cdots,\vec{v_n}$ s.t $V=span\{\vec{v_1},\vec{v_2},\cdots\vec{v_n}\}$ .
We take $span\{\vec{v_1},\vec{v_2},\cdots,\vec{v_k}\}=V$ , take one non-zero element $\vec{v_1}$ , let $S_1=span\{\vec{v_1}\}$ .
1. If $S_1=V$ , return 0;
2. If $S_1\neq V$, take another $\vec{v_i}\neq 0 ,\vec{v_i} \notin S_1$ ,let it be $\vec{v_2}$ , $S_2=span\{\vec{v_1},\vec{v_2}\}$ .
We will arrive a situation that $S_l=V$ with $l\leq k$ .
**note:** this shows any spanning set of $V$ can be reduced to a basis of $V$ .

**Suppose $V$ is finite dimensional then any set of l.i. vectors $\mathbf{\vec{v_1},\vec{v_2},\cdots,\vec{v_k}}$ can be extended to a basis $\mathbf{V}$ .** 
**Proof:** 
Let $\vec{w_1},\vec{w_2},\cdots,\vec{w_n}$ be a spanning set of $V$, then we take $S=span\{\vec{v_1},\vec{v_2},\cdots,\vec{v_k}\}$ 
1. If $S=V$, return 0;
2. If $S\neq V$ , take $\vec{w_i} \notin S$  ,let it be $\vec{v_{k+1}}$ ,,$S=span\{\vec{v_1},\vec{v_2},\cdots,\vec{v_k},\vec{v_{k+1}}\}$ , back to 1.

# Dimension
## Def

If $V$ is a vector space with basis $\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$ , then the dimension of $V$ is n, noted as $dimV$ .

## Prop.

**Dimension is well-defined.**
**Proof:**
Let $\vec{v_1},\vec{v_2},\cdots,\vec{v_n}$ be a basis of $V$, $\vec{w_1},\vec{w_2},\cdots,\vec{w_m}$ be another basis, suppose $m>n$ .
Let $n=2,m=3$:
$$\begin{split}&\vec{w_1}=a_{11}\vec{v_1}+\vec{a_{21}}\vec{v_2}\\&\vec{w_2}=a_{12}\vec{v_1}+\vec{a_{22}}\vec{v_2}\\&\vec{w_3}=a_{12}\vec{v_1}+a_{23}\vec{v_2}\end{split}$$
Write a matrixish operation:$$[\vec{w_1},\vec{w_2},\vec{w_3}]=[\vec{v_1},\vec{v_2}]\begin{bmatrix}a_{11} & a_{12} & a_{13} \\ a_{21}&a_{22}&a_{23} \end{bmatrix}$$ So we can find:
$$\begin{bmatrix}c_1\\c_2\\c_3\end{bmatrix}\text{ with } c_1,c_2,c_3 \text{ not all 0's},\text{ s.t }A\begin{bmatrix}c_1\\c_2\\c_3\end{bmatrix}=\begin{bmatrix}0\\0\end{bmatrix}$$

$$[\vec{w_1},\vec{w_2},\vec{w_3}]\begin{bmatrix}c_1\\c_2\\c_3\end{bmatrix}=[\vec{v_1},\vec{v_2}]A\begin{bmatrix}c_1\\c_2\\c_3\end{bmatrix}=0$$ 
So $c_1\vec{w_1}+c_2\vec{w_2}+c_3\vec{w_3}=\vec{0}$ has non-zero solution, so they are linear dependent, thus not a basis of $V$ .
**note:** If a is a m\*n matrix, then a $\mathbb{R}^n$ vector $\vec{v}$ multiply $A$ is a map from $\mathbb{R}^n$ to $\mathbb{R}^m$ .

**$\mathbf{dimC(A)+dim(N(A))=n}$ for m\*n matrix  .** 
**Proof:** 
From the def of rank, ${rk{A}=dimC(A)}$ , and the dimension of ${N(A)}$ is the number of free variables(see in [[An interesting insight from the method of finding the null space of A#Proof]], we prove that $N(A)$ is construct by a basis of free variables). So ${dimC(A)+dim(N(A))=n}$ for m\*n matrix $A$ .

**If $\mathbf{W}$ is a subset of finite dimensional $\mathbf{V}$ ,then $\mathbf{dimW\leq dimV}$ .**
**Proof:** 
Take a basis of $W$ ,we can extended them to the basis of $V$.
[[LAw5.pdf#page=10&rect=72,480,536,551|LAw5, p.10]]

$\mathbf{rank(AB)\leq min\{rank(A),rank(B)\}}$ 
**Proof:** 
*Lemma1:* $C(AB)\subseteq C(A)$ 
    Let A be 3\*2, B be 2\*2:$A=[\vec{a_1},\vec{a_2},\vec{a_3}],B=[\vec{b_1},\vec{b_2}]$ 
    $$AB=\begin{bmatrix}b_{11}\vec{a_1}+b_{21}\vec{a_2}&b_{12}\vec{a_1}+b_{22}\vec{a_2}\end{bmatrix}$$        So every column of $AB$ is a linear combination of columns in $A$.
    
*Lemma2:* If $B$ is invertible, then $C(AB)=C(A)$ 
    $A=ABB^{-1}$ so, $C(A)\subseteq C(AB)$ .
    $C(A)\subseteq C(AB),C(AB)\subseteq C(A)\Longrightarrow C(A)=C(AB)$ 
    
*Lemma3:*$rk(A^TA)=rk(A)$
    For $\vec{x}\in N(A), A^TA\vec{x}=A^T\vec{0}=\vec(0)$ 
    For $\vec{x}\in N(A^TA)$ , $\vec{x}^TA^TA\vec{x}=\vec{0}\Longrightarrow (A\vec{x})^T(A\vec{x})=0$ So $<A\vec{x},A\vec{x}>=0$ , so $A\vec{x}=0$
    So $N(A)=N(A^TA)$ ,$rk(A^TA)=n-dimN(A^TA)=n-dimN(A)=rk(A)$ 
    
*Lemma4:*  $rank(A^T)=rank(A)$
     $rank(A^TA)=rank(A)\leq rank(A^T)$, so $rank(A)\leq rank(A^T) \leq rank(A)$, $rank(A)=rank(A^T)$      
     
So $rank(AB)=rank((AB)^T)=rank(B^TA^T)\leq rank(B^T)=rank(B)$ 

# Four fundamental space of A
## Intro.
Take a m\*n matrix $A$ .
1. column space $C(A)=\{\vec{b}\text{ }|\text{ }\vec{b}=A\vec{x},\vec{x}\in \mathbb{R}^n\}$ 
2. null space $N(A)=\{\vec{x}\text{ | }A\vec{x}=\vec{0}\}$ \
3. row space $C(A^T)$
4. left null space $N(A^T)$
**note:** $C(A^T)$ and $N(A)$ are subspace in $\mathbb{R}^n$ ,$C(A)$ and $N(A^T)$ are subspaces in $\mathbb{R}^m$ .
 
## Prop.

**$\mathbf{C(A^T)}$ is orthogonal to $\mathbf{N(A)}$ and $\mathbf{C(A^T)+N(A)=\mathbb{R}^n}$**
**Proof:** 
$$\text{For x in N(A) },A\vec{x}=\vec{0}\Longrightarrow\begin{bmatrix}\alpha_1\\\alpha_2\\\vdots\\\alpha_n\end{bmatrix}\begin{bmatrix}\vec{x_1}\\\vec{x_2}\\\vdots\\\vec{x_n}\end{bmatrix}=\begin{bmatrix}\alpha_1\vec{x}\\\alpha_2\vec{x}\\\vdots\\\alpha_n\vec{x} \end{bmatrix}=\begin{bmatrix}0\\0\\\vdots\\0\end{bmatrix}$$ So every vector $\vec{v}\in V$ ,$<\vec{v}^T,\vec{x_n}>=0$, so $C(A^T)$ is orthogonal to $N(A)$
*Def:* $W_1+W_2=\{\vec{v}\text{ | }\vec{v}=\vec{w_1}+\vec{w_2},\vec{w_1}\in W_1,\vec{w_2}\in W_2 \}$ 
![[An interesting insight from the method of finding the null space of A#Prop]]

From [[Vector Space#Dimension#Prop.]] lemma4 we know $rank(A^T)=rank(A)$ ,so$dimC(A^T)+dimN(A)=dimC(A)+dimN(A)=n$, so we can find n vector from $C(A^T)+N(A)$ are linear independent. So this is a basis of $\mathbb{R}^n$ .
[[Lecture 9.pdf#page=62&rect=103,54,821,212&color=important|Lecture 9, p.62]]
**note:** Similarly we can prove $C(A)$ and $N(A^T)$ are orthogonal and $C(A)+N(A^T)=\mathbb{R}^m$ 
Suppose $\vec{x}$ is a vector in $\mathbb{R}^n$ , and we proved $\mathbb{R}^n=C(A^T)+N(A)$ 
1.For $\vec{x}\in N(A)$ , then $A\vec{x}=\vec{0}$ .
2.For $\vec{x}\in C(A^T)$, then $A\vec{x}=\vec{b}$ . The def of $C(A)$ is $C(A)=\{\vec{b}\text{ }|\text{ }\vec{b}=A\vec{x},\vec{x}\in \mathbb{R}^n\}$ ,so we find $A$ change a vector in $\mathbb{R}^n$ to $C(A)$ . 
So we can consider $A$ as a linear map s.t :$$\begin{split}&\qquad\quad \mathbb{R}^n\longrightarrow\mathbb{R}^m\\&L_A:\\&\qquad\quad \vec{v}\longrightarrow A\vec{v}\end{split}$$

# Left inverse and right inverse

## Intro.
For a m\*n matrix $A$ at best we can find a $B$ that $AB=I$ or $BA=I$ 
1. $m>n=rkA$ : Left inverse exist
2. $n>m=rkA$ : Right inverse exist
Right inverse $C=A^T(AA^T)^{-1}$ , we want to show that for m\*n matrix $A$ , if $n>m=rkA$ ,then $(AA^T)^{-1}$ exist.
$$rkA=rkA^T=m\implies rkAA^T=m\implies (AA^T)^{-1}\text{exist}$$
From [[Vector Space#Dimension#Prop.]]Lemma 3 we prove that $rkA^TA=rkA$ ,so $rkAA^T=rkA^T$ 
Left inverse:
Take $A^TC=I \iff C^TA=I$ ,so left inverse: $C^T=(A^TA)^{-1}A^T$ 




 
  