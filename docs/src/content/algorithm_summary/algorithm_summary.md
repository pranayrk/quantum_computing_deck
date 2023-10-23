<section data-markdown>
### Grover's Algorithm
> We are given a set of $N$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x_i \in X$.  
> We are tasked with finding that unique $x_i$

* Consider without loss of generality that $N = 2^n$ for some $n \in \mathbb{N}$
* Let each $x_i \in \\{ x_1, x_2, ..., x_N \\}$ correspond to the basis vector $\ket{i-1}$ in a quantum state space with basis vectors $\\{\ket{0}, \ket{1}, ..., \ket{N-1} \\}$
* Since $N = 2^n$, we will need to use an $n$-qubit register to achieve a suitable corresponding basis.
* Grover's algorithm relies on a black box circuit which tells us whether a particular $x_i$ is a solution
* We wrap this black box in a *quantum oracle* which takes a quantum state as input and can tell us whether a given basis vector $\ket{i}$ is a solution.

</section>
