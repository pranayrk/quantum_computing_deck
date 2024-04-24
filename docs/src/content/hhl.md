<section>
<section data-markdown>
### HHL Algorithm

>  Consider a system of linear equations represented as $A \vec{x} = \vec{b}$ where $A$ is an $N\times N$ *self-adjoint* matrix and $\vec{x}$ and $\vec{b}$ are $N$-dimensional vectors.  
> Find the solution $\vec{x} = A^{\-1} \vec{b}$

* Can also be applied to non-self-adjoint matrices $A$ by using the block matrix $\begin{bmatrix}
        0 & A \\\\ A^\dagger & 0
    \end{bmatrix}$ which is self-adjoint
* The *Conjugate Gradient Method* has a time complexity of $O(N)$
* HHL Algorithm finds the solution in $O(\log N)$

Note:
2008
</section>
<section data-markdown>
### HHL Algorithm
This algorithm makes use of the following theorem.
> **Spectral Theorem:** If $A$ is Hermitian on a vector space $V$, then there exists an orthonormal basis of $V$ consisting of eigenvectors of $A$. 
> Each eigenvalue of $A$ is real.

$A$ is diagonalizable precisely when there are exactly $N$ linearly independent eigenvectors.
</section>
<section data-markdown>
### HHL Algorithm
Let the eigenvectors of the matrix $A$ be $\ket{\phi_0}, \ket{\phi_1}, ..., \ket{\phi_{N-1}}$ where each eigenvector $\ket{\phi_i}$ is associated to an eigenvalue $\lambda_i$.

> The self-adjoint matrix $A$ can be written as a linear combination of outer products of its eigenvectors as $$A = \sum_{j=0}^{N-1} \lambda_j \ket{\phi_j}\bra{\phi_j}$$

</section>
<section data-markdown>
### HHL Algorithm
* $A = \sum_{j=0}^{N-1} \lambda_j \ket{\phi_j}\bra{\phi_j} \implies A^{-1} = \sum_{j=0}^{N-1} \lambda_j^{-1} \ket{\phi_j}\bra{\phi_j}$
* Let $\ket{b} = \sum_{i=0}^{N-1} b_i \ket{\phi_i}$ in the eigenvector basis of $A$.

* Then $\ket{x}$ can be written in the eigenvector basis of $A$ as  
$$\begin{aligned}
    \ket{x} & = A^{-1} \ket{b} \\\\
            & = \left (\sum_{j=0}^{N-1} \lambda_j \ket{\phi_j}\bra{\phi_j} \right ) \left (\sum_{i=0}^{N-1} b_i \ket{\phi_i} \right) \\\\
            & = \sum_{j=0}^{N-1} \lambda_j^{-1} b_j \ket{\phi_j}
\end{aligned}$$
</section>
<section data-markdown>
### HHL Algorithm

> Let $U = e^{i A t}$ where $t \in \mathbb{R}$ represents the time-evolution of the unitary.   
> Then $U$ is a unitary matrix. 

> The eigenvectors of $A$ are the eigenvectors of $U = e^{iAt}$ and for each eigenvector $\ket{\phi_i}$ of $A$, we have  $$U \ket{\phi_i} = e^{i \lambda_i t} \ket{\phi_i}$$
        
    
</section>

<section>
<h3>HHL Algorithm</h3>
<img src="media/hhl.png"></img>
</section>
</section>

