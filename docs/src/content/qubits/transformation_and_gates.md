<section data-markdown>
### Unitary Transformation
> A **unitary transformation** &nbsp; $U: \mathcal{H}\_1 \to \mathcal{H}\_2$ between two Hilbert space $\mathcal{H}\_1$ and $\mathcal{H}\_2$ is a isomorphism that preserves the inner product.  
> That is, for a unitary transformation $U$ on $\mathcal{H}$ we have $\braket{U \psi | U \phi } = \braket{\psi | \phi }$ for all $\ket{\psi}, \ket{\phi} \in \mathcal{H}$

> A matrix $U$ is called **unitary** if its conjugate transpose $U^\dagger$ is its inverse.   
> That is, a matrix is said to be unitary if &nbsp; $U U^\dagger = U^\dagger U = I$

> A unitary transformation $U$ is represented by a unitary matrix.
---
### Qubits
##### Principle of Transformation
>   In a quantum state space $\mathcal{H}$, every change of a quantum state over time that has not been caused by measurement is described by a unitary transformation.  
> If $\ket{\psi\_1}$ is the state at time $t\_1$ and $\ket{\psi\_2}$ is the state at time $t\_2 > t\_1$, then $\ket{\psi\_2}$ is described by  
> $\ket{\psi\_2} = U \ket{\psi\_1}$ where $U: \mathcal{H} \to \mathcal{H}$ is a unitary transformation.

* A **quantum gate** is a function $U: \mathcal{H} \to \mathcal{H}$ such that $f(\ket\psi) = \ket\phi$ where $\ket\psi, \ket\phi \in \mathcal{H}$ are valid quantum states in the state space $\mathcal{H}$ of $n$ interacting qubits.
* Any quantum gates is unitary and any unitary transformation is a valid quantum gate.
* A **quantum circuit** is a sequence of quantum gates and measurement operators applied to an $n$-qubit register initialized to some known quantum state.

---
# Quantum Gates
---
### Quantum Gates
> Any quantum gate is reversible.

> Any quantum gate has the same number of inputs and outputs

This implies that not all classical gates have a direct quantum analog.

> Consider the state space of a single qubit $\mathcal{H}$ and the orthonormal basis $\\{ \ket{e_1}, \ket{e_2} \\}$.
> The operator   
> $U: \mathcal{H} \to \mathcal{H}$ that takes $\ket{e_1} \to \ket{\psi}$ and $\ket{e_2} \to \ket{\phi}$ is represented  
> by the matrix $\ket{e_1}\bra{\psi} + \ket{e_2}\bra{\phi}$.

> *Deferred Measurement Principle*: Every quantum circuit is equivalent to a circuit in which all measurements are made after all other computations.
---
### Quantum Gates
##### Gates on a single qubit

> The **Pauli Gates** are the gates $\\{ \\; I, X, Y, Z  \\; \\}$ where  
> $I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix}$, $X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}$, 
> $Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix}$ and $Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}$

* The Pauli $X$ gate is also known as the **Quantum NOT Gate** since   
     $X \ket{0} = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \ket{1}$ and $X \ket{1} = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} = \ket{0}$   
    resembles the behaviour of the classical NOT Gate.
* However, most quantum gates do not have a classical analog in the same way.

---
### Quantum Gates
##### Gates on a single qubit

> The **Hadamard Gate** is the gate $H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix} = \ket{0}\bra{+} + \ket{1}\bra{-}$ 

* The Hadamard gate is important because it allows us to obtain a uniform superposition state, $\ket{+}$ from $\ket{0}$ or $\ket{-}$ from $\ket{1}$
*  $H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix} = \frac{1}{\sqrt{2}} \left ( \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} + \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} \right ) = \frac{1}{\sqrt{2}} ( X + Z ) $
* $H X H = Z$ and $HYH = -Y$.
---
### Quantum Gates
##### Gates on a single qubit
> The **Rotation Gates** are the gates $\\{ R\_x, R\_y, R\_z \\}$ where   
> $R\_x = \begin{bmatrix} \cos(\frac{\theta}{2}) & -i \sin(\frac{\theta}{2}) \\\\ -i \sin(\frac{\theta}{2}) & \cos(\frac{\theta}{2}) \end{bmatrix}$, 
> $R\_y = \begin{bmatrix} \cos \frac{\theta}{2} & - \sin \frac{\theta}{2} \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}$ and
> $R\_z = \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i\theta} \end{bmatrix}$

