<section data-markdown>
### Classical Approach
> We are given a set of $N$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x_i \in X$.  
> We are tasked with finding that unique $x_i$

* The only classical deterministic algorithm is to query the function $f$ with each value of $x_i \in X$ until we find the solution $x_i$ with $f(x_i) = 1$
* On average we will require $\frac{N}{2}$ queries to $f$ to determine the solution, and in the worst case we will need $N$ queries to $f$
* This means that the algorithm will have a time complexity of $O(N)$
Note: 
* When we know the number of solutions, say $t$ solutions among $N$ possibilities, a randomized algorithm will give a time complexity of $O(\frac{N}{t})$
</section>
