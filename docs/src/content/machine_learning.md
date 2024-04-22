<section data-markdown>
# Applications to Machine Learning
</section>
<section>
<h3>Components of a Machine Learning System</h3>
<img src="media/ml.drawio.png"></img>

<p><b>Data</b> $\to$ <b>Model</b> $\to$ <b>Training</b></p>

</section>
<section data-markdown>
### Quantum Optimization in Training
* Training a machine learning model involves minimizing the difference between the models output and the expected output
* The training stage of a machine learning model is often the most time-consuming process.
* This training step can be formulated as minimizing a cost function
* Finding global minima among a large number of local minima is often the most significant challenge
</section>
<section data-markdown>
### Quantum Optimization in Training
##### D&#252;rr-Høyer Algorithm

> To find the global minimum of a function $f$ among $N$ local minima

* Choose a random local minima and label it $y$
* Repeat the following steps $22.5 \sqrt{N} + 1.4 \text{lg}^2(N)$
    * Run Grover's algorithm to find an element $y_n$ which results in a value $f(y_n)$ less than $f(y)$
    * If we find such a $y_n$, set $y = y_n$ for the next iteration.
* Return y.
</section>
<section data-markdown>
### Types of Machine Learning Models
* **Linear:** These are deterministic methods use a model function of the form $f = \phi(\bm{w}^T \bm{x})$.
* **Neural Networks:** These models can be probabilistic or deterministic and they have components that resemble neurons.
* **Graphical Methods:** These are probabilistic models that use graphical techniques to display and simplify probability distributions operating over the input data.
* **Kernel Methods:** Kernel methods solve machine learning tasks based on a similarity measure between data points.
</section>
<section data-markdown>
### Quantum Neural Network using QFT


Unlike standard neural networks, Convolutional Neural Networks (CNNs) use the operation of **convolution** between layers.


> Shen, F., & Liu, J. (2021). *QFCNN: Quantum Fourier Convolutional Neural Network*  
> https://doi.org/10.48550/arxiv.2106.10421

This paper describes the use of QFT to speed up the convolution operation. 
</section>
<section data-markdown>
### Quantum Neural Network using QFT

> The **discrete convolution** of two vectors $X = \begin{bmatrix} x\_0  & x\_1 & ... & x_{N-1} \end{bmatrix}^T$ and $K = \begin{bmatrix} k\_0  & k\_1 & ... & k_{N-1} \end{bmatrix}^T$ is a vector of length $N$ whose components are given by $$(X * K)\_m = \sum\_{j=0}^{N-1} x\_{m-j} k\_{j}$$

</section>
<section data-markdown>
### Quantum Neural Network using QFT

> **Convolution Theorem:** For two vectors $X = \begin{bmatrix} x_0  & x_1 & ... & x_{N-1} \end{bmatrix}^T$ and $K = \begin{bmatrix} k_0  & k_1 & ... & k_{N-1} \end{bmatrix}^T$,  
> the convolution $(X * K)$ of $X$ and $K$ is given by $$(X * K) = F_N^{-1} (F_N(X) \cdot F_N(K))$$
</section>
<section data-markdown>
### Quantum Neural Network using QFT


> Lomont, C. (2003). *Quantum convolution and quantum correlation algorithms are physically impossible.*  
> https://doi.org/10.48550/arxiv.quant-ph/0309070

This paper suggests that is no physically realizable process $P$ to compute the convolution of the coefficients of two quantum states.   
</section>
<section data-markdown>
### Quantum Neural Network using QFT
* Feihong Shen and Jun Liu circumvented this problem by devising a quantum circuit which implements a process $M$ described as 
 $$\sum_{i,j = 0}^{N-1} x_i k_j \ket{ij} \overset{M}{\to} \sum_{i,j = 0}^{N-1} x_i k_{i+j} \ket{ij}$$

