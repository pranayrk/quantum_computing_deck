<section data-markdown>
### Qubits
* The computers we use today rely on classical information theory, which are based on **bits** (binary digits) which can represents a $0$ or $1$ state.
* These computers (which will be referred to as **classical computers**) are equivalent to a Turing Machine in computational efficiency.
* On a quantum computer the **qubit** (quantum bit) is the basic unit of information.
---
### Qubits
* While bits take only two values, qubits can take on a continuum of values
* On a real-life quantum computer, a qubit can be implemented using a variety of quantum phenomena
* In labs, qubits have been implemented using photon polarization, electron spin, the ground/excited state of an atom in a cavity, and even defect centers in a diamond.

Note: 
* While there could be many such real-life realizations of qubits, we are not concerned with the specific implementation, as long as they follow certain rules
* We will abstract out these rules to form an abstract qubit that we can work with without knowing the specific details of the implementation
---
### Qubits
> A **qubit** is any quantum mechanical system which is associated with two-dimensional complex Hilbert space $\mathcal{H}_S$ (known as the **state space** and follows the below postulates:
> * Postulate of **Superposition**
> * Postulate of **Measurement**
> * Postulate of **Entanglement**
> * Postulate of **Transformation**
>
> A given state of the system is completely described by a  
> *unit vector* $\ket{\psi}$, which is called the **state vector** (or wave function) on the Hilbert Space 

---
### Qubits
> **Notation:** Observe above that we have written the vector   
> $\vec{\psi} \in \mathcal{H}$ as $\ket{\psi}$. This is the notation for a vector in Dirac's bra/ket notation, and is read **ket v**
* The standard basis (or **computational basis**) of the two dimensional complex vector space $\mathcal{H}$ are normally denoted as   
    $\ket{0} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}$ and $\ket{1} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}$

---
### Qubits
> **Postulate of Superposition**  
> With respect to the computational basis $\{ \ket{0}, \ket{1} \}$, the state of the qubit can be described as $\ket{\psi} = a \ket{0} + b \ket{1}$  
> $ = \begin{bmatrix} a \\\\ 0 \end{bmatrix} + \begin{bmatrix} 0 \\\\ b \end{bmatrix} = \begin{bmatrix} a \\\\ b \end{bmatrix} $ where $a, b \in \mathbb{C}$ and $a^2 + b^2 = 1$.

* Qubits are called **two-state** quantum systems. This does not mean that this system has only two states, but rather that all possible states exist as a linear combination of just two states

Note: 
The above follows from the Schrodinger Wave Equation which is a linear first order differential equation.

---
### Qubits
![Qubit](media/qubit_space.png)

</section>
