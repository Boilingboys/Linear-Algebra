### Expert-Level Linear Algebra Exercises (Strang, Chapters 1-3.2)

This problem set is for those seeking a deep, theoretical challenge. The problems require abstract reasoning and proofs based on the fundamental concepts of vector spaces, subspaces, orthogonality, and linear transformations, often in non-standard settings.

1.  **The Geometry of the Pseudoinverse**
    Let $A$ be an $m \times n$ matrix. The Moore-Penrose pseudoinverse, $A^+$, is the unique matrix satisfying four specific properties. For the simplified case where $A$ has full column rank ($r=n$), we defined the left-inverse as $A^+_L = (A^TA)^{-1}A^T$. For the case where $A$ has full row rank ($r=m$), the right-inverse is $A^+_R = A^T(AA^T)^{-1}$.
    (a) Prove that the matrix $P = A^+_L A$ is the projection matrix onto the row space of $A$, $C(A^T)$.
    (b) Prove that the matrix $Q = A A^+_R$ is the projection matrix onto the column space of $A$, $C(A)$.
    (c) Consider an arbitrary vector $\mathbf{x} \in \mathbb{R}^n$. Show that $A^+_L A \mathbf{x}$ gives the component of $\mathbf{x}$ that lies in the row space of $A$. In other words, prove that $\mathbf{x} - A^+_L A \mathbf{x}$ is in the nullspace $N(A)$. This shows that $A^+_L A$ acts as an orthogonal projector from $\mathbb{R}^n$ onto $C(A^T)$.

2.  **Linear Transformations on Matrix Spaces**
    Let $V$ be the vector space of all $n \times n$ real matrices. Consider the linear transformation $T: V \to V$ defined by $T(A) = A - A^T$.
    (a) Describe the kernel of $T$. What is its dimension?
    (b) Describe the image of $T$. What is its dimension?
    (c) Show that the kernel of $T$ and the image of $T$ are orthogonal subspaces under the inner product $\langle A, B \rangle = \text{trace}(A^TB)$. (This inner product is known as the Frobenius inner product).

3.  **Nullspace of Block Matrices**
    Let $A$ be an $m \times n$ matrix and $B$ be an $m \times p$ matrix. Consider the block matrix $C = \begin{pmatrix} A & B \end{pmatrix}$.
    (a) Prove that the nullspace $N(C)$ is isomorphic to the intersection of the nullspaces of two related transformations.
    (b) Now, consider a different block matrix $M = \begin{pmatrix} A & I \\ 0 & A^T \end{pmatrix}$, where $A$ is $m \times n$. Prove that the dimension of the nullspace of $M$ is equal to the dimension of the nullspace of $A^TA$. Use this to relate $\dim N(M)$ to the rank of $A$.

4.  **The Angle Between Subspaces**
    The angle $\theta$ between two subspaces $F$ and $G$ of $\mathbb{R}^n$ is defined by
    $$ \cos(\theta) = \max_{\mathbf{u} \in F, \mathbf{v} \in G} \frac{\mathbf{u}^T \mathbf{v}}{\|\mathbf{u}\| \|\mathbf{v}\|} $$
    Let $F$ be the subspace spanned by the columns of a matrix $A$ and let $G$ be the subspace spanned by the columns of a matrix $B$. Show how you could compute $\cos(\theta)$ using projection matrices $P_F$ and $P_G$. (Hint: Consider the operator norm $\|P_G P_F\|_2 = \max_{\|\mathbf{x}\|=1} \|P_G P_F \mathbf{x}\|$.)

5.  **Uniqueness of Reduced Row Echelon Form**
    Prove that the reduced row echelon form (RREF) of a matrix $A$ is unique. (This is a cornerstone result that is often used but rarely proven in introductory courses).
    *Hint: Assume $R_1$ and $R_2$ are two different RREFs of $A$. Let $\mathbf{x}$ be a solution to $A\mathbf{x}=0$. Then $R_1\mathbf{x}=0$ and $R_2\mathbf{x}=0$. Let $j$ be the first column where $R_1$ and $R_2$ differ. Show that this leads to a contradiction by constructing a special vector in the nullspace.*

6.  **Fredholm Alternative**
    Prove the Fredholm Alternative theorem: For any $m \times n$ matrix $A$, exactly one of the following systems has a solution:
    (i) $A\mathbf{x} = \mathbf{b}$
    (ii) $A^T\mathbf{y} = \mathbf{0}$ with $\mathbf{y}^T\mathbf{b} \neq 0$
    This provides a deep connection between the column space $C(A)$ and the left nullspace $N(A^T)$. (Hint: The theorem is essentially a restatement of the orthogonality of these two subspaces).

7.  **The QR Decomposition and Linear Independence**
    Let $A$ be an $m \times n$ matrix with linearly independent columns. The Gram-Schmidt process gives a decomposition $A=QR$, where $Q$ has orthonormal columns and $R$ is upper triangular.
    (a) Prove that $R$ must be invertible.
    (b) Show that the projection matrix onto the column space of $A$ can be expressed simply as $QQ^T$. Why is this computationally better than the formula $A(A^TA)^{-1}A^T$?
    (c) Prove that the QR decomposition of an invertible square matrix is unique if we require the diagonal entries of $R$ to be positive.

8.  **Nilpotent Transformations**
    A linear transformation $T: V \to V$ is called nilpotent if $T^k = 0$ for some positive integer $k$ (where $T^k$ is $T$ composed with itself $k$ times).
    (a) Let $A$ be a strictly upper triangular $n \times n$ matrix (i.e., $A_{ij}=0$ for $i \ge j$). Prove that $A$ is nilpotent.
    (b) If $T$ is a nilpotent transformation, prove that $(I-T)$ is invertible. Find its inverse. (Hint: Think about geometric series).
    (c) Prove that the only eigenvalue of a nilpotent matrix is 0.

9.  **Commuting Matrices and Subspaces**
    Let $A$ and $B$ be two $n \times n$ matrices such that $AB=BA$.
    (a) Prove that the nullspace of $B$, $N(B)$, is an invariant subspace under $A$. (This means that for any $\mathbf{x} \in N(B)$, it must be that $A\mathbf{x}$ is also in $N(B)$).
    (b) Prove that the column space of $B$, $C(B)$, is also an invariant subspace under $A$.

10. **The Jordan Form for a $2 \times 2$ Matrix**
    Let $A$ be a $2 \times 2$ matrix that is *not* diagonalizable. This happens when $A$ has a repeated eigenvalue $\lambda$ but its eigenspace has dimension 1 (i.e., there is only one line of eigenvectors).
    (a) Let $\mathbf{v}_1$ be an eigenvector, so $(A-\lambda I)\mathbf{v}_1 = \mathbf{0}$. A "generalized eigenvector" $\mathbf{v}_2$ is a vector that satisfies $(A-\lambda I)\mathbf{v}_2 = \mathbf{v}_1$. Prove that such a $\mathbf{v}_2$ must be linearly independent from $\mathbf{v}_1$.
    (b) Let $M$ be the matrix whose columns are $\mathbf{v}_1$ and $\mathbf{v}_2$. Show that $A M = M J$, where $J = \begin{pmatrix} \lambda & 1 \\ 0 & \lambda \end{pmatrix}$. This proves that any non-diagonalizable $2 \times 2$ matrix is similar to a Jordan block.