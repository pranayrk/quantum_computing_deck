<section data-markdown>
### Amplitude Amplification Algorithm
> We are given a set of $N = 2^n$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *some* $x_i \in X$.   
> Given each $x_i$ corresponds to a basis element $\ket{i-1}$ of a quantum state space with basis $\\{\ket{0},\ket{1}, ...,\ket{2^n - 1} \\}$, we want to bring the state space close to a uniform superposition of the basis vectors for which the corresponding $x_i$ satisfies $f(x_i) = 1$

* Generalization of Grover's original algorithm where there are multiple possible solutions in the solution space
* More precisely, Grover's original algorithm belongs to what we now call the class of amplitude amplification algorithms
* This finds use as a subroutine in many other quantum algorithms either to prepare the input as an equal superposition of certain basis states or to emphasize the effect of certain basis states
---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\psi}$

* $U_\pm \ket{x} = \begin{cases} \ket{x} & \text{ if } f(x) \text{ is not a solution } \\\\ -\ket{x} & \text{ if } f(x) \text{ is a solution } \end{cases} = (-1)^{f(x)} \ket{x}$
* $U_\pm$ puts a negative sign for all $\ket{i}$ which are solutions and none of $\ket{i}$ which are not solutions
* $D = 2 \ket\psi \bra\psi - I$ and is normally written as $H^{\otimes n} (2 \ket{0}\bra{0} - I) H^{\otimes n}$ in most sources

---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$


* We call the equal superposition of basis vectors in $\mathscr{B}'$ as the good state $\ket{G}$ and the superposition of vectors in $\mathscr{B} - \mathscr{B}'$ as the bad state $\ket{B}$.
* The analysis of the amplitude amplification algorithm can be done fully in the 2-d vector space spanned by the basis $\\{ \ket{G}, \ket{B} \\}$.
* Clearly, $\ket{G}$ and $\ket{B}$ are orthogonal, i.e. $\ket{B}$ is an angle $\displaystyle \frac{\pi}{2}$ away from $\ket{G}$ in this vector space

---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$


Let there be $M$ solutions out out $N = 2^n$ possibilities. 

Let those $M$ solutions be known as *marked states*.

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
$\implies \theta = \sin^{-1}(\frac{\sqrt{M}}{\sqrt{N}})$

For $M \ll N$, $\theta \approx \frac{\sqrt{M}}{\sqrt{N}}$

The phase oracle $U_\pm$ can be thought of as a reflection of the state of the register around $\ket{B}$

$D$ is a reflection about the uniformly distributed state $\ket\psi$. 

So for each iteration, we have two reflections in the $\ket{G}$ - $\ket{B}$ plane

---
### Amplitude Amplification Algorithm
![amplitude](media/amplitude.png)


---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$


In each iteration, the state of the register will be rotated towards $\ket{G}$ by an angle of $2 \theta \approx 2 \frac{\sqrt{M}}{\sqrt{N}}$. 

Since the register was initially set at an angle $\theta$ from $\ket{B}$, the state of the register after $k$ iterations will be at an angle $(2k + 1) \theta$ away from $\ket{B}$

If the number of solutions are small, i.e. $M \ll N$, then the starting state will be very close to $\ket{B}$, i.e. we will need to rotate the state by almost an angle of $\frac{\pi}{2}$ to reach $\ket{G}$

So performing $k$ iterations to get to $\displaystyle \frac{\pi}{2}$ away from $\ket{B}$,  
$(2k+1)\theta = \displaystyle \frac{\pi}{2} \implies$ we will require $k = \displaystyle  \frac{1}{2} \left (   \frac{\pi}{2 \theta} - 1 \right ) \approx \frac{\pi}{4}  \frac{\sqrt{N}}{\sqrt{M}}$ iterations.


---
### Amplitude Amplification Algorithm
> Given a quantum state space of an $n$-qubit register with basis $\mathscr{B} = \\{\ket{0}, \ket{1}, ..., \ket{2^n-1} \\}$, and a subbasis $\mathscr{B}'$. 
> To bring the state of the register close to a superposition of basis vectors in $\mathscr{B}'$,
> we apply the algorithm $G = \underbrace{D \cdot U_\pm \cdot....U_\pm \cdot D \cdot U_\pm \cdot D \cdot U_\pm}_{\text{ applied a certain number of times }}$ to any initial state $\ket{\phi}$

Therefore around $\displaystyle  \frac{1}{2} \left (   \frac{\pi}{2 \theta} - 1 \right )$ (rounded up or down) iterations are required. This is the complexity of the Amplitude Amplification algorithm when the number of solutions $M$ is known.

Some particular cases $M$ lead to interesting results. Consider the case when $M$ is exactly $25%$ of the total number of possible solutions $N$, i.e. $M = \displaystyle \frac{1}{4} N$. Therefore $\theta \approx \displaystyle \frac{\sqrt{M}}{\sqrt{N}} = \frac{\sqrt{\frac{1}{4}N}}{\sqrt{N}} = \frac{1}{2}$

Then to reach the good state $\ket{G}$, we will need $\displaystyle  \frac{1}{2} \left (   \frac{\pi}{2 \theta} - 1 \right ) \approx 1.07$ iterations, i.e we reach close to the good state in one call to the black box.

</section>

