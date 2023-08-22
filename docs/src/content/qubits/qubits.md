<section data-markdown>
### Qubits
* The computers we use today rely on classical information theory, which are based on **bits** (binary digits) which can represents a $0$ or $1$ state.
* These computers (which will be referred to as **classical computers**) are equivalent to a Turing Machine in computational efficiency.
* On a quantum computer the **qubit** (quantum bit) is the basic unit of information.
---
### Qubits
* While bits take only two values, qubits can take on a continuum of values
* On a real-life quantum computer, a qubit can be implemented using a variety of quantum phenomena
* In labs, qubits have been implemented using photon polarization, electron spin, the ground/excited state of an atom in a cavity, and even defect centers in a diamond.

Note: 
* While there could be many such real-life realizations of qubits, we are not concerned with the specific implementation, as long as they follow certain rules
* We will abstract out these rules to form an abstract qubit that we can work with without knowing the specific details of the implementation
---
### Qubits
> A **qubit** is any quantum mechanical system which is associated with $2$-dimensional complex Hilbert space $\mathcal{H}$ (known as the **state space** and follows the below postulates:
> * Postulate of **Superposition**
> * Postulate of **Measurement**
> * Postulate of **Projection** `TODO: Refer Scherer, P37`
> * Postulate of **Entanglement**
> * Postulate of **Transformation**
>
> A given state of the system is completely described by a  
> *unit vector* $\ket{\psi}$, which is called the **state vector** (or wave function) on the Hilbert Space 

---
### Qubits
> **Notation:**  
> Observe above that we have written the vector   
> $\vec{\psi} \in \mathcal{H}$ as $\ket{\psi}$. This is the notation for a vector in Dirac's bra/ket notation, and is read **ket psi**
* Normally, when working with the Hilbert space associated with a quantum system, we use *orthogonal bases*
* The standard basis (or **computational basis**) of the two dimensional complex vector space $\mathcal{H}$ is $\\{ \ket{0}, \ket{1} \\}$ where
    $\ket{0} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}$ and $\ket{1} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}$

