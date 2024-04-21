<section data-markdown>
### Foundations of Quantum Computing
##### Principle of Entanglement

> Multiple qubits interacting together results in the state space of the combined system being the *tensor product space* of the individual qubit state spaces

The tensor product $\ket{\psi} \otimes \ket{\phi} = \begin{bmatrix} a \\\\ b \end{bmatrix} \begin{bmatrix} c \\\\ d \end{bmatrix} = \begin{bmatrix} ac \\\\ ad \\\\ bc \\\\ bd \end{bmatrix}$

</section>
<section data-markdown>
### Foundations of Quantum Computing
##### Principle of Entanglement

> Two interacting qubits have a state space of dimension 4

The state space for two interacting qubits has the **computational basis** $\\{\\; \ket{0}, \ket{1}, \ket{2}, \ket{3} \\; \\}$ where 

 $\ket{0} = \ket{0} \otimes \ket{0} \qquad \ket{1} = \ket{0} \otimes \ket{1}$

 $\ket{2} = \ket{1} \otimes \ket{0} \qquad \ket{3} = \ket{1} \otimes \ket{1}$



</section>
<section data-markdown>
### Foundations of Quantum Computing
##### Principle of Entanglement

> $n$ interacting qubits have a state space of dimension $2^n$

The state space for two interacting qubits has the **computational basis** $\\{\\; \ket{0}, \ket{1}, \ket{2}, ..., \ket{2^n - 1} \\; \\}$ where 

 $\ket{0} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}_{n \text{ times}}$

 $\ket{2^n - 1} = \underbrace{\ket{1} \otimes \ket{1} \otimes ... \otimes \ket{1}}_{n \text{ times}}$

</section>

<section data-markdown>
### Foundations of Quantum Computing
##### Principle of Entanglement

> Most states in the tensor product space cannot be expressed as the tensor product of states in the individual qubits

For example:

The state $\ket{\phi^+} = \frac{1}{\sqrt{2}} ( \ket{0} + \ket{1} )$ cannot be expressed as a tensor product of two individual qubit states


</section>
