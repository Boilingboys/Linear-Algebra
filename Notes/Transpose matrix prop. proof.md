$\mathbf{(A+B)^T=A^T+B^T}$ 
# Proof1:
$((A+B)^T)_{ij}=a_{ji}+b_{ji}=(A^T)_{ij}+(B^T)_{ij}$

## 
$\mathbf{ (AB)^T=B^T A^T }$
# Proof2:
$$((AB)^T)_{ij}=\sum_{k=1}^{n}a_{jk}b_{ki}$$
$$(B^TA^T)_{ij}=\sum_{k=1}^nb_{ki}a_{jk}=((AB^T))_{ij}$$

## 
$\mathbf{(A^{-1})^T=(A^T)^{-1}}$
# Proof3:
$$(AA^{-1})^T=(A^{-1})^TA^T=I$$ 
##
**If A is a symmetric matrix, then $\mathbf{A=LDU}$, gives $\mathbf{L^T=U}$**
# Proof4:
$$A=LDU=A^T=U^TD^TL^T$$ We can see $U^T$ is a lower triangular and $L^T$ is a upper triangular, so $A=U^TD^TL^T$ is also a LDU factorization. Given that LDU factorization is unique, so $L^T=U$.
