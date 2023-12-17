<section data-markdown>
### Tensor Product
> Let $\ket\psi = \begin{bmatrix} a \\\\ b \end{bmatrix} \in \mathcal{H}\_1$ and $\ket\phi = \begin{bmatrix} c \\\\ d \end{bmatrix} \in \mathcal{H}\_2$  
> The **tensor product** of $\ket\psi$ and $\ket\phi$ is defined as $\ket\psi \otimes \ket\phi = \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \end{bmatrix} = \begin{bmatrix} a \begin{bmatrix} c \\\\ d \end{bmatrix} \\\\ b \begin{bmatrix} c \\\\ d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\ ad \\\\ bc \\\\ bd \end{bmatrix}$ 


* $\ket{0} \otimes \ket{0} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 1 \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \\\\ 0 \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix}$
* Similarly, $\ket{0} \otimes \ket{1} = \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \\\\ 0 \end{bmatrix}$, $\ket{1} \otimes \ket{0} = \begin{bmatrix} 0 \\\\ 0 \\\\ 1 \\\\ 0 \end{bmatrix}$ and $\ket{1} \otimes \ket{1} = \begin{bmatrix} 1 \\\\ 1 \\\\ 1 \\\\ 1 \end{bmatrix}$

---

### Tensor Product

> The notation $\ket\psi \otimes \ket\phi$ is often simplified as $\ket\psi \ket\phi$ or $\ket{\psi \phi}$

> Let $\ket{\psi_1}, \ket{\psi_2} \in \mathcal{H}\_1$ and $\ket{\phi_1}, \ket{\phi_2} \in \mathcal{H}\_2$.
> The inner product of the tensors $\ket{\psi\_1} \otimes \ket{\phi\_1}$  
>  and $\ket{\psi\_2} \otimes \ket{\phi\_2}$ is defined as  
> $\braket{\\; \ket{\psi\_1} \otimes \ket{\phi\_1} \\; | \\; \ket{\psi\_2} \otimes \ket{\phi\_2} \\;} = ( \\; \bra{\psi\_1} \otimes \bra{\phi\_1} \\; | \\; \ket{\psi\_2} \otimes \ket{\phi\_2} \\; ) = \braket{\psi\_1 | \psi\_2} \braket{\phi\_1 | \phi\_2}$

* *Example:* $\braket{\\; \ket{01} \\; | \\; \ket{11} \\;} = \braket{0|1} \braket{1|1} = 0 \cdot 1 = 0$
* *Example:* $\braket{\\; \ket{01} \\; | \\; \ket{11} \\;} = \braket{0|0} \braket{1|1} = 1 \cdot 1 = 1$
* Similarly, taking all combinations, we can see $\\{ \\; \ket{00}, \ket{01}, \ket{10}, \ket{11} \\; \\}$ is an orthogonal set and linearly independent
* $\\{ \\; \ket{00}, \ket{01}, \ket{10}, \ket{11} \\; \\}$ forms an orthonormal basis for a space of dimension 4

---
### Qubits
##### Principle of Entanglement

> Given an ONB $\\{ \ket{ e\_{i}} \\}\_{i = 1}^n$ for $\mathcal{H}\_1$ and an ONB $\\{ \ket{f_{j}} \\}\_{j = 1}^m$ for $\mathcal{H}\_2$, we have $\\{ \ket{e\_{i}} \otimes \ket{f\_{j}} \\}$ is an orthonormal basis for the **tensor product space** $\mathcal{H}\_1 \otimes \mathcal{H}\_2$.

> When we have two qubits being treated as a combined system, the state space of the combined system is the tensor product $\mathcal{H}\_1 \otimes \mathcal{H}\_2$ of the state spaces $\mathcal{H}\_1, \mathcal{H}\_2$ of the component qubit subsystems.
>
> Further, for a system of $n$ interacting qubits, the combined state space is the tensor product  
> $\mathcal{H}\_1 \otimes \mathcal{H}\_2 \otimes ... \otimes \mathcal{H}\_n$ of the state spaces of the $n$ qubits taken independently.

