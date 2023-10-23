<section data-markdown>
### Amplitude Amplification Algorithm
> We are given a set of $N = 2^n$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *some* $x_i \in X$.   
> Given each $x_i$ corresponds to a basis element $\ket{i-1}$ of a quantum state space with basis $\\{\ket{0},\ket{1}, ...,\ket{N} \\}$, we want to bring the state space close to a uniform superposition of the basis vectors for which the corresponding $x_i$ satisfies $f(x_i) = 1$

* Generalization of Grover's original algorithm where there are multiple possible solutions in the solution space
* More precisely, Grover's original algorithm belongs to what we now call the class of amplitude amplification algorithms
* This finds use as a subroutine in many other quantum algorithms either to prepare the input as an equal superposition of certain basis states or to emphasize the effect of certain basis states
---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\psi}$

* $U_\pm \ket{x} = \begin{cases} \ket{x} & \text{ if } f(x) \text{ is not a solution } \\\\ -\ket{x} & \text{ if } f(x) \text{ is a solution } \end{cases} = (-1)^{f(x)} \ket{x}$
* $U_\pm$ puts a negative sign for all $\ket{i}$ in the good state and none of $\ket{i}$ in the bad state
* $D = 2 \ket\psi \bra\psi - I$ and is normally written as $H^{\otimes n} (2 \ket{0}\bra{0} - I) H^{\otimes n}$ in most sources

---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$


* We call the equal superposition of basis vectors in $\mathscr{B}'$ as the good state $\ket{G}$ and the superposition of vectors in $\mathscr{B} - \mathscr{B}'$ as the bad state $\ket{B}$.
* Clearly, $\ket{G}$ and $\ket{B}$ are orthonormal
* The analysis of the amplitude amplification algorithm can be done purely in a 2-d vector space, i.e. the vector space spanned by the basis $\\{ \ket{G}, \ket{B} \\}$.

---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$

Let there be $M$ solutions out out $N = 2^n$ possibilities. Let those $M$ solutions be known as *marked states*.

Then $\ket{G} = \displaystyle \frac{1}{\sqrt{M}} \sum_{i \text{ is marked }} \ket{i}$ and $\ket{B} = \displaystyle \frac{1}{\sqrt{N-M}} \sum_{i \text{ is unmarked }} \ket{i}$

Then a state $\ket\phi$ can be uniquely decomposed as $\ket\phi = \sin\theta \ket{G} + \cos\theta \ket{B}$

Assume for simplicity that $\ket{\phi} = \ket{\psi}$ is the uniform superposition state. For analysis on a general state $\ket{\phi}$ check the [Wikipedia article, Algorithm section](https://en.wikipedia.org/wiki/Amplitude_amplification).

---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$

$\ket\psi = \sin\theta \ket{G} + \cos\theta \ket{B}$ and  
$\ket\psi = \displaystyle \frac{\sqrt{M}}{\sqrt{N}} \ket{G} + \frac{\sqrt{N - M}}{\sqrt{N}} \ket{B}$
$\implies \theta = \arcsin(\frac{\sqrt{M}}{\sqrt{N}})$

For $M \ll N$, $\theta \approx \frac{\sqrt{M}}{\sqrt{N}}$

The phase oracle $U_\pm$ can be thought of as a reflection of the state of the register about $\ket{B}$.
$D$ is a reflection about the uniformly distributed state.

</section>
