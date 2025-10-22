**Prop.1** Inverse is unique upon exist.
# Proof1:
Suppose $AB=AC=I$ , and $B\neq C$ .
$CAB=C(AB)=CI=C$  ,$CAB=(CA)B=B$ , then $C=B$.
Conflict!


##
**Prop.2** If A and B are invertible so is AB, furthermore $(AB)^{-1}=A^{-1}B^{-1}$ 
# Proof2:
$AB\cdot B^{-1}A^{-1}=I$
so $(AB)^{-1}=A^{-1}B^{-1}$ 
##
**Prop.3** A n\*n matrix A is invertible if and only if the elimination gives n pivots.
# Proof3:
Factorize $A$ : $A=PLU$. 
**Lemma:**$P$ and $L$ are invertible 
**Pf.**  We can see $P=P_1P_2P_3\dots P_k$ every $P_i$ is an exchange of 2 row, so $P_i$ is invertible, because $P_iP_i=I$. So the multiplication of $P_i$ is invertible(from prop.1).
We can also see $L=E_1E_2E_3\dots E_n$ is invertible if any $E_i$ is invertible.
The effect of $E_i$ is $k\cdot \text{row}n+\text{row}m \rightarrow \text{row}m$    , so we can always find a $E_i^{'}$ s.t the effect is $-k\cdot \text{row}n+\text{row}m \rightarrow \text{row}m$, so $A \cdot E_iE_i^{'}=A=A(I)$ , every $E_i$ is invertible so $L$ is invertible.
$$\text{So }A \text{ is invertible }\Longleftrightarrow \text{ }B \text{ is invertible} $$

Next we want to prove: **$U$ is invertible if and only $U$ has n pivots.**  
**Pf.** Suppose $U$ has inverse and $U$ doesn't has n pivots, so $$U=\begin{pmatrix}* & \dots & *\\ \vdots & \ddots & \vdots\\ 0 & \dots &0 \end{pmatrix}\text{ the last k rows of U are all 0's.}$$ 
 So $(U\cdot U_{-1})_{ii}=0(\text{if }i>n-k)$, it can't be $I$. 
 Next we want to show that **$U$ with n pivots is invertible.**
 Let $U$ be 3\*3 matrix
 $$ U=\begin{pmatrix} d_1 & * & *\\ 0 & d_2 & *\\ 0& 0 &d_3\end{pmatrix}=\begin{pmatrix}d_1&0&0\\0&d_2&0\\0&0&d_3\end{pmatrix}\begin{pmatrix}1&*&*\\0&1&*\\0&0&1\end{pmatrix}=D\tilde{U}$$ For $\tilde{U}$, we can easily know that it is invertible using the same method proving $L$ is invertible.
 

 

