<section data-markdown>
# Qubits 
---
### Qubits
* The computers we commonly use today are based on **bits**
* A **bit** can take on either a $0$ or a $1$ state
* Their behaviour is modelled by classical information theory
* Classical information theory tells us these **classical computers** are equivalent to an abstract Turing Machine in computational efficiency
---
### Qubits
* On a quantum computer the **qubit** (quantum bit) is the basic unit of information.
* While bits take only two values, the state of a qubit can take on a continuum of values
* Along with some other quantum induced phenomena, this lets quantum computers have a computational efficiency more than a Turing Machine in some cases
* In labs, qubits have been implemented using photon polarization, electron spin and even defect centers in a diamond.
---
### Hilbert Space
> A complex **Hilbert space** $\mathcal{H}$ is a vector space over $\mathbb{C}$ with a positive definite inner product  
$\braket{} : \mathcal{H} \times \mathcal{H} \to \mathbb{C}$ defined as $(\vec\psi,\vec\phi) \to \braket{\vec\psi,\vec\phi}$ such that: 
> * conjugate symmetric: $\braket{\vec\psi,\vec\phi} = \overline{\braket{\vec\phi,\vec\psi}}$
> * positive definite: $\braket{\vec\psi,\vec\psi} \geq 0$ and $\braket{\vec\psi,\vec\psi} = 0 \iff \vec\psi = 0$
> * conjugate linear in first argument: $\braket{a \vec\phi_1 + b \vec\phi_2, \psi} = \overline{a} \braket{\vec\phi_1, \vec\psi} + \overline{b} \braket{\vec\phi_2, \vec\psi}$
> * linear in second argument: $\braket{\vec\psi, a \vec\phi_1 + b \phi_2} = a \braket{\vec\psi,\vec\phi_1} + b \braket{\vec\psi,\vec\phi_2}$  
> 
> and this inner product induces a norm $||.|| : \mathcal{H} \to \mathbb{R}$ defined as $\psi \to \sqrt{\braket{\vec\psi,\vec\psi}}$ in which $\mathcal{H}$ is complete.
---
### Qubits
>  A **qubit** is any quantum mechanical system whose state can be completely described by a unit vector   
> in a $2$-dimensional complex Hilbert space $\mathcal{H}$ and which follows these axioms:
> * Principle of Superposition
> * Principle of Entanglement
> * Principle of Measurement
> * Principle of Transformation
> 
> The Hilbert space $\mathcal{H}$ is known as the **state space** and is equipped with the inner product $\braket{}$ which is defined as $\braket{\vec\psi, \vec\phi} = \overline{a} c + \overline{b} d = \begin{bmatrix} \overline{a} & \overline{b} \end{bmatrix} \begin{bmatrix} c \\\\ d \end{bmatrix}$ &nbsp; where &nbsp;  $\vec\psi = \begin{bmatrix} a \\\\ b\end{bmatrix}, \vec\phi = \begin{bmatrix} c \\\\ d \end{bmatrix} \in \mathcal{H}$. 
>
> Any unit vector of $\mathcal{H}$ is called a **state vector**.

---
### Dirac Bra/Ket Notation
> We will write any qubit state vector $\vec{\psi} \in \mathcal{H}$ as $\ket{\psi}$ and is read as **ket psi**  

> The notation $\bra{\psi}$ represents conjugate transpose of $\ket\psi$  
> $\bra\psi = \ket{\psi}^\dagger = \begin{bmatrix} \overline{a} & \overline{b} \end{bmatrix}$ and is read as **bra psi**

This means the inner product $\braket{\vec\psi,\vec\phi}$ will be $\bra{\psi}\ket\phi$.

> The inner product will be denoted as $\braket{\psi|\phi} = \overline{a} c + \overline{b} d$  
>  for any $\ket{\psi} = \begin{bmatrix} a \\\\ b\end{bmatrix}, \ket{\phi} = \begin{bmatrix} c \\\\ d \end{bmatrix} \in \mathcal{H}$ and is read as **braket**

The set of all bra vectors forms the dual space of $\mathcal{H}$.
</section>
