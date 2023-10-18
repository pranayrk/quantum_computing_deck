<section data-markdown>
### Oracle
> We are given a set of $N$ distinct elements forming a set $X = \\{ 0, 1, ..., 2^n-1 \\}$ and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x \in X$

* Consider we have access to a classical circuit $\boxed{O_c}$ which takes input of $x \in X$ as a binary string, i.e. $x \in \\{0,1\\}^n$, and outputs $f(x)$</li>
* Since we have possible values of $x$ from $0$ to $2^n-1$, we will need an $n$-bit binary string as input to $\boxed{O_c}$</li>
* Using $\boxed{O_c}$ directly in Grover's algorithm by swapping in $\ket{x}$ will not work since is not a valid quantum gate</li>

</section>
<section data-markdown>
### Oracle
> We are given a set of $N$ distinct elements forming a set $X = \\{ 0, 1, ..., 2^n-1 \\}$ and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x \in X$

* One way of rectifying this is by constructing a bit-oracle circuit $\boxed{U_f}$ in such a way that it has equal number of inputs and outputs. Also the circuit should be invertible.
* We define $\boxed{U_f}$ as the circuit such that $U_f(\ket{x}\ket{y}) = \ket{x}\ket{y \oplus f(x)}$ where $\oplus$ denotes addition modulo 2 and $\ket{y}$ is an extra ancilliary qubit given to hold the output.
* Note that we are not concerned with the exact implementation of $\boxed{U_f}$ and leave it as a black-box which we expect is provided to us

Note: 
* To show $U_f$ is unitary and reversible, check https://people.vcu.edu/~sgharibian/courses/CMSC491/notes/Lecture%206%20-%20Deutsch%27s%20algorithm.pdf 
</section>
<section data-markdown>
### Oracle
* The circuit for $\boxed{U_f}$ has extra output qubit $\ket{y}$ to handle, this can be simplified to an $n$-qubit circuit.
* The approach for this is to construct a phase-oracle $\boxed{U_\pm}$ such that $U_\pm \ket{x} = \begin{cases} \ket{x} & \text{ if } f(x) = 0 \\\\ -\ket{x} & \text{ if } f(x) = 1 \end{cases} = (-1)^{f(x)} \ket{x}$
---
### Oracle
> Given a bit-oracle circuit $\boxed{U_f}$ we can construct the phase-oracle $\boxed{U_\pm}$

Suppose that we are given a bit-oracle circuit $\boxed{U_f}$ and the ancilliary $\ket{y}$ is set to $\ket{-}$.

Then the state of the input is $\ket{x}\otimes \ket{-} = \frac{1}{\sqrt{2}} (\ket{x0} - \ket{x1})$

*First case, $f(x) = 0$:* $U_f( \ket{x} \otimes \ket{-})$ leaves the state unchanged.

*Second case, $f(x) = 1$:* $U_f(\ket{x} \otimes \ket{-}) =  \ket{x} \otimes \frac{1}{\sqrt{2}} (\ket{0 \oplus 1} - \ket{1 \oplus 1})$

$ = \ket{x} \otimes \frac{1}{\sqrt{2}} (\ket{1} - \ket{0}) = \frac{1}{\sqrt{2}} (\ket{x1} - \ket{x0})$

$ \implies U_f(\ket{x} \otimes \ket{-}) = (-1)^{f(x)} (\ket{x} \otimes \ket{-})$ which is the action of the phase-oracle
</section>
