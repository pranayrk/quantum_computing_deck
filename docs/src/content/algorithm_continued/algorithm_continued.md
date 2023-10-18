<section data-markdown>
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

* The matrix $D$ in the above algorithm is known as Grover's Diffusion operator
* The algorithm can be described as applying $G$ to $\ket{0}^n$:
    * Set the $n$-qubit register to $\ket{0}^n$
    * Apply the Hadamard Transform $H^{\otimes n}$ to get the average state  
        $\ket\psi = \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$
    * Repeat the following steps a certain number of times:
        * Apply the phase oracle $U_\pm$
        * Apply Grover's diffusion operator $D$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

* The diffusion operator $D$ in the above algorithm reflects any current state $\ket{\phi}$ of the $n$-qubit register about the axis of the average state $\ket{\psi} = \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$
* $D = 2 \ket\psi\bra\psi - I$
* $D$ can be realised as $D = H^{\otimes n} (2 \ket{0}\bra{0} - I) H^{\otimes n}$


</section>
