<section data-markdown>
### Reflection about a Vector
> Given vectors $\ket\psi, \ket\phi \in \mathcal{H}$, the operator $R_\psi = 2 \ket\psi \bra\psi - I$ applied to $\ket\phi$ represents the reflection of $\ket\phi$ about the direction of $\ket\psi$

Let $\mathcal{H}_\psi^\perp \subset \mathcal{H}$ represent the subspace of $\mathcal{H}$ orthogonal to $\ket\psi$.

Let $\ket{\psi^\perp} \in \mathcal{H}_\psi^\perp$ such that $\ket{\psi^\perp} = \ket\phi - \ket\psi$ $\implies \ket\phi = \ket\psi + \ket{\psi^\perp}$

*Note:* $\ket{\psi^\perp}$ is orthogonal to $\ket\psi$

$R_\psi \ket\phi = (2 \ket\psi \bra\psi - I) \ket\phi$

$ = 2 \ket\psi \bra\psi \ket\phi - \ket\phi = 2 \ket\psi \bra\psi (\ket\psi + \ket{\psi^\perp}) - \ket\phi$

$ = 2 \ket\psi \braket{\psi|\psi} + 2 \ket\psi \braket{\psi|\psi^\perp} - \ket\phi = 2 \ket\psi - \ket\phi$

$ = 2 \ket\psi - (\ket\psi + \ket{\psi^\perp}) = \ket\psi - \ket{\psi^\perp}$

</section>
<section>
<h3>Reflection about a Vector</h3>
<blockquote><p>Given vectors $\ket\psi, \ket\phi \in \mathcal{H}$, the operator $R_\psi = 2 \ket\psi \bra\psi - I$ applied to $\ket\phi$ represents the reflection of $\ket\phi$ about the direction of $\ket\psi$</p></blockquote>

<img src="media/reflection.png" height="500"></img>
</section>