* Given the computational basis $\\{ \\; \ket{0}, \ket{1} \\; \\}$ for $\mathcal{H}\_1$ and the computational basis $\\{ \\; \ket{0}, \ket{1} \\; \\}$ for $\mathcal{H}\_2$. Then $\\{ \\; \ket{00}, \ket{01}, \ket{10}, \ket{11} \\; \\}$ is an ONB for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$ called the **computational basis** for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$ and is also denoted as $\\{ \ket{0}, \ket{1}, \ket{2}, \ket{3} \\}$

---
### Qubits
* For $1$ qubit, the computational basis is $\\{ \ket{0}, \ket{1} \\}$
* For $2$ qubits, the computational basis is $\\{ \ket{0}, \ket{1}, \ket{2}, \ket{3} \\}$ where
   * $\ket{0} = \ket{00} = \ket{0} \otimes \ket{0}$
   * $\ket{1} = \ket{01} = \ket{0} \otimes \ket{1}$
   * $\ket{2} = \ket{10} = \ket{1} \otimes \ket{0}$
   * $\ket{3} = \ket{11} = \ket{1} \otimes \ket{1}$
* For $n$ qubits, the computational basis is $\\{ \ket{0}, \ket{1}, ..., \ket{2^n - 1} \\}$ where
    * $\ket{0} = \ket{00...00} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}\_{n\text{ times }}$
    * $\ket{1} = \ket{00...01} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}\_{n-1\text{ times }} \otimes \ket{1}$
    * $\ket{2^n - 1} = \ket{11...11} = \underbrace{\ket{1} \otimes \ket{1} \otimes ... \otimes \ket{1}}\_{n\text{ times }}$
---
### Qubits
* Another commonly used basis for a $2$-qubit system is the **Bell Basis** which is the set of Bell states $\\{ \\; \ket{\phi^+}, \ket{\phi^-}, \ket{\psi^+}, \ket{\psi^-} \\; \\}$ where:
* $\ket{\phi^+} = \frac{1}{\sqrt{2}} ( \ket{00} + \ket{11} ) = \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ 0 \\\\ 0 \\\\ \frac{1}{\sqrt{2}} \end{bmatrix}$ and $\ket{\phi^-} = \frac{1}{\sqrt{2}} ( \ket{00} - \ket{11} ) = \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ 0 \\\\ 0 \\\\ - \frac{1}{\sqrt{2}} \end{bmatrix}$
* $\ket{\psi^+} = \frac{1}{\sqrt{2}} ( \ket{01} + \ket{10} ) = \begin{bmatrix} 0 \\\\ \frac{1}{\sqrt{2}} \\\\ \frac{1}{\sqrt{2}}\\\\ 0  \end{bmatrix}$ and $\ket{\psi^-} = \frac{1}{\sqrt{2}} ( \ket{01} - \ket{10} ) = \begin{bmatrix} 0 \\\\ \frac{1}{\sqrt{2}} \\\\ - \frac{1}{\sqrt{2}} \\\\ 0 \end{bmatrix}$
* The Bell states are orthonormal
* Bell states are of fundamental importance to quantum information processing. Particularly for their use for quantum teleportation and dense coding.

---
### Qubits

> A state $\ket{\psi} \in \mathcal{H}\_1 \otimes \mathcal{H}\_2 \otimes ... \otimes \mathcal{H}\_n$ is said to be **entangled** if it cannot be written as a tensor product of state vectors $\ket{v\_1} \in \mathcal{H}\_1, \ket{v\_2} \in \mathcal{H}\_2, ..., \ket{v\_n} \in \mathcal{H}\_n$.
>
> The state is said to be **seperable** if we can write $\ket{\psi} = \ket{v\_1} \otimes \ket{v\_2} \otimes ... \otimes \ket{v\_n} = \ket{v\_1 v\_2...v\_n}$  
> for some $\ket{v\_i} \in \mathcal{H}\_i$.

* *Example:* The state $\ket{\psi} = \frac{1}{\sqrt{2}} (\ket{01} + \ket{11})$ of a $2$-qubit system is seperable since we can write $\ket{\psi} = \ket{+} \otimes \ket{1} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) \otimes \ket{1}$
* *Example:* The state $\ket{\psi^+} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11})$ of a $2$-qubit system is an entangled state. 
* In fact all the Bell states are entangled states

</section>
