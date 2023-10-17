<section data-markdown>
### Computational Basis of Multiple Qubits
* For $1$ qubit, the computational basis is $\\{ \ket{0}, \ket{1} \\}$
* For $2$ qubits, the computational basis is $\\{ \ket{0}, \ket{1}, \ket{2}, \ket{3} \\}$ where 
   * $\ket{0} = \ket{00} = \ket{0} \otimes \ket{0}$
   * $\ket{1} = \ket{01} = \ket{0} \otimes \ket{1}$
   * $\ket{2} = \ket{10} = \ket{1} \otimes \ket{0}$
   * $\ket{3} = \ket{11} = \ket{1} \otimes \ket{1}$
* For $n$ qubits, the computational basis is $\\{ \ket{0}, \ket{1}, ..., \ket{2^n - 1} \\}$ where
    * $\ket{0} = \ket{00...00} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}_{n\text{ times }}$
    * $\ket{1} = \ket{00...01} = \underbrace{\ket{0} \otimes \ket{0} \otimes ... \otimes \ket{0}}_{n-1\text{ times }} \otimes \ket{1}$
    * $\ket{2^n - 1} = \ket{11...11} = \underbrace{\ket{1} \otimes \ket{1} \otimes ... \otimes \ket{1}}_{n\text{ times }}$
</section>

