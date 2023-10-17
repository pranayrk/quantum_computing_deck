<section data-markdown>
### Grover's Algorithm
> Given a set of $N$ elements forming a set $X = \\{ x_1, x_2, ..., x_N \\}$ and a boolean function  
> $f: X \to \\{ 0,1 \\}$, find elements $x_i \in X$ such that $f(x_i) = 1$

* To make the solution space easier to work with, first label the values $x_i \in X$ directly as $i - 1$, so
$X = \\{0, 1, 2, ..., N - 1\\}$ and redefine $f$ so that $f(i - 1) = f(x_i)$ 
* Also consider (WLOG) that $N = 2^n$

</section>
