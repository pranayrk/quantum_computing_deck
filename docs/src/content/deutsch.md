<section data-markdown>
# Quantum Algorithms
</section>
<section data-markdown>
### Deutsch-Jozsa Algorithm

A function $f: \mathbb{Z}_n \to \\{ 0, 1 \\}$ is said to be **constant** when $f(x) = f(y)$ for all $x$ and $y$ in $\mathbb{Z}_n$. 

A function $f: \mathbb{Z}_n \to \\{ 0, 1 \\}$ is said to be **balanced** if an equal number of input values to the function return $0$ and $1$.
    
> Given a funtion $f: \mathbb{Z}_n \to \\{0,1\\}$, determine whether the function is constant or balanced.

* Classical algorithms can solve this problem in $O(n)$
* Deutsch-Jozsa algorithm can solve this problem in $O(1)$

Note:
proposed by David Deutsch and Richard Jozsa in 1992

Although of little practical use, it is one of the first examples of a quantum algorithm that is exponentially faster than any possible deterministic classical algorithm.
</section>
