<section data-markdown>
### Quantum Gates
* **Quantum Gates** (or Quantum State Transformations) are the building blocks of complex computational systems based on qubits
* Quantum Gates are a mapping from the state space of a quantum system to itself.
* It can be shown that these transformations are valid only when the matrix representing the transformation is unitary. `TODO: Include Proof`
* A mapping $U: \mathcal{H} \to \mathcal{H}$ is unitary when $U^\dagger U = I$ where $U^\dagger$ is the complex conjugate transpose of $U$, known as the *Hermitian transpose*.
---
### Quantum Gates
> **Postulate of Transformation:**  
> Any state of the qubit can be transformed into any other state. Such transformations are carried out by means of processes that can be represented using unitary linear transformations

* All quantum state transformations are unitary, however that does not mean every unitary operator can be efficiently realized as a quantum transformation. `TODO: Include Proof`
* The fact that transformations are unitary imply that they are reversible. `TODO: Include Proof`
* The hadamard gates and the phase-shift gates are enough to perform any unitary operation on a single qubit. `TODO: Include Proof`
---
### Quantum Gates
* A common set of quantum gates are those which use the unitary Pauli matrices,   
   $\sigma_x = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}, \sigma_y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix}, \sigma_z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}$
* These quantum gates are known as **Pauli Gates**, and are the transformations $I, X=\sigma_x, Y = \sigma_y, Z = \sigma_z$.  
  These are quantum gates that act on a single qubit
* The **Hadamard Gate** is another common single-qubit gate where the transformation is represented by a unitary matrix $H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}$
---
### Quantum Gates
* The phase shift gate is a family of single-qubit gates that map the basis states as $\ket{0} \to \ket{0}$, $\ket{1} \to e^{i \phi} \ket{1}$ where $\phi$ is the phase shift with period $2 \pi$. It is represented by the unitary matrix $P(\phi) = \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \phi} \end{bmatrix}$
* It can be shown that every single qubit gate can be represented by some combination of Hadamard gates and Phase Shift gates. `TODO: Include Proof`

</section>
