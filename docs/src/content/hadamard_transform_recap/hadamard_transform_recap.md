<section data-markdown>
### Hadamard Gate
> The **Hadamard gate** $H$ acts on a single qubit and is represented by the Hadamard matrix 
$H = \displaystyle\frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 & -1 \end{bmatrix}$

* The Hadamard gate acts on $\ket{0}, \ket{1}$ as:
    * $H\ket{0} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) = \ket{+}$ 
    * $H\ket{1} = \frac{1}{\sqrt{2}} (\ket{0} - \ket{1}) = \ket{-}$
* The Hadamard gate is self inverse, $H H = I$

Note:
* Creates an equal superposition of the basis states
* The conjugate transponse of $H$ is $H$ itself, so to check it is unitary, we only need to check $HH = I$
* $H\ket{+} = \ket{0}$ and $H\ket{-} = \ket{1}$
</section>
<section data-markdown>
### Hadamard Transform
> The **Hadamard transform** denoted $H^{\otimes n}$ represents the application of the Hadamard gate to each qubit of an $n$-qubit register in parallel.

Consider the Hadamard tranform applied to an $n$-qubit register, each qubit set to $\ket{0}$,

$H^{\otimes n} \ket{0}^n  = \underbrace{(H \ket{0}) \otimes (H \ket{0}) \otimes (H \ket{0}) \otimes ... \otimes (H \ket{0})}_{n\text{ times }}$

$= \underbrace{\frac{1}{2^{n/2}} (\ket{0} + \ket{1}) \otimes (\ket{0} + \ket{1}) \otimes (\ket{0} + \ket{1}) ... \otimes (\ket{0} + \ket{1})}_{n \text{ times }}$ 

$= \displaystyle\frac{1}{2^{n/2}} \sum_{j=0}^{2^n -1} \ket{j} \text{ where $\ket{j}$ is the bitstring that represents $j$ in binary}$
</section>
