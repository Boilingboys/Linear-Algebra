
# Chapter1 Matrices and Gaussian Elimination


1. Consistency: If a linear system has at least one solution, it is called consistent. Otherwise, inconsistent.
    [[LA w1.pdf#page=1&rect=33,245,478,326&color=yellow|LA w1, p.1]]
2. Row Echelon Form and Reduced Row Echelon Form
3. Homogeneous equation 
    Equation in the form as $A\vec{x}=\vec{0}$
4. Inner product
        $<\vec{a},\vec{b}>=\vec{a^T}\cdot\vec{b}$
        [[Lecture 4.pdf#page=216&rect=86,314,761,397|Lecture 4, p.216]]
    Outer product
        $\vec{x}\cdot\vec{y^T}$  is the outer product of $\vec{x}$ and $\vec{y}$ .
        $(\vec{x}\cdot\vec{y^T})^n=(\vec{y^T}\cdot\vec{x})^{n-1}\vec{x}\cdot\vec{y^T}$
        [[Lecture 4.pdf#page=222&rect=176,426,668,534|Lecture 4, p.222]]
5. Matrix Multiplication Properties
    1. Distributivity
		$A(B+C)=AB+AC$
		[[LAw2.pdf#page=1&rect=40,523,294,614&color=yellow|LAw2, p.1]]
	2. Associativity
	    $(AB)C+A(BC)$
	    [[LAw2.pdf#page=2&rect=48,716,214,755&color=yellow|LAw2, p.2]]
6. Elementary matrices

	1. type1 permutation matrices
        [[LAw2.pdf#page=3&rect=66,668,219,745&color=yellow|LAw2, p.3]]
    2. Type2
        [[LAw2.pdf#page=3&rect=164,553,323,624&color=yellow|LAw2, p.3]]
    3. Type3 
        [[LAw2.pdf#page=3&rect=89,426,279,501&color=yellow|LAw2, p.3]] 
7. Left product and right product
    ![[LAw2.pdf#page=3&rect=47,97,516,207|LAw2, p.3]]
8. Singular & non-singular
    Def: n\*n matrix is non-singular if it has n pivots in its RREF.
    [[LAw2.pdf#page=4&rect=61,729,572,810&color=yellow|LAw2, p.4]]
    Prop:$A$ is n\*n matrix TFAE
       i) $A$ non-singular
       ii) $A\vec{x}=\vec{0}$ has unique solution $\vec{0}$
       iii) $A\vec{x}=\vec{b}$ has a unique solution for all $\vec{b}$
       [[LAw2.pdf#page=4&rect=48,533,567,721|LAw2, p.4]]
        Proof: 
            ![[Singular Prop. Proof#Proof]]  ^fd94d3
9. Inverse
    Def: $A$ is a n*n matrix B is a inverse of $A$ if $AB=BA=I$
        [[LAw2.pdf#page=6&rect=48,704,579,814|LAw2, p.6]]
    Prop: 
    1. Inverse is unique upon exist.
        Proof:![[Inverse Prop. Proof#Proof1]][[Lecture 4.pdf#page=70&rect=64,117,639,190|Lecture 4, p.70]]
    2. If A and B are invertible so is AB, furthermore $(AB)^{-1}=A^{-1}B^{-1}$ 
        Proof:![[Inverse Prop. Proof#Proof2]]
        [[Lecture 4.pdf#page=78&rect=41,431,826,588|Lecture 4, p.78]]
    3. A n\*n matrix A is invertible if and only if the elimination gives n pivots.
        Proof: 
10. LDU factorization
        A, n\*n matrix
        If A is non-singular:
          There exist $P=P_{1}P_{2}\dots P_k$ s.t $PA=LDU$
          $P\longleftrightarrow$ row exchange in elimination process
          $L\longleftrightarrow$ Lower triangle matrix
        If A is singular:
         There exists $P$ s.t $PA=LU$
         $U\longleftrightarrow$ without full set of pivots
         [[Lecture 3.pdf#page=149&rect=41,456,585,540|Lecture 3, p.149]]
         
    Prop:
    Product of lower triangular matrices are also lower triangular matrix. Further more, if diagonal are all 1's, then so is the product.
            Proof:
                ![[LDU factorization prop. proof#Proof1]]
     If $A$ is non-singular, then LDU factorization is unique.
            Proof:
                ![[LDU factorization prop. proof#Proof2]] 
11. Gauss-Jordan method
    Used to find the inverse of $A$
    $$\left[\begin{array}{c|c}A & I\end{array}\right]\longrightarrow\left[\begin{array}{c|c}A^{-1}&I\end{array}\right]$$         [[Lecture 4.pdf#page=121&rect=51,0,802,584|Lecture 4, p.121]]    
12. Transpose matrix and symmetric matrix
    Transpose matrix
     **Def:**
        $(A^T)_{ij}=A_{ji}$ 
    **Prop.**  
        i) $(A+B)^T=A^T+B^T$ 
        ii)$(AB)^T=B^TA^T$
        iii)$(A^{-1})^T=(A^T)^{-1}$
    **Proof:** 
        ![[Transpose matrix prop. proof#Proof1]]
        ![[Transpose matrix prop. proof#Proof2]]
        ![[Transpose matrix prop. proof#Proof3]]
    Symmetric matrix
    **Def:** $A$ is symmetric if $A^T=A$ .
    **Theorem:** Suppose there is a LDU factorization of a **non-singular symmetric**  matrix A, then $L^T=U$
        **Proof:**
        ![[Transpose matrix prop. proof#Proof4]]
to_chapter2:[[Vector Space]]