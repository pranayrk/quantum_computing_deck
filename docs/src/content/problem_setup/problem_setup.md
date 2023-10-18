<section data-markdown>
### Problem Setup

> We are given a set of $N$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$  
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x_i \in X$.  
> We are tasked with finding that unique $x_i$

* The problem above represents an unstructured search problem
* We need to search for the solution from a finite set of possible solutions
* Consider an example for such a problem:
    * A set of $N$ coins is laid out on a table heads up
    * One of these coins is flipped so that it is tails up
    * We need to find which coin has been flipped by checking only one coin at a time

Note:
* Unstructured means we cannot use any clever tricks like binary search
* Lov Grover designed this algorithm to be used for searching databases, where we need to match a certain query
</section>
