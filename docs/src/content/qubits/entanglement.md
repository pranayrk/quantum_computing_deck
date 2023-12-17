<section data-markdown>
### Tensor Product Space
> Consider we have finite dimensional Hilbert spaces $\mathcal{H}\_1$ and $\mathcal{H}\_2$.  
> Consider fixed vectors $\ket{\psi} \in \mathcal{H}\_1$ and $\ket{\phi} \in \mathcal{H}\_2$  
> Define a function $f_{\psi,\phi}: \mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C}$ as $f_{\psi,\phi}(\ket\xi, \ket\eta) = \braket{\xi|\psi}\_{\mathcal{H}\_1} \braket{\eta | \phi}\_{\mathcal{H}\_2}$   
> for some $\ket{\xi} \in \mathcal{H}\_1, \ket{\eta} \in \mathcal{H}\_2$.  
>   
> Then the function $f\_{\psi,\phi}$ is conjugate linear and continuous.


> The function $f_{\psi, \phi}$ is known as the **tensor product** of $\ket\psi$ and $\ket\phi$.
>
> In Dirac bra/ket notation, the function $f_{\psi,\phi}$ is denoted as $\ket{\psi} \otimes \ket{\phi}$ &nbsp; or &nbsp;  $\ket\psi \ket\phi $ &nbsp; or &nbsp;  $\ket{\psi\phi}$

---
### Tensor Product Space

> Given two Hilbert spaces $\mathcal{H}\_1$ and $\mathcal{H}\_2$, consider $\mathcal{G}$ to be the set of all anti-linear and continuous functions from $\mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C}$.  
>
> Then $G = \\{ g: \mathcal{H}\_1 \times \mathcal{H}\_2 \\; | \\; g \text{ is antilinear and continuous } \\}$ is a  
> vector space over $\mathbb{C}$ with vector addition  
> defined as $[g\_1 + g\_2](\ket\xi, \ket\eta) = g\_1(\ket\xi, \ket\eta) + g\_2(\ket\xi, \ket\eta)$   
> and scalar multiplication defined as expected.

> Consider $\mathcal{F} = \\{ \\; \ket\psi \otimes \ket\phi \\;\\; | \\;\\; \ket\psi \in \mathcal{H}\_1 \text{ and } \mathcal{H}\_2 \\}$  
> Then $\mathcal{F} \subseteq \mathcal{G}$.

---
### Tensor Product Space

> Let $\\{ \ket{ e\_{i}} \\}\_{i = 1}^n$ be an orthonormal basis for $\mathcal{H}\_1$ and $\\{ \ket{f_{j}} \\}\_{j = 1}^m$ be an orthonormal basis for $\mathcal{H}\_2$. 
> 
> Then $\\{ \ket{e\_{i}} \otimes \ket{f\_{j}} \\}$ is a basis  
> for $\mathcal{G} = \\{ g: \mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C} \\;\\; | \\;\\; g \text{ is antilinear and continuous } \\; \\}$

> Consider two vectors $\ket{\psi\_1} \otimes \ket{\phi\_1}$ and $\ket{\psi\_2} \otimes \ket{\phi\_2}$ in $\mathcal{F}$.  
> 
> Then $\braket{\ket{\psi\_1} \otimes \ket{\phi\_1} \\; | \\; \ket{\psi\_2} \otimes \ket{\phi\_2} } = \braket{\psi\_1|\psi\_2}\_{\mathcal{H}\_1} \braket{\phi\_1|\phi\_2}\_{\mathcal{H}\_2}$ defines an inner product on $\mathcal{F}$.

> Let $g_1, g_2 \in \mathcal{G}$ where $g_1 = \sum_{i=1}^n c\_i ( \ket{e\_{1i}} \otimes \ket{f\_{1j}} )$ and  $g_2 = \sum_{j=1}^m d\_j (\ket{e\_{2i}} \otimes \ket{f\_{2j}}) $.
>
> Then $\braket{\\; g_1 | g_2 \\;} = \sum_{i = 1}^n \sum_{j=1}^m \overline{c_i} d_j \braket{e_{1i} \otimes f_{1j} | e_{2i} \otimes f_{2j}}$ defines an inner product on $\mathcal{G}$.

---
### Tensor Product Space

> The vector space $\mathcal{G} = \\{ g: \mathcal{H}\_1 \times \mathcal{H}\_2 | g \text{ is antilinear and continuous } \\}$ along with the inner product $\braket{\\; g\_1 | g\_2 \\;}$ defined as previously is a Hilbert space and is known as the **tensor product space** of $\mathcal{H}\_1$ and $\mathcal{H}\_2$.