* Applying the Inverse QFT operation on the result of the process $M$ will result in the convolution $$\left( \sum_{i = 0}^{N-1} x_i \ket{i} \right) * \left( \sum_{m = 0}^{N-1} k_m  \exp(- 2 \pi i m j) \ket{m} \right)$$
</section>
<section data-markdown>
### Kernel Methods
* Kernel methods are based on finding the similarity between any two data points
* This similarity measure is captured by a *kernel function*
* An example of a kernel function would be the the radial basis function kernel (RBF kernel) given by  $$\mathcal{K}(\bm{x_i}, \bm{x_j}) = \exp\left( - \frac{||\bm{x_i} - \bm{x_j}||^2}{2 \sigma^2} \right)$$ gives a similarity score between $0$ and $1$ for any two data points $\bm{x_i}$ and $\bm{x_j}$ which increases with distance between the two points.
</section>
<section data-markdown>
### Kernel Methods
> A function $\mathcal{K}: \mathcal{X} \times \mathcal{X} \to \mathbb{R}$ is called a **kernel function** if there exists a Hilbert space $\mathbb{F}$ and a function $\phi: \mathcal{X} \to \mathbb{F}$ such that $$\mathcal{K}(\bm{x_i}, \bm{x_j}) = \braket{\phi(\bm{x_i}), \phi(\bm{x_j})}$$  
> The function $\phi: \mathcal{X} \to \mathbb{F}$ is called the **feature map** and the Hilbert space $\mathbb{F}$ is called the **feature space**.
</section>
<section data-markdown>
### Kernel Methods
* Kernel methods are commonly used to classify patterns
* Kernel methods enable us to use a linear classifier to solve a non-linear problem.
* The feature map of a kernel embeds the linearly inseparable data into the higher dimensional feature space where the patterns can be discovered as linear relations.
* This is known as the *kernel trick*.
</section>
<section>
<h3>Kernel Methods</h3>
<figure height="30%">
<img width="45%" src="media/schuld_a.png"></img>
<img width="50%" src="media/schuld_b.png"></img>
  <figcaption>courtesy Schuld & Petruccione:  Machine Learning with Quantum Computers</figcaption>
</figure>

$$\phi(\bm{x}) = \phi(\begin{bmatrix}
         x_1 & x_2
     \end{bmatrix}^T) = \begin{bmatrix}
         x_1 &  x_2 & \frac{1}{2} (x_1^2 + x_2^2)
     \end{bmatrix}^T$$
</section>
<section data-markdown>
### Kernel Methods

 Consider $\mathcal{X} \subseteq \mathbb{R}^2$ and the kernel $$\mathcal{K}(\bm{x}, \bm{y}) = x_1^2 y_1^2 + x_2^2 y_2^2 + 2 x_1 y_1 x_2 y_2$$

    
Consider the feature space as $\mathbb{R}^3$ enriched with the standard dot product and a feature map $\phi_1(\bm{x}) : \mathbb{R}^2 \to \mathbb{R}^3$ defined as 
    $$\phi_1(\bm{x}) = \begin{bmatrix}
        x_1^2 & x_2^2 & \sqrt{2} x_1x_2
    \end{bmatrix}^T $$

which gives

$$\mathcal{K}(\bm{x}, \bm{y}) = x_1^2 y_1^2 + x_2^2 y_2^2 + 2 x_1 y_1 x_2 y_2 = \braket{\phi_1(\bm{x}), \phi_1(\bm{y})}$$

</section>
<section data-markdown>
### Kernel Methods
 Consider $\mathcal{X} \subseteq \mathbb{R}^2$ and the kernel $$\mathcal{K}(\bm{x}, \bm{y}) = x_1^2 y_1^2 + x_2^2 y_2^2 + 2 x_1 y_1 x_2 y_2$$

 
Alternatively, we can also consider the feature space as $\mathbb{R}^4$ and the feature map $\phi_2(\bm{x}) : \mathbb{R}^2 \to \mathbb{R}^4$ defined as $$\phi_2(\bm{x}) = \begin{bmatrix}
        x_1^2 & x_2^2 & x_1x_2 & x_2 x_1
    \end{bmatrix}$$
