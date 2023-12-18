<section data-markdown>
### Quantum Teleportation
* Quantum teleportation is a technique for transferring quantum information from a sender at one location to a receiver some distance away.
* This protocol was developed by Artur Ekert in 1991. 
* The principle of quantum teleportation could be used to establish secure communication channels between two individuals using a quantum key distribution (QKD) scheme, which guarantees eavesdropper-proof encryption keys.
* The sender (canonically referred to as *Alice*) wants to transmit a quantum state to the receiver (canonically referred to as *Bob*) who is an arbitrary distance away.
* Consider a pair of qubits in the Bell state $\ket{\phi^+} = \frac{1}{\sqrt{2}} ( \ket{00} + \ket{11} ) $, i.e. an EPR pair
* The presupposition is that Alice and Bob met long ago and each took one qubit from the EPR pair and that they are able to communicate via a classical communication channel
---
### Quantum Teleportation
* Consider that Alice wants to send the state of a qubit $\ket\psi = a \ket{0} + b \ket{1}$.
* The coefficients $a$ and $b$ are unknown to both Alice and Bob.
* Even if the coefficients were known, since $\ket\psi$ has a continuum of possibilities, Alice would not be able to send the state purely through a classical channel.
* Consider that Alice's qubit is allowed to interact with the EPR pair to form a combined system.
* The state of that combined system of three qubits would be $\ket{\phi\_0} = \ket\psi \otimes \ket{\phi^+} =$  
    $ ( a \ket{0} + b \ket{1} ) \otimes \left (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) \right ) = $  
    $ \frac{1}{\sqrt{2}} (a \ket{000} + a \ket{011} + b \ket{100} + b \ket{111} )$
* Since the EPR pair is seperated, Alice can only interact with the first two qubits and Bob can only interact with the last qubit.

---
### Quantum Teleportation
> *Step 1* Alice applies the CNOT gate to the first two qubits

$\ket{\phi\_1} = (\text{CNOT} \otimes I) (\ket{\phi\_0}) = \frac{1}{\sqrt{2}} (\text{CNOT} \otimes I) (a \ket{000} + a \ket{011} + b \ket{100} + b \ket{111} )$

$ = \frac{1}{\sqrt{2}} (a \ket{000} + a \ket{011} + b \ket{110} + b \ket{101})$

> *Step 2* Alice applies the Hadamard gate to the first qubit

$\ket{\phi\_2} = (H \otimes I \otimes I) (\ket{\phi\_1}) = \frac{1}{\sqrt{2}} (H \otimes I \otimes I) \frac{1}{\sqrt{2}} (a \ket{000} + a \ket{011} + b \ket{110} + b \ket{101})$

$ = \frac{1}{2} \left [ \ket{00} (a \ket{0} + b \ket{1}) \\; + \\; \ket{01} ( a \ket{1} + b \ket{0} ) \\; + \\; \ket{10} (a \ket{0} + b \ket{1} ) \\; + \\; \ket{11} (a \ket{1} - b \ket{0} \right]$ 

---

### Quantum Teleportation
> *Step 3* Alice measures her qubits with respect to the computational basis



The current state of the system is 
$\frac{1}{2} \left [ \ket{00} (a \ket{0} + b \ket{1}) \\; + \\; \ket{01} ( a \ket{1} + b \ket{0} ) \\; + \\; \ket{10} (a \ket{0} + b \ket{1} ) \\; + \\; \ket{11} (a \ket{1} - b \ket{0} \right]$ 

Since the initial EPR pair was entangled, this will cause the whole system to collapse into the observed result state including Bob's qubit.

* *Case 1*: &nbsp; Alice measures $\ket{00} \implies $ Bob's qubit is in the state $a \ket{0} + b \ket{1}$
* *Case 2*: &nbsp; Alice measures $\ket{01} \implies $ Bob's qubit is in the state $a \ket{1} + b \ket{0}$
* *Case 3*: &nbsp;  Alice measures $\ket{10} \implies $ Bob's qubit is in the state $a \ket{0} - b \ket{1}$
* *Case 4*: &nbsp; Alice measures $\ket{11} \implies $ Bob's qubit is in the state $a \ket{1} - b \ket{0}$

---
### Quantum Teleportation

> *Step 4:* Alice sends her measurement result to Bob

Depending on what value Bob receives from Alice, he will apply the following gates to get the qubit in the required state $\ket\psi = a \ket{0} + b \ket{1}$

* *Case 1* &nbsp; Alice sends $\ket{00}$, then Bob will apply $I$ gate
* *Case 1* &nbsp; Alice sends $\ket{01}$, then Bob will apply $X$ gate
* *Case 1* &nbsp; Alice sends $\ket{10}$, then Bob will apply $Z$ gate
* *Case 1* &nbsp; Alice sends $\ket{11}$, then Bob will apply $ZX$ gate


</section>
