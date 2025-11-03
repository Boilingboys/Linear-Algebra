



1.  **Geometric Interpretation**
    Let $V = \mathbb{R}^3$ and let $W$ be the subspace spanned by the vector $(1, 1, 1)$, i.e., $W = \text{span}\{(1, 1, 1)\}$. Describe the elements of the quotient space $V/W$ geometrically. What is the dimension of $V/W$?

2.  **Polynomial Spaces**
    Let $V = P_3(\mathbb{R})$ be the vector space of all real polynomials of degree at most 3. Let $W = P_1(\mathbb{R})$ be the subspace of all real polynomials of degree at most 1.
    (a) What is the dimension of the quotient space $V/W$?
    (b) Find a basis for $V/W$.
    (c) Express the coset $[x^3 + 2x^2 + 3x + 4]$ as a linear combination of your basis vectors.

3.  **Quotient Norm Calculation**
    Consider the space $V = C[0, 1]$ with the supremum norm $\|f\|_\infty = \sup_{t \in [0, 1]} |f(t)|$. Let $W$ be the subspace of functions that are zero at the endpoints, i.e., $W = \{g \in C[0, 1] \mid g(0) = g(1) = 0\}$. Let $f(t) = t$. Compute the norm of the coset $[f]$ in the quotient space $V/W$, which is defined as $\|[f]\|_{V/W} = \inf_{g \in W} \|f+g\|_\infty$.

4.  **The Natural Projection Map**
    Let $V$ be a vector space and $W$ be a subspace of $V$. Prove that the canonical projection map $\pi: V \to V/W$ defined by $\pi(v) = [v] = v+W$ is a surjective linear transformation with $\ker(\pi) = W$.

5.  **The First Isomorphism Theorem**
    Let $T: V \to U$ be a linear transformation between two vector spaces $V$ and $U$. Prove that the quotient space $V/\ker(T)$ is isomorphic to the image of $T$, i.e., $V/\ker(T) \cong \text{Im}(T)$.

6.  **The Quotient Norm**
    Let $(V, \|\cdot\|)$ be a normed vector space and let $W$ be a closed subspace of $V$. For any coset $[v] \in V/W$, we define the quotient norm as
    $$ \|[v]\|_{V/W} = \inf_{w \in W} \|v+w\| $$
    Prove that this defines a valid norm on the quotient space $V/W$. (You need to show that it's well-defined and satisfies the three axioms of a norm). Why is the condition that $W$ is a *closed* subspace important?

7.  **Completeness of Quotient Spaces (Banach Spaces)**
    Prove that if $V$ is a Banach space and $W$ is a closed subspace of $V$, then the quotient space $V/W$ (equipped with the quotient norm) is also a Banach space.

8.  **Quotient Spaces in Hilbert Spaces**
    Let $H$ be a Hilbert space and let $M$ be a closed subspace of $H$. Let $M^\perp$ be the orthogonal complement of $M$. Prove that the quotient space $H/M$ is isometrically isomorphic to $M^\perp$.

9.  **A Non-Closed Subspace**
    Let $V = C[0, 1]$ with the supremum norm $\| \cdot \|_\infty$. Let $W$ be the subspace of all polynomial functions. Show that $W$ is not a closed subspace of $V$. What does this imply for the quotient space $V/W$ and the quotient norm?

10. **Dual Space of a Quotient Space**
    Let $V$ be a normed vector space and $W$ be a closed subspace. Let $V^*$ be the dual space of $V$. Define the annihilator of $W$, denoted $W^\perp$, as
    $$ W^\perp = \{f \in V^* \mid f(w) = 0 \text{ for all } w \in W\} $$
    Prove that the dual space of the quotient $V/W$, denoted $(V/W)^*$, is isometrically isomorphic to the annihilator $W^\perp$.