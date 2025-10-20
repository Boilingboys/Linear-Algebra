# Introduce:
**say:** **A is a m\*n matrix and has m-k pivots and k free-variables.**
Later we will know that this method gives a base of A. The reason is that since every pivots can be determined by the free variable, so we take all the possible values of free variables can determined all possible values of $\vec{x}$ . Note one possible values of free variables as:  $\vec{f}$ 
    So all $\vec{f}\in F\text{ (let F be the vector space containing all possible value of free variables)}$ can be written as: $$\vec{f}=c_1\begin{pmatrix}1\\0\\\vdots\\0\\0\end{pmatrix}+c_2\begin{pmatrix}0\\1\\\vdots\\0\\0\end{pmatrix}+\cdots+c_i\begin{pmatrix}0\\\vdots\\1\\\vdots\\0\end{pmatrix}+\cdots+c_n\begin{pmatrix}0\\0\\\vdots\\0\\1\end{pmatrix}\text{   all }c_k\in\mathbb{R}$$ So what we do is we take one basis of $F$, and solve one $\vec{x}$ ,we can further prove that $\vec{x}$ is also a basis of $N(A)$. There are 2 things we need to prove:
        1. for every $\vec{f_i}$ , $\vec{x_i}$ is unique.
        2. for every $\vec{f}\longrightarrow\vec{x}$ , if $\vec{f}=c_1\vec{f_1}+\cdots+c_n\vec{f_n}$ , then $\vec{x}=d_1\vec{x_1}+\cdots+d_n\vec{x_n}$ . 
        Where:$$\begin{split}&\vec{f_1}\longrightarrow\vec{x_1}\\&\vec{f_2}\longrightarrow\vec{x_2}\\&\text{ }\text{  }\text{  }\text{  }\text{  }\text{  }\text{  }\vdots\\&\vec{f_n}\longrightarrow\vec{x_n}\end{split}$$
    If proved, we actually construct a base of $N(A)$ from the basis of $F$ , next we want to see why this can be happened.
    Before the proof, we first extend $\vec{f}$ to an vector in $\mathbb{R}^m$ : $$\vec{f'}=\begin{pmatrix}0 \\ f_1\\ \vdots \\f_i \\ \vdots\\0\end{pmatrix}\text{ }f_i\text{ is in the row that the corresponding x is free variable, and the other rows are all 0's. }$$
    (e.g. $x_k=f_i$ ,so $f'_k=f_i$ )
    Later, we write all the $f'$ and $F'$ as $f$ and $F$ 
    And we introduce $\vec{p}$ to describe the values of pivots in the same way we did for $\vec{f}$  $$\vec{p}=\begin{pmatrix}p_1 \\ p_1\\ \vdots \\p_i \\ \vdots\\0\end{pmatrix}$$
    The vector space that all $\vec{p}$ formed is $P$ .
    From the definition we can see $\vec{p}+\vec{f}=\vec{x_n}$ .
    [[Lecture 8.pdf#page=126&rect=41,40,798,540&color=important|Lecture 8, p.126]]
# Core concept
## Def:
### Orthogonal vector spaces:
Vector space $U$ and vector space $V$ are orthogonal ,if for any $u,v \in U,V ,<u,v>=0$ .
### Direct sum:
Let $U_1$ , $U_2$ be the subspaces of $V$ , ,if any $\vec{v}\in V$  , the way we write $\vec{v}=\vec{u_1}+\vec{u_2}$ ,is unique. We say $V$ is the direct sum of $U_1$ and $U_2$ ,noted as $U_1\oplus U_2=V$ 

## Prop:
**If U and V are orthogonal, then for $\mathbf{U\cap V=\{\vec{0}\}}$  .** 
    **proof:** 
        let $x\in U\cap V$ ,  $<x,x>=0$ , because x is in U, and x is in V, the inner product of a vector in U and a vector in V equals 0.
**If $\mathbf{U\cap{V}=\{\vec{0}\}}$ , a basis of $V$ and a basis of $U$ are linear independent, furthermore, the vector space of it is $U\oplus V$ .** 
    **proof:**
         let $c_1\vec{v_1}+\cdots+c_n\vec{v_n}+d_1\vec{u_1}+\cdots+d_m\vec{u_m}=\vec{0}$ :
         so: $c_1\vec{v_1}+\cdots+c_n\vec{v_n}=-(d_1\vec{u_1}+\cdots+d_m\vec{u_m})$ , L.H.S is in V, R.H.S. is in U, so L.H.S=R.H.S=0. So, $c_1=\cdots=c_n=d_1=\cdots=d_m=0$ ,they are independent.
         We can write any $\vec{v}=c_1\vec{v_1}+\cdots+c_n\vec{v_n}+d_1\vec{u_1}+\cdots+d_m\vec{u_m}=\vec{v}+\vec{u}$ ,which is unique.
# Proof:
First, we show that $P$ and $V$ are orthogonal, because $<\vec{p},\vec{f}>=0$ .  From the prop. and $\vec{x_n}=\vec{p}+\vec{f}$, so $N(A)=P\oplus F$ ,thus for every $\vec{f_i}$ , $\vec{x_i}$ is unique.
	Next, because $p_i$ can be written as the linear combination of free variables(From the process of solving the equation), we can write a matrix to describe the connection between $\vec{p}$ and $\vec{f}$ :$$\vec{p}=\begin{pmatrix}p_1 \\ p_1\\ \vdots \\p_i \\ \vdots\\0\end{pmatrix}=\begin{pmatrix}c_{11}&c_{12}&\cdots&c_{1n}\\0&0&\cdots&0\\ \vdots&\vdots&\ddots&\vdots\\c_{i1}&c_{i2}&\cdots&c_{in}\\\vdots&\vdots&\ddots&\vdots\\0&0&0&0\end{pmatrix}\begin{pmatrix}0 \\ f_1\\ \vdots \\f_i \\ \vdots\\0\end{pmatrix}=C\vec{f}$$
 So :$$\begin{split}\vec{x}&=C\vec{f}+\vec{f}\\\Longrightarrow \vec{x}&=d_1\vec{x_1}+\cdots+d_n\vec{x_n}=C(c_1\vec{f_1}+\cdots+c_n\vec{f_n})+c_1\vec{f_1}+\cdots+c_n\vec{f_n}\\&=c_1(C\vec{f_1}+\vec{f_1})+c_2(\vec{f_2}+\vec{f_2})+\cdots+c_n(C\vec{f_n}+\vec{f_n})\end{split}$$
 Given that every $\vec{x_i}$  is unique , so for every $\vec{f}\longrightarrow\vec{x}$ , if $\vec{f}=c_1\vec{f_1}+\cdots+c_n\vec{f_n}$ , then $\vec{x}=c_1\vec{x_1}+\cdots+d_n\vec{x_n}$ . Where:$$\begin{split}&\vec{f_1}\longrightarrow\vec{x_1}\\&\vec{f_2}\longrightarrow\vec{x_2}\\&\text{ }\text{  }\text{  }\text{  }\text{  }\text{  }\text{  }\vdots\\&\vec{f_n}\longrightarrow\vec{x_n}\end{split}$$

# Reflection:
We construct a map from $F$ to $N(A)$ where a base of $F$ mapped to a base of $N(A)$ . We say $F$ and $N(A)$ are isomorphic. Now the problem is why this mapping could happened, what's the condition.
[[Vector Space#Linear independence#Prop]] From here we can see $C+I$ is an invertible matrix.