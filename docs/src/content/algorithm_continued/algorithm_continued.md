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

Applying the Hadamard gate on $\ket{0}^n$, we get the register in the *average state*  
$\ket\psi = H^{\otimes n} \ket{0}^n = \displaystyle \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$

Applying $U_\pm$ on this average state $\ket\psi$, we get $U_\pm(\ket\psi) = U_\pm (\frac{1}{2^{n/2}} \sum_{j=0}^{2^n - 1} \ket{j}) $ 

$ = \frac{1}{2^{n/2}} \sum_{j=0}^{2^n-1} U_\pm (\ket{j}) = - \frac{1}{2^{n/2}} \ket{k} + \frac{1}{2^{n/2}} \sum_{j=0, j \neq k}^{2^n-1} \ket{j}$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

![after_upm](media/after_upm.png)

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

* Grover's diffusion operator $D$ in the above algorithm is a gate which reflects any state $\ket{\phi}$ about the axis of the average state $\ket{\psi} = \frac{1}{2^{n/2}} \sum_{i=0}^{2^n-1}\ket{j}$
* We can represent the operation of $D$ as $D = 2 \ket\psi\bra\psi - I$
* [Grover's paper, Page 5](https://arxiv.org/pdf/quant-ph/9605043.pdf) has details on how to construct $D$ from Hadamard Gates and Rotation Gates

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

The mean amplitude of the state $U_\pm(\ket\psi)$ before applying $D$ is 

$\displaystyle \frac{\frac{-1}{2^{n/2}} + \frac{1}{2^{n/2}} (2^n -1) }{2^n} = \displaystyle \frac{(2^n - 2) \frac{1}{2^{n/2}}}{2^n} \approx \frac{2^n}{2^n} \frac{1}{2^{n/2}} = \frac{1}{2^{n/2}} = \frac{1}{\sqrt{N}}$

Therefore after reflection about $\ket\psi$, the amplitudes of most entries $\ket{j}$ where $j \neq k$ are slightly   
reduced but roughly the same.

However, for the solution $k \in \\{0,1 \\}^n$, the entry of $\ket{k}$ will be reflected to an  
 amplitude of $\displaystyle\frac{3}{2^{n/2}} = \frac{3}{\sqrt{N}}$

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  

![after_diffusion](media/after_diffusion.png)


---

### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  


After one application of $D U_\pm$, the amplitude of the solution component $\ket{k}$ will be $\displaystyle \frac{3}{\sqrt{N}}$   
and the amplitude of the non-solution components will be sligtly less than $\displaystyle\frac{1}{\sqrt{N}}$

If we apply $D U_\pm$ a second time, the amplitude of the solution component $\ket{k}$ will be $\displaystyle \frac{5}{\sqrt{N}}$ and the amplitude of the non-solutions will be even lower.

So $p$ applications of $D U_\pm$ will result in the solution component having an amplitude of $\displaystyle\frac{2p + 1}{\sqrt{N}}$ and the non-solution components will reduce in amplitude with each application.

---
### Grover's Algorithm
> The circuit for Grovers algorithm $\boxed{G}$ performs the operation given by the operator  
> $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }} \cdot H^{\otimes n}$  


Suppose we need to make the amplitude of the solution greater than a constant $A$.  
We proceed to apply $D U_\pm$ a total of $\displaystyle \frac{A\sqrt{N}}{2}$ times (rounded up). 

We will get the solution component having an amplitude of $\displaystyle \frac{2 \frac{A\sqrt{N}}{2} + 1}{\sqrt{N}} > A$ and the non-solution components will have very low amplitude for large $N$.

Since we repeat $D U_\pm$ a total of $\displaystyle \frac{A\sqrt{N}}{2}$ (rounded up), we see that Grover's algorithm has a time-complexity of $\frac{A}{2} \sqrt{N} \sim O(\sqrt{N})$



</section>