Note:
This is because these orthogonal bases represent perfectly distinguishable states (refer Shor's Notes, Lec 02)

---
### Qubits
> **Postulate of Superposition:**  
> With respect to the computational basis $\{ \ket{0}, \ket{1} \}$, the state of the qubit can be described as $\ket{\psi} = a \ket{0} + b \ket{1}$  
> $ = \begin{bmatrix} a \\\\ 0 \end{bmatrix} + \begin{bmatrix} 0 \\\\ b \end{bmatrix} = \begin{bmatrix} a \\\\ b \end{bmatrix} $ where $a, b \in \mathbb{C}$ and $a^2 + b^2 = 1$.

* Another common basis is the **Hadamard Basis** $\{ \ket{+}, \ket{-} \}$ where  
     $\ket{+} = \displaystyle\frac{1}{\sqrt 2} (\ket{0} + \ket{1})$ and $\ket{-} = \displaystyle\frac{1}{\sqrt 2} (\ket{0} - \ket{1})$

Note: 
The above follows from the Schrodinger Wave Equation which is a linear first order differential equation.

---
### Qubits
* Qubits are called **two-state** quantum systems. This does not mean that this system has only two states, but rather that all possible states exist as a linear combination of just two states
* There could be quantum systems whose states are modelled as vectors in $3$-dimensional vector spaces, these are called **qutrits**. 
* Similarly, quantum systems whose states are modelled with $n$-dimensional vector spaces are called **qudrits**. 

---
### Qubits
* The state of a qubit is a continuum which might indicate that we can use a single qubit to store an infinite amount of information
* However, a principal of quantum mechanics states that we cannot interact with the qubit without fundamentally altering its state
* To work with the state stored in a qubit, we must perform a measurement which forces the state of the qubit to "collapse" into one of two *preferred states*
---
### Qubits

> **Postulate of Measurement:**
>
> Any measurement device that interacts with the qubit will be calibrated with a pair of orthonormal vectors called the **preferred basis**, say $\\{ \ket{u}, \ket{v} \\}$.  
> If the state of the qubit with respect to the preferred basis is $\ket{\psi} = a \ket{u} + b \ket{v}$, then measurement of the qubit will yield either $\ket{u}$ with a probability of $|a|^2$  
> or $\ket{v}$ with a probability $|b|^2$.  
> After measurement, the state of the qubit itself will be changed to the output of the measurement.

Note: 
* This behaviour is an axiom of quantum mechanics substantiated by empirical observations from experiments over the last hundred years.

---
### Qubits
* This property limits the amount of information that can be extracted from a qubit: a measurment yields atmost a single classical bit worth of information
* In most cases, we also cannot make more than one measurement of original state of the qubit
* On measurement, we have two possibilities, each corresponding to a probability of $|a|^2$ and $|b|^2$, then the total probability of the whole space will be $|a|^2 + |b|^2 = 1$, which is valid for unit vectors $\ket{\psi} = a \ket{0} + b \ket{1}$.
---

### Qubits

> **Notation:**  
> When $\ket{\psi} = a \ket{0} + b \ket{1} = \begin{bmatrix} a \\\\ b \end{bmatrix}$, then  
> $\bra{\psi}$ is the conjugate transpose of $\ket{\psi}$ and is read as **bra psi**, 
> $\bra{\psi} = \begin{bmatrix} \overline{a} & \overline{b}\end{bmatrix}$

* This lets us write the inner product for $\mathcal{H}$ as:  
    For any $\ket{v} = \begin{bmatrix} a \\\\ b \end{bmatrix}, \ket{w} = \begin{bmatrix} c \\\\ d \end{bmatrix} \in \mathcal{H}$, the operation 
    $\braket{v|w} = \bra{v}\ket{w} = \begin{bmatrix} \overline{a} & \overline{b} \end{bmatrix} \begin{bmatrix} c \\\\ d \end{bmatrix} = \overline{a} c + \overline{b} d $

---
### Qubits
* **Note:** We will consider the inner product as being linear in the second variable and conjugate-linear in the first variable.
* If $\ket{\psi} = \begin{bmatrix} a \\\\ b \end{bmatrix}$, then we can show $\braket{0|\psi} = a$, $\braket{1|\psi} = b$. 
    Therefore we can write $\ket{\psi} = a \ket{0} + b \ket{1} = \braket{0|\psi} \ket{0} + \braket{1|\psi} \ket{1}$
* The standard inner product of the $\ket{\psi} = \begin{bmatrix} a \\\\ b \end{bmatrix}$ with itself in the Hilbert space $\mathcal{H}$ can therefore be written as $\braket{\psi | \psi} = \bra{\psi}\ket{\psi} = \begin{bmatrix} \overline{a} & \overline{b}\end{bmatrix} \begin{bmatrix} a \\\\ b \end{bmatrix} = |a|^2 + |b|^2$

---
### Qubits
> **Postulate of Measurement:**
> Any physical observable is associated with a self-adjoint operator $\mathcal{A}$ on the Hilbert space $\mathcal{H}_S$. The possible outcome of a measurement of the observable $\mathcal{A}$ is one of the eigenvalues of the operator $\mathcal{A}$.  
> Writing the eigenvalues equation,
> $\mathcal{A} \ket{i} = a_i \ket{i}$
> where $\ket{i}$ is an orthonormal basis of eigenvectors of the operator $\mathcal{A}$, and 
> $\ket{\psi} = \sum_i c_i \ket{i}$,
> then the probability that a measurement of the observable $\mathcal{A}$ results in the outcome $a_i$ is given by
> $p_i = |\braket{i|\psi}|^2 = |c_i|^2$

`TODO: Proof that self-adjoint matrices represent measurement operators`

---
### Qubits
* Let $\mathcal{H_1}$ be an $n$-dimensional vector space with basis $\alpha = \\{ \ket{a_1}, \ket{a_2}, ..., \ket{a_n} \\}$ and $\mathcal{H_2}$ be an $m$-dimensional vector space with basis $\beta = \\{ \ket{b_1}, \ket{b_2}, ..., \ket{b_n} \\}$, the tensor product $\mathcal{H_1} \otimes \mathcal{H_2}$ is an $nm$-dimensional space with basis elements of the form $\ket{a_i} \otimes \ket{b_j}$ 

> **Notation:**  
> In dirac's bra/ket notation, the tensor product of  
>  $\ket{v} \in \mathcal{H_1}, \ket{w} \in \mathcal{H_2}$ is $\ket{vw} = \ket{v}\ket{w} = \ket{v} \otimes \ket{w}$

---
### Qubits
* The tensor product is defined to satisfy the following properties:
    1. $(\ket{v_1} + \ket{v_2} ) \ket{w} = \ket{v_1}\ket{w} + \ket{v_2}\ket{w}$
    2. $\ket{v}(\ket{w_1} + \ket{w_2}) =  \ket{v}\ket{w_1} + \ket{v}\ket{w_2}$
    3. $(a \cdot \ket{v})\ket{w} = \ket{v}(a \cdot \ket{w})  = a \cdot (\ket{v}\ket{w})$
* Every element $\ket{\sigma} \in \mathcal{H_1} \otimes \mathcal{H_2}$ can be written as a superposition of elements of the basis $\\{ \ket{a_i}\ket{bj} \\}$  
   as $\ket{\sigma} = \alpha_{11} \ket{a_1 b_1} + \alpha_{12} \ket{a_1 b2} + ... + \alpha_{nm} \ket{a_n b_m}$
* Most elements $\ket{\sigma} \in \mathcal{H_1} \otimes \mathcal{H_2}$ *cannot* be decomposed to $\ket{\sigma} = \ket{v}\ket{w}$ where $v \in \mathcal{H_1}, w \in \mathcal{H_2}$.  
    `TODO: Check proof`
---
### Qubits
* As we have observed, a single qubit only gives us one classical bit worth of information. This equivalence diverges once we include *multiple* interacting qubits in the system
* A system of $n$ classical bits will have one degree of freedom for each bit, resulting in a state-space of $n$ dimensions, i.e. classical systems are linear in $n$
* In quantum systems, however, a system of $n$ qubits will result in a state space of $2^n$ dimensions.
* This is because of the quantum property of *entanglement* which describes how quantum systems interact with each other.
---
### Qubits
> **Postulate of Entanglement**  
> When we have two qubits being treated as a combined system, the state space of the combined system is the tensor product $\mathcal{H_1} \otimes \mathcal{H_2}$ of the state spaces $\mathcal{H_1}, \mathcal{H_2}$ of the component qubit subsystems.  
> If the first qubit is in state $\ket{\psi}$ and the second in state $\ket{\sigma}$, then the combined system of two interacting qubits is in state $\ket{\psi\sigma} = \ket{\psi}\ket{\sigma}$.  
> Similarly, for a system of $n$ qubits, the state space is the tensor product $\mathcal{H_1} \otimes \mathcal{H_2} \otimes ... \otimes \mathcal{H_n}$ of the state spaces of the $n$ independent qubits.
---
### Qubits
* The most natural basis for $\mathcal{H} = \mathcal{H_1} \otimes \mathcal{H_2}$ is constructed from the tensor products of the basis vectors of $\mathcal{H_1}$ (say $\\{ \ket{0}_1, \ket{1}_1 \\}$ and of $\mathcal{H_2}$ (say $\\{ \ket{0}_2, \ket{1}_2 \\}$), then a basis for $\mathcal{H}$ is given by $\\{ \ket{0}_1\ket{0}_2, \ket{0}_1\ket{1}_2, \ket{1}_1\ket{0}_2, \ket{1}_1\ket{1}_2 \\} = \\{ \ket{00}, \ket{01}, \ket{10}, \ket{11} \\}$
* We will often this basis as $ \\{ \ket{00}, \ket{01}, \ket{10}, \ket{11} \\} = \\{ \ket{0}, \ket{1}, \ket{2}, \ket{3} \\}$ when the context is unambiguous.
* So an arbitary state $\ket{\psi} \in \mathcal{H}$ can be described as  
  $\ket{\psi} = c_0 \ket{00} + c_1 \ket{01} + c_2 \ket{10} + c_3 \ket{11} $  
$ = c_0 \ket{0} + c_1 \ket{1} + c_2 \ket{2} + c_3 \ket{3}$.

---
### Qubits
* A state $\ket{\psi}$ is said to be **entangled** if it cannot be written as a simple tensor product of states $\ket{v} \in \mathcal{H_1}$ and $\ket{w} \in \mathcal{H_2}$. If we can write $\ket{\psi} = \ket{v}\ket{w}$, the state is said to be **seperable**.

* **Example:** Consider the state $\ket{\psi_1} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11})$. We can show this is entangled. `TODO`
* **Example:** Consider the state $\ket{\psi_2} = \frac{1}{\sqrt{2}} (\ket{01} + \ket{11})$. We can show this is seperable since we can write $\ket{\psi_2} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) \otimes \ket{1}$

</section>