which gives
        $$\mathcal{K}(\bm{x}, \bm{y}) = x_1^2 y_1^2 + x_2^2 y_2^2 + 2 x_1 y_1 x_2 y_2 = \braket{\phi_2(\bm{x}), \phi_2(\bm{y})}$$

</section>
<section data-markdown>
### Kernel Methods
>  A function $f: \mathcal{X} \times \mathcal{X} \to \mathbb{R}$ is **finitely positive semi-definite** if it is a symmetric function for which the matrices formed by restriction to any finite subset of the space $\mathcal{X}$ (Gram matrices)  are positive semi-definite matrices.

> Kernel functions are finitely positive semi-definite.
</section>
<section data-markdown>
### Kernel Methods

> Let $\mathcal{K}: \mathcal{X} \times \mathcal{X} \to \mathbb{R}$ be either a continuous function or a function on a finite domain which is finitely positive semi-definite.  
> Then $\mathcal{K}$ is a kernel function. 

The proof of this theorem involves constructing a feature space $\mathbb{F}\_K$ and a feature map $\phi: \mathcal{X} \to \mathbb{F}\_K$ such that $$\mathcal{K}(\bm{x_i}, \bm{x_j}) = \braket{\phi(\bm{x_i}), \phi(\bm{x_j}) }$$

This specific feature space involved in this construction is known as the **Reproducing Kernel Hilbert Space (RKHS)**.

</section>
<section data-markdown>
### Kernel Methods

> A **Reproducing Kernel Hilbert space (RKHS)** is a Hilbert space of functions in which point evaluation is a continuous linear functional, that is, an RKHS is a Hilbert space of functions where all evaluation functionals $e_{\bm{x}} : \mathbb{F}\_K \to \mathbb{R}$ defined as $$e_{\bm{x}}(f) = f(\bm{x})$$ are bounded and linear.
</section>
<section data-markdown>
### Kernel Methods
> **Reproducing Property:** Let $\mathbb{F}\_K$ be the RKHS of a kernel $\mathcal{K}(\bm{x_i}, \bm{x_j})$ and consider $f \in \mathbb{F}\_K$ such that $f(\bm{y}) = \sum_{i=1}^m a_i \mathcal{K}\_{\bm{x}\_i}(\bm{y})$. 
> Then $$\braket{f, \mathcal{K}\_{\bm{x}}} = \sum_{i=1}^m a_i \mathcal{K}(\bm{x_i}, \bm{x}) = f(\bm{x})$$


> **Moore–Aronszajn theorem**: Every positive definite kernel $\mathcal{K}(\bm{x_i}, \bm{x_j})$ is associated with a unique RKHS $\mathbb{F}\_K$.
</section>
<section data-markdown>
### Quantum Machine Learning as Kernel Methods


> Schuld, M. (2021). *Supervised quantum machine learning models are kernel methods*  
> https://doi.org/10.48550/ARXIV.2101.11020

This paper suggests that most quantum machine learning algorithms fall under the classification of kernel methods. 

*"... most supervised, deterministic quantum models can fundamentally be formulated as a classical kernel method whose kernel is computed by a quantum computer."*

</section>
<section>
<h3>Quantum Machine Learning as Kernel Methods</h3>

<figure>
<img height="40%" src="media/schuld_3.png"></img>
  <figcaption>courtesy Schuld & Petruccione:  Machine Learning with Quantum Computers</figcaption>
</figure>

$$\mathcal{K}(x_i, x_j) =\text{Trace}(\rho(x_j)^\dagger \rho(x_i)) = |\braket{\phi(x_j)| \phi(x_i)}|^2$$
</section>
<section data-markdown>
### Quantum Machine Learning as Kernel Methods
##### Inferences from RKHS of Quantum Kernel

* Quantum Machine Learning models are linear models in the feature space
* Quantum Machine Learning models as a kernel method are universal function approximators
* Training a quantum model means to find the measurement which minimises a cost function that depends on
training data
* Most quantum models can be formulated as general support vector machines with a kernel evaluated on a quantum computer
* This allows the results of kernel theory to be applied directly to these models.
</section>
