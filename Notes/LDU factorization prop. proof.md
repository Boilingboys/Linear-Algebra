**Product of lower triangular matrices are also lower triangular matrix. Further more, if diagonal are all 1's, then so is the product.**
## Proof1:
For n=3:
 $$ \begin{pmatrix}a_{11} & 0 & 0 \\a_{21} & a_{22} & 0 \\a_{31} & a_{32} & a_{33} \\ \end{pmatrix}\cdot\begin{pmatrix}b_{11} & 0 & 0 \\b_{21} & b_{22} & 0 \\b_{31} & b_{32} & b_{33}\end{pmatrix} $$ $$(AB)_{12}=\begin{pmatrix}a_{11} & 0 &0&0\end{pmatrix}\begin{pmatrix}0\\b_{22}\\b_{32}\end{pmatrix}=0$$ We can see $(AB)_{ij}$ ，the first $i$ number of elements row of $A$ $=0$ ，the last $j$ number of elements of row of $B$ $=0$. 
 If $j>i$, then $i+j>n$ so the multiplication of them are all 0's. 
 so all $(AB)_{ij}=0$ if $i>j$ . 
 
##  

**If $A$ is non-singular, then LDU factorization is unique.**
## Proof2:
A is a non-singular matrix.
Suppose $A=L_1D_1U_1=L_2D_2U_2$  $U_1$ and $U_2$ are invertible($U$ is also non-singular from def [[Matrices and Gaussian Elimination#^fd94d3]])
$$L_2^{-1}L_1D_1=D_2U_2U_1^{-1}$$ left-side is lower triangular, right-side is upper triangular from proof1.

So $L_2^{-1}L_1=U_2U_1^{-1}=I$ , then $L_2=L_1$ $U_2=U_1$ $D_1=D_2$ .

