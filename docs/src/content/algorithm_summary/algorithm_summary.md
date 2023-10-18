<section data-markdown>
### Grover's Algorithm
> We are given a set of $N$ distinct elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$
> and a boolean function $f: X \to \\{ 0,1 \\}$ with $f(x) = 1$ for *exactly one* $x_i \in X$.  
> We are tasked with finding that unique $x_i$

* Consider without loss of generality that $N = 2^n$ for some $n \in \mathbb{N}$
* To make the solution space easier to work with, notice we can label the values $x_i \in X$ directly as $i - 1$, so
$X = \\{0, 1, 2, ..., N - 1\\}$ and also redefine $f$ so that $f(i - 1)$ will have the same value as the original $f(x_i)$ 
* Grover's algorithm relies on a black box which we wrap in an *oracle*

</section>
