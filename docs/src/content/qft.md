<section data-markdown>
### Quantum Fourier Transform
Let $\omega = \exp\left(  \frac{ 2\pi i}{N} \right)$

>  The **Discrete Fourier Transform (DFT)** is a function $F\_N: \mathbb{C}^N \to \mathbb{C}^N$ that transforms a vector of complex numbers $\\begin{bmatrix} x\_0  & x\_1 & ... & x\_{N-1} \\end{bmatrix}^T$ into another vector of complex numbers $\begin{bmatrix} y\_0  & y\_1 & ... & y\_{N-1} \end{bmatrix}^T$ such that $$y\_k = \frac{1}{\sqrt{N}} \sum_{j=0}^{N-1} x\_j \exp\left(-\frac{2 \pi i }{N} k j \right) = \frac{1}{\sqrt{N}} \sum_{j=0}^{N-1} x\_j \omega^{-kj}$$ 

</section>
<section data-markdown>
### Quantum Fourier Transform
 > The **Inverse Discrete Fourier Transform (IDFT)** is a function  
 > $F_N^{-1}: \mathbb{C}^N \to \mathbb{C}^N$ transforms a vector of complex numbers $\\begin{bmatrix} x\_0  & x\_1 & ... & x\_{N-1} \\end{bmatrix}^T$ into another vector of complex numbers $\begin{bmatrix} y\_0  & y\_1 & ... & y\_{N-1} \end{bmatrix}^T$ such that
$$y_k = \frac{1}{\sqrt{N}} \sum_{j=0}^{N-1} x_j \omega^{kj}$$
</section>
<section data-markdown>
### Quantum Fourier Transform

> The **Quantum Fourier Transform (QFT)** is the quantum gate with matrix representation $F_N^{-1}$ for some $N = 2^n$ and it transforms an $n$-qubit state $\ket{\psi} = \sum_{j=0}^{N-1} x_j \ket{j}$ to another $n$-qubit state $\ket\phi =\sum_{k=0}^{N-1} y_k \ket{k}  $ such that 
    $$y_k = \frac{1}{\sqrt{N}}\sum_{j=0}^{N-1} x_j \omega^{k j}$$

    
</section>
<section data-markdown>
### Quantum Fourier Transform
* Evaluating the DFT directly has a time complexity of $O(N^2)$
* Using a faster algorithm known as *Fast Fourier Transform (FFT)* allows us to calculate the DFT in $O(N \log N)$
* The QFT performs an action similar to the DFT in only $O((\log N)^2 )$
Note:
However, since the action is performed on the amplitudes of the quantum states, we cannot use the QFT as a replacement for the DFT
It still finds much use as a subroutine in other quantum algorithms
</section>
