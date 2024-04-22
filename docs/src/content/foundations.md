<section data-markdown>
# Fundamentals of Quantum Computing
</section>
<section data-markdown>
### Fundamentals of Quantum Computing

* The **qubit** forms the foundational unit of computing
* A qubit can be represented as a mathematical model with the following principles:
    * Principle of Superposition
    * Principle of Transformation
    * Principle of Measurement
    * Principle of Entanglement
</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Superposition
> The state of every qubit can be represented by a unit vector in a 2-dimensional complex Hilbert space

The state is normally described with respect to the **computational basis** $\\{ \\; \ket{0}, \ket{1} \\; \\} $
where 

$\ket{0} = 1 + 0 i = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}$ and $\ket{1} = 0 + 1 i = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}$
</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Transformation
> Any change in the state of a qubit can be described by the action of a unitary transformation

A unitary transformation is a linear isomorphism that preserves the inner product.

This can be represented by a unitary matrix $U$ where $$U U^\dagger = U^\dagger U = I$$

</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Entanglement

> Multiple qubits interacting together results in the state space of the combined system being the *tensor product space* of the individual qubit state spaces

The tensor product $\ket{\psi} \otimes \ket{\phi} = \begin{bmatrix} a \\\\ b \end{bmatrix} \begin{bmatrix} c \\\\ d \end{bmatrix} = \begin{bmatrix} ac \\\\ ad \\\\ bc \\\\ bd \end{bmatrix}$

</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Entanglement

> Two interacting qubits have a state space of dimension 4

The state space for two interacting qubits has the **computational basis** $\\{\\; \ket{0}, \ket{1}, \ket{2}, \ket{3} \\; \\}$ where 

 $\ket{0} = \ket{0} \otimes \ket{0} \qquad \ket{1} = \ket{0} \otimes \ket{1}$

 $\ket{2} = \ket{1} \otimes \ket{0} \qquad \ket{3} = \ket{1} \otimes \ket{1}$



</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Entanglement

> $n$ interacting qubits have a state space of dimension $2^n$

The state space for two interacting qubits has the **computational basis** $\\{\\; \ket{0}, \ket{1}, \ket{2}, ..., \ket{2^n - 1} \\; \\}$ where 

 $\ket{0} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}_{n \text{ times}}$

 $\ket{2^n - 1} = \underbrace{\ket{1} \otimes \ket{1} \otimes ... \otimes \ket{1}}_{n \text{ times}}$

</section>

<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Entanglement

> Most states in the tensor product space cannot be expressed as the tensor product of states in the individual qubits

For example:

The state $\ket{\phi^+} = \frac{1}{\sqrt{2}} ( \ket{0} + \ket{1} )$ cannot be expressed as a tensor product of two individual qubit states


</section>
<section data-markdown>
### Fundamentals of Quantum Computing
##### Principle of Measurement
Consider the qubit in state $\ket{\psi} = a \ket{0} + b \ket{1}$ and a measurement device calibrated to the computational basis

> The action of measurement causes the state of the qubit to collapse into either $\ket{0}$ or $\ket{1}$ which will be output of measurement

The probability of measuring $\ket{0}$ is $|a|^2$ and the probability of measuring $\ket{1}$ is $|b|^2$

</section>

