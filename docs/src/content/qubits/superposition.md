<section data-markdown>
### Qubits
##### Principle of Superposition

> Suppose $\ket{\psi}$ and $\ket{\sigma}$ are two mutually orthogonal vectors in a Hilbert space $\mathcal{H}$, and $a, b \in \mathbb{C}$.  
>
>Then $a \ket{\psi} + b \ket{\sigma} \in \mathcal{H}$ is a valid state vector of the state space of a qubit when $|a|^2 + |b|^2 = 1$.  
>

> Consider a state $\ket{\psi} = a \ket{0} + b \ket{1}$ and a state $\ket{\sigma} = a' \ket{0} + b' \ket{1}$  
> Let $a \ket{0} + b \ket{1} = c (a' \ket{0} + b' \ket{1})$ where $c \in \mathbb{C}$ and $|c| = 1$.   
> Then $\ket\psi$ and $\ket\sigma$ represent the same state.   
> The multiple $c \in \mathbb{C}$ with $|c| = 1$ by which two vectors representing the same quantum state vector differ is called the **global phase**.

---
### Qubits
* When working with Hilbert spaces associated with quantum systems, we normally use *orthonormal bases* to describe state vectors.
* The **computational basis** for the two dimensional complex vector space $\mathcal{H}$ is $\\{ \ket{0}, \ket{1} \\}$ where $\ket{0} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}$ and $\ket{1} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}$
* The **Hadamard Basis** for the two dimensional complex vector space $\mathcal{H}$ is  $\\{ \ket{+}, \ket{-} \\}$ where $\ket{+} = \displaystyle\frac{1}{\sqrt 2} (\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\ 1 \end{bmatrix}$  
  and $\ket{-} = \displaystyle\frac{1}{\sqrt 2} (\ket{0} - \ket{1}) = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\ -1 \end{bmatrix}$

---
### Qubits
##### Basic Properties of the computational basis

Using the orthonormality of the basis $\\{ \ket{0}, \ket{1} \\}$, we have the following facts:
* $\braket{0|0} = \bra{0}\ket{0} = 1$
* $\braket{1|1} = \bra{1}\ket{1} = 1$
* $\braket{1|0} = \bra{1}\ket{0} = 0$ 
* $\braket{0|1} = \bra{0}\ket{1} = 0$

If $\ket{v}$ is a state vector and $\ket{v} = \begin{bmatrix} a \\\\ b \end{bmatrix} \in \mathcal{H}$ with respect to the computational basis, then: 
* $\braket{0|v} = a$ 
* $\braket{1|v} = b$ 
* $\ket{v} = a \ket{0} + b \ket{1} = \braket{0|v} \ket{0} + \braket{1|v} \ket{1}$
</section>