> The tensor product space of $\mathcal{H}\_1$ and $\mathcal{H}\_2$ is denoted as $\mathcal{H}\_1 \otimes \mathcal{H}\_2$.

> The tensor product of two vectors satisfies the following properties:
> * $(a \ket\psi) \otimes \ket\phi = \ket\psi \otimes (a \ket\phi) = a (\ket\psi \otimes \ket\phi)$
> * $a (\ket\psi \otimes \ket\phi) + b (\ket\psi \otimes \ket\phi) = (a + b) (\ket\psi \otimes \ket\phi)$
> * $(\ket{\psi_1} + \ket{\psi_2}) \otimes \ket\phi = \ket{\psi_1} \otimes \ket\phi + \ket{\psi_2} \otimes \ket\phi$
> * $\ket\psi \otimes (\ket{\phi_1} + \ket{\phi_2}) = \ket\psi \otimes \ket{\phi_1} + \ket\psi \otimes \ket{\phi_2}$

---
### Qubits
##### Principle of Entanglement

> When we have two qubits being treated as a combined system, the state space of the combined system is the tensor product $\mathcal{H}\_1 \otimes \mathcal{H}\_2$ of the state spaces $\mathcal{H}\_1, \mathcal{H}\_2$ of the component qubit subsystems.
>
> Further, for a system of $n$ interacting qubits, the combined state space is the tensor product  
> $\mathcal{H}\_1 \otimes \mathcal{H}\_2 \otimes ... \otimes \mathcal{H}\_n$ of the state spaces of the $n$ qubits taken independently.

* Given an ONB $\\{ \ket{ e\_{i}} \\}\_{i = 1}^n$ for $\mathcal{H}\_1$ and an ONB $\\{ \ket{f_{j}} \\}\_{j = 1}^m$ for $\mathcal{H}\_2$, we have $\\{ \ket{e\_{i}} \otimes \ket{f\_{j}} \\}$ is a basis for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$. (Infact this is an ONB for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$)
* Suppose we take, in particular, the computational basis $\\{ \\; \ket{0_1}, \ket{1_1} \\; \\}$ for $\mathcal{H}\_1$ and the computational basis $\\{ \\; \ket{0_2}, \ket{1_2} \\; \\}$ for $\mathcal{H}\_2$.  
   Then $\\{ \\; \ket{0_1} \otimes \ket{0_2}, \ket{0_1} \otimes \ket{1_2}, \ket{1_1} \otimes \ket{0_2}, \ket{1_1} \otimes \ket{1_2} \\; \\}$ is an ONB for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$.  
  This basis is called the **computational basis** for $\mathcal{H}\_1 \otimes \mathcal{H}\_2$ and is also denoted as $\\{ \\; \ket{00}, \ket{01}, \ket{10}, \ket{11} \\; \\}$ or more simply, $\\{ \ket{0}, \ket{1}, \ket{2}, \ket{3} \\}$

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
* Consider $\ket\psi = \begin{bmatrix} a \\\\ b \end{bmatrix}$ and $\ket\phi = \begin{bmatrix} c \\\\ d \end{bmatrix}$. Then their tensor product is  
 $\ket\psi \otimes \ket\phi = \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \end{bmatrix} = \begin{bmatrix} a \begin{bmatrix} c \\\\ d \end{bmatrix} \\\\ b \begin{bmatrix} c \\\\ d \end{bmatrix} \end{bmatrix} = \begin{bmatrix} ac \\\\ ad \\\\ bc \\\\ bd \end{bmatrix}$
* $\ket{0} \otimes \ket{0} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix}$, $\ket{0} \otimes \ket{1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \\\\ 0 \end{bmatrix}$
*  $\ket{1} \otimes \ket{0} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 0 \\\\ 1 \\\\ 0 \end{bmatrix}$, $\ket{1} \otimes \ket{1} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 0 \\\\ 0 \\\\ 1 \end{bmatrix}$

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
> If we can write $\ket{\psi} = \ket{v\_1}\ket{v\_2}...\ket{v\_n} = \ket{v\_1 v\_2...v\_n}$, the state is said to be **seperable**.

* *Example:* The state $\ket{\psi} = \frac{1}{\sqrt{2}} (\ket{01} + \ket{11})$ of a $2$-qubit system is seperable since we can write $\ket{\psi} = \ket{+} \otimes \ket{1} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) \otimes \ket{1}$
* *Example:* The state $\ket{\psi^+} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11})$ of a $2$-qubit system is an entangled state. (In fact all Bell states are entangled states)

</section>
