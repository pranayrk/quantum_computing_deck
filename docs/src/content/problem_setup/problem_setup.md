<section data-markdown>
### Problem Setup

> Given a set of $N$ elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$ and a boolean function  
> $f: X \to \\{ 0,1 \\}$, find elements $x_i \in X$ such that $f(x_i) = 1$

* We are given an unstructured search problem
* We need to search for solutions from a finite set of possible solutions
* Consider an example for such a problem:
    * A set of $N$ coins is laid out on a table heads up
    * A few of those coins are flipped so that they are tails up
    * We need to find which coins have been flipped by only looking at one coin at a time

Note:
* Unstructured means we cannot use any clever tricks like binary search
* Lov Grover designed this algorithm to be used for searching databases, where we need to match a certain query
</section>