* $R\_x, R\_y, R\_z$ each define a rotation on the Bloch sphere of the state about the $x$-axis, $y$-axis, $z$-axis respectively by an angle of $\theta$.
* $R\_z = \ket{0}\bra{0} + e^{i\theta} \ket{1}\bra{1}$
* The Pauli matrix $Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi} \end{bmatrix}$ is a special case of the $R\_z$ matrix and represents a rotation of $\pi$ degrees about the $z$-axis.
---
### Quantum Gates
##### Gates on multiple qubits

> The **CNOT gate** (Controlled-NOT) is the gate defined by the matrix   
> $\text{CNOT} = \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix} = \ket{00} \bra{00} + \ket{01} \bra{01} + \ket{11} \bra{01} + \ket{10} \bra{11}$

* The CNOT gate acts on 2 qubits to apply a NOT gate on the second qubit if the first qubit is in the $\ket{1}$ state.
* $\text{CNOT} \ket{00} = \ket{00}$, $\text{CNOT} \ket{01} = \ket{01}$, $\text{CNOT} \ket{10} = \ket{11}$ and $\text{CNOT} \ket{11} = \ket{10}$.
* The CNOT gate is important because it allows us to obtain an entangled state from unentangled states. For example, it sends the unentangled state $\frac{1}{\sqrt{2}} ( \ket{00} + \ket{10} )$ to the entangled state $\frac{1}{\sqrt{2}} ( \ket{00} + \ket{11} )$.

---
### Quantum Gates
##### Gates on multiple qubits

> Given a register of $n$ qubits, the **Hadamard Transform** $H^{\otimes n}$ is the transformation that applies the Hadamard gate $H = \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}$ on each of the $n$ qubits.  
> $H^{\otimes n} = \underbrace{H \otimes H \otimes ... \otimes H}\_{n \text{ times }}$

* Consider $H\_0 = 1$.   
    Then we can recursively define the Hadamard transform as   
    $H^{\otimes n} = \frac{1}{\sqrt{2}} \begin{bmatrix} H^{\otimes n - 1} & H^{\otimes n - 1} \\\\ H^{\otimes n - 1} & -H^{\otimes n - 1} \end{bmatrix}$ for all $n > 0$.
* For $n > 1$, we can also recursively define the Hadamard transform as   
    $H^{\otimes n} = H \otimes H^{\otimes n - 1}$

---

### Quantum Gates
##### Gates on multiple qubits

> Consider an $n$-qubit register with each qubit set to $\ket{0}$.   
> Then $H^{\otimes n} \ket{\underbrace{00...0}\_{n \text{ times }}} = \displaystyle\frac{1}{2^{n/2}} \sum_{j=0}^{2^n -1} \ket{j}$

Consider the Hadamard transform applied to an $n$-qubit register, each qubit set to $\ket{0}$,

$H^{\otimes n} \ket{0}^n  = \underbrace{(H \ket{0}) \otimes (H \ket{0}) \otimes (H \ket{0}) \otimes ... \otimes (H \ket{0})}_{n\text{ times }}$

$= \underbrace{\frac{1}{2^{n/2}} (\ket{0} + \ket{1}) \otimes (\ket{0} + \ket{1}) \otimes (\ket{0} + \ket{1}) ... \otimes (\ket{0} + \ket{1})}\_{n \text{ times }} = \displaystyle\frac{1}{2^{n/2}} \sum_{j=0}^{2^n -1} \ket{j}$
</section>


</section>

