<section data-markdown>
### Reflection about a Vector
> Given vectors $\ket\psi, \ket\phi \in \mathcal{H}$, the operator $R_\psi = 2 \ket\psi \bra\psi - I$ applied to $\ket\phi$ represents the reflection of $\ket\phi$ about the direction of $\ket\psi$

Let $\mathcal{H}_\psi^\perp \subset \mathcal{H}$ represent the subspace of $\mathcal{H}$ orthogonal to $\ket\psi$.

Let $\ket{\psi^\perp} \in \mathcal{H}_\psi^\perp$ such that $\ket{\psi^\perp} = \ket\phi - a \ket\psi$ for some $a \in \mathbb{C}$ 

$\implies \ket\phi = a \ket\psi + \ket{\psi^\perp}$

$R_\psi \ket\phi = (2 \ket\psi \bra\psi - I) \ket\phi$

$ = 2 \ket\psi \bra\psi \ket\phi - \ket\phi = 2 \ket\psi \bra\psi ( a \ket\psi + \ket{\psi^\perp}) - \ket\phi$

$ = 2 a \ket\psi \braket{\psi|\psi} + 2 \ket\psi \braket{\psi|\psi^\perp} - \ket\phi = 2 a \ket\psi - \ket\phi$

$ = 2 a \ket\psi - (a \ket\psi + \ket{\psi^\perp}) = a \ket\psi - \ket{\psi^\perp}$

</section>
<section>
<h3>Reflection about a Vector</h3>
<blockquote><p>Given vectors $\ket\psi, \ket\phi \in \mathcal{H}$, the operator $R_\psi = 2 \ket\psi \bra\psi - I$ applied to $\ket\phi$ represents the reflection of $\ket\phi$ about the direction of $\ket\psi$</p></blockquote>

<img src="media/reflection.png" height="500"></img>
</section>
<section data-markdown>
### Reflection about a Vector
> Given vectors $\ket\psi, \ket\phi \in \mathcal{H}$, the operator $R_\psi = 2 \ket\psi \bra\psi - I$ is unitary and therefore is a valid quantum gate

$R_\psi R_\psi^\dagger = (2 \ket\psi\bra\psi - I)(2 \ket\psi\bra\psi - I)^\dagger$ 

$ = (2 \ket\psi\bra\psi - I) (2 (\ket\psi\bra\psi)^\dagger - I^\dagger)$

$ = (2 \ket\psi\bra\psi - I)(2 \ket\psi\bra\psi - I)$

*Because $(\ket\psi\bra\psi)^\dagger = \ket\psi\bra\psi$*

$ = 4\ket\psi\bra\psi - 2 \ket\psi \bra\psi - 2 \ket\psi \bra\psi + I = I$

</section>
