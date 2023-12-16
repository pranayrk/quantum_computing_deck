<section data-markdown>
### Tensor Space
> Consider we have finite dimensional Hilbert spaces $\mathcal{H}\_1$ and $\mathcal{H}\_2$.  
> Consider fixed vectors $\ket{\psi} \in \mathcal{H}\_1$ and $\ket{\phi} \in \mathcal{H}\_2$  
> Define a function $f_{\psi,\phi}: \mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C}$ as $f_{\psi,\phi}(\ket\xi, \ket\eta) = \braket{\xi|\psi}\_{\mathcal{H}\_1} \braket{\eta | \phi}\_{\mathcal{H}\_2}$   
> for some $\ket{\xi} \in \mathcal{H}\_1, \ket{\eta} \in \mathcal{H}\_2$.  
>   
> Then the function $f\_{\psi,\phi}$ is conjugate linear and continuous.


> The function $f_{\psi, \phi}$ is known as the **tensor product** of $\ket\psi$ and $\ket\phi$.
>
> In Dirac bra/ket notation, the function $f_{\psi,\phi}$ is denoted as $\ket{\psi} \otimes \ket{\phi}$ &nbsp; or &nbsp;  $\ket\psi \ket\phi $ &nbsp; or &nbsp;  $\ket{\psi\phi}$

---
### Tensor Space

> Given two Hilbert spaces $\mathcal{H}\_1$ and $\mathcal{H}\_2$, consider $\mathcal{G}$ to be the set of all anti-linear and continuous functions from $\mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C}$.  
>
> Then $G = \\{ g: \mathcal{H}\_1 \times \mathcal{H}\_2 \\; | \\; g \text{ is antilinear and continuous } \\}$ is a  
> vector space over $\mathbb{C}$ with vector addition  
> defined as $[g\_1 + g\_2](\ket\xi, \ket\eta) = g\_1(\ket\xi, \ket\eta) + g\_2(\ket\xi, \ket\eta)$   
> and scalar multiplication defined as expected.

> Consider $\mathcal{F} = \\{ \\; \ket\psi \otimes \ket\phi \\;\\; | \\;\\; \ket\psi \in \mathcal{H}\_1 \text{ and } \mathcal{H}\_2 \\}$  
> Then $\mathcal{F} \subseteq \mathcal{G}$.

---
### Tensor Space

> Let $\\{ \ket{ e\_{i}} \\}\_{i = 1}^n$ be an orthonormal basis for $\mathcal{H}\_1$ and $\\{ \ket{f_{j}} \\}\_{j = 1}^m$ be an orthonormal basis for $\mathcal{H}\_2$. 
> 
> Then $\\{ \ket{e\_{i}} \otimes \ket{f\_{j}} \\}$ is a basis  
> for $\mathcal{G} = \\{ g: \mathcal{H}\_1 \times \mathcal{H}\_2 \to \mathbb{C} \\;\\; | \\;\\; g \text{ is antilinear and continuous } \\; \\}$

> Consider two vectors $\ket{\psi}\_1 \otimes \ket{\phi}\_1$ and $\ket{\psi}\_2 \otimes \ket{\phi}\_2$ in $\mathcal{F}$.  
> 
> Then $\braket{\ket\psi\_1 \otimes \ket\phi\_1 \\; | \\; \ket\psi\_2 \otimes \ket\phi\_2 } = \braket{\psi\_1|\psi\_2}\_{\mathcal{H}\_1} \braket{\phi\_1|\phi\_2}\_{\mathcal{H}\_2}$ defines an inner product on $\mathcal{F}$.

> Let $g_1, g_2 \in \mathcal{G}$ where $g_1 = \sum_{i=1}^n c\_i ( \ket{e}\_{1i} \otimes \ket{f}\_{1j} )$ and  $g_2 = \sum_{j=1}^m d\_j (\ket{e}\_{2i} \otimes \ket{f}\_{2j}) $.
>
> Then $\braket{\\; g_1 | g_2 \\;} = \sum_{i = 1}^n \sum_{j=1}^m \overline{c_i} d_j \braket{e_{1i} \otimes f_{1j} | e_{2i} \otimes f_{2j}}$ defines an inner product on $\mathcal{G}$.



</section>
