<section data-markdown>
### Classical Approach
> Given a set of $N$ elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$ and a boolean function  
> $f: X \to \\{ 0,1 \\}$, find elements $x_i \in X$ such that $f(x_i) = 1$

* Consider the case where there is only $1$ possible solution
* The only classical deterministic algorithm is to query the function $f$ with each value of $x_i \in X$ until we find a solution
* On average we will require $\frac{N}{2}$ queries to $f$ to determine the solution, and in the worst case we will need $N$ queries to $f$
* This means that the algorithm will have a time complexity of $O(N)$
---
### Classical Approach
> Given a set of $N$ elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$ and a boolean function  
> $f: X \to \\{ 0,1 \\}$, find elements $x_i \in X$ such that $f(x_i) = 1$

* When the number of solutions is not known, any deterministic algorithm will need to query all $N$ possibilities to check if each one is a solution
* We will need $N$ queries to $f$ in the average and worst case 
* This means that the time complexity for any classical deterministic algorithm is $O(N)$

Note: 
* When we know the number of solutions, say $t$ solutions among $N$ possibilities, a randomized algorithm will give a time complexity of $O(\frac{N}{t})$
</section>
