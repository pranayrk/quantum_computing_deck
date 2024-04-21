<section data-markdown>
### Simon's Algorithm


Let  $\oplus$ represent addition modulo 2

> Given a 2 to 1 function $f$ satisfying the property that there exists a fixed $a \in \\{ 0, 1 \\}^n$ such that $f(x) = f(x \oplus a)$ for all $x \in \\{ 0,1 \\}^n$.  
> Find the fixed string $a$. 

* Classical randomized algorithms are known to have a worst-case time complexity of $O(2^{n/2})$
* Simon's algorithm solves the problem statement with a time complexity of $O(n)$

Note:
served as the inspiration for Shor's algorithm
1994
</section>
