<section data-markdown>
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

* The steps in the algorithm are:
    * Set the $n$-qubit register to $\ket{0}^n$
    * Apply the Hadamard Transform $H^{\otimes n}$
    * Repeat the following steps a certain number of times:
        * Apply the phase oracle $U_\pm$
        * Apply Grover's diffusion operator $D$
    * Measure the state of the $n$-qubit register

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

Let $k \in \\{ 0, 1 \\}^n$ be the required solution.

We will require the $n$-qubit register to be very close to the state $\ket{k} \in \ket{0}, ..., \ket{2^n-1}$.

Applying the Hadamard gate on $\ket{0}^n$, we get the register in the average state  
 $\ket\psi = H^{\otimes n} \ket{0}^n = \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$

Applying $U_\pm$ on this average state $\ket\psi$, we get  
 $U_\pm(\ket\psi) = U_\pm (\frac{1}{2^{n/2}} \sum_{j=0}^{2^n - 1} \ket{j}) $ 

$ = \frac{1}{2^{n/2}} \sum_{j=0}^{2^n-1} U_\pm (\ket{j}) = - \frac{1}{2^{n/2}} \ket{k} + \frac{1}{2^{n/2}} \sum_{j=0, j \neq k}^{2^n-1} \ket{j}$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

* Grover's diffusion operator $D$ in the above algorithm is a gate which reflects any current state $\ket{\phi}$ of the $n$-qubit register about the axis of the average state   
   $\ket{\psi} = \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$
* We can represent the operation of $D$ as $D = 2 \ket\psi\bra\psi - I$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

The mean amplitude of the state $U_\pm(\ket\psi)$ before applying $D$ is 

$\displaystyle \frac{\frac{-1}{2^{n/2}} + \frac{1}{2^{n/2}} (2^n -1) }{2^n} = \displaystyle \frac{(2^n - 2) \frac{1}{2^{n/2}}}{2^n} \approx \frac{2^n}{2^n} \frac{1}{2^{n/2}} = \frac{1}{2^{n/2}}$ for large $n$.

Therefore after reflection about $\ket\psi$, the amplitudes of most entries $\ket{j}$ where $j \neq k$ stays roughly the same.

However, for the solution $k \in \\{0,1 \\}^n$, the entry of $\ket{k}$ will be reflected to an amplitude of $\displaystyle\frac{3}{2^{n/2}}$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

$D (U_\pm \ket\psi) = D ( - \frac{1}{2^{n/2}} \ket{k} + \frac{1}{2^{n/2}} \sum_{j=0, j \neq k}^{2^n-1} \ket{j} )$



</section>
