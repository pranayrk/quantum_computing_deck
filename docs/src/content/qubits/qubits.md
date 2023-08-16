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
> A **qubit** is any quantum mechanical system which is associated with $2$-dimensional complex Hilbert space $\mathcal{H}_S$ (known as the **state space** and follows the below postulates:
> * Postulate of **Superposition**
> * Postulate of **Measurement**
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

* The standard inner product of the $\ket{\psi}$ with itself in the Hilbert space $\mathcal{H}$ can therefore be written as $\braket{\psi | \psi} = \bra{\psi}\ket{\psi} = \begin{bmatrix} \overline{a} & \overline{b}\end{bmatrix} \begin{bmatrix} a \\\\ b \end{bmatrix} = |a|^2 + |b|^2$

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

</section>
