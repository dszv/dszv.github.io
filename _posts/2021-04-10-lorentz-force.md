---
layout: post
title: "Lorentz force from symmetry"
author: "D."
categories: journal
tags: [quantum mechanics]
image: vanallen.jpg
---

In this article we will try to deduce the expression of the Lorentz force as a relation of expected values on the quantum mechanical formalism using symmetry arguments.

## Klein-Gordon equation with minimal coupling

Conventions: metric $ \eta_{ \mu \nu } = \text{diag} (+1, -1, -1, -1) $, natural units $ \hbar = c = 1$.

### Lorentz symmetry

It can be showed[^1] that the only possible terms of the Lagrangian for a complex scalar field $ \Phi (x) $ are of the form

$$
\begin{equation}\label{1}
 \mathcal{L} = C_1 \partial_{\mu }\Phi ^* \partial ^{\mu }\Phi + C_2 \Phi ^* \Phi \tag{1}
\end{equation}
$$

Renaming the constants $ C_1 = 1/2 $ and $ C_2 = -m^2 /2 $, we can call this the *Klein-Gordon Lagrangian*. Given the action of the system as

$$
\begin{equation}
 S = \int \mathrm{d}^4 x \ \mathcal{L} = \int \mathrm{d}^4 x \ \left ( \frac{1}{2} \partial_{\mu }\Phi ^* \partial ^{\mu }\Phi - \frac{m^2 }{2} \Phi ^* \Phi \right )
\end{equation}
$$

we use the least action principle to obtain the *Klein-Gordon equation*

$$
\begin{equation}\label{2}
 \delta _{\Phi ^*} S = 0 \quad \Rightarrow \quad \partial _{\mu } \partial ^{\mu } \Phi + m^2 \Phi = 0 \tag{2}
\end{equation}
$$

where $ \partial _{\mu} \partial ^{\mu } = \partial _0 ^2 - \nabla ^2 $. Using the following separation of variables 

$$
\begin{equation}
 \Phi (x) = \phi (\vec{x}) \exp \{ -iEx^0 \}
\end{equation}
$$

we obtain the equation for the spatial part of $ \Phi $:

$$
\begin{equation}
 \nabla ^2 \phi + (E^2 - m^2) \phi = 0
\end{equation}
$$

Taking into account the Einstein energy-mass relation $ E^2 = p^2 + m^2 $ we can solve this equation. We will not do that here.

### Gauge symmetry

We can make this field interact with another one by making the Klein-Gordon Lagrangian $ U(1) $*-gauge invariant*[^1]. The $U(1)$-gauge transformation is given by

$$
\begin{equation}
 \Phi(x) \quad \mapsto \quad \Phi '(x) = \Phi(x) \exp \{ -iq \alpha (x) \}
\end{equation}
$$

where $ \alpha (x) $ is a function and $ q $ is a constant which we need for later. At first sight, the Lagrangian $ \eqref{1} $ is not gauge invariant, but we can make it so by replacing the derivative with the *covariant derivative*

$$
\begin{equation}
 \partial _{\mu } \quad \Rightarrow \quad D_{\mu } = \partial _{\mu } + iqA_{\mu } (x)
\end{equation}
$$

where $ A(x) $ is a vector field, and $ q $ is called the coupling constant. The gauge transformation law needed for the vector field results

$$
\begin{equation}
 A_{\mu } (x) \quad \mapsto \quad A'_{\mu } (x) = A_{\mu } (x) + \partial _{\mu } \alpha (x)
\end{equation}
$$

This is the same transformation we  can make to the electromagnetic potential without changing its dynamics[^2]. Now

$$
\begin{equation}
 \mathcal{L} = \frac{1}{2}(\partial _{\mu } - iqA_{\mu }) \Phi ^* (\partial ^{\mu } + iqA^{\mu }) \Phi - \frac{m^2}{2} \Phi ^* \Phi
\end{equation}
$$

is $U(1)$-gauge invariant. The principle of least action gives the following equation for the scalar field

$$
\begin{equation}\label{3}
 \partial _{\mu } \partial ^{\mu } \Phi + [m^2 + iq(\partial _{\mu } A^{\mu }) + 2iq A^{\mu } \partial _{\mu } - q^2 A^2 ] \Phi = 0 \tag{3}
\end{equation}
$$

## Non-relativistic limit

We take the separation of variables for $ \eqref{2} $ as a reference to make the following ansatz for equation $ \eqref{3} $:

$$
\begin{equation}
 \Phi (x) = \Psi (x) \exp \{ -imx^0 \}
\end{equation}
$$

where

$$
\begin{equation}
 \Psi (x) = \phi (\mathbf{x})\exp \{ -i(E - m)x^0 \}
\end{equation}
$$

Calculating

$$
\partial _{\mu } \partial ^{\mu } \Phi = -(m^2 \Psi + 2im \partial _0 \Psi - \partial ^2 _0 \Psi + \nabla ^2 \Psi ) \exp \{-imx^0 \}
$$

and

$$
A^{\mu } \partial _{\mu } \Phi = A^0 \partial _0 \Phi + A^i \partial _i \Phi = [ A^0 (-im \Psi + \partial _0 \Psi ) + A^i \partial _i \Psi ] \exp \{-imx^0 \}
$$

we replace these results in $ \eqref{3} $ ending up with

$$
\begin{align}
 -2im \partial _0 \Psi + \partial ^2 _0 \Psi & - \nabla ^2 \Psi + iq (\partial _{\mu } A^{\mu } ) \Psi \\
    & + 2qm A^0 \Psi + 2iq A^0 \partial _0 \Psi + 2iq A^i \partial _i \Psi - q^2 A^2 \Psi= 0
\end{align}
$$

which can be rewritten as

$$
\begin{align}
 i \partial _0 \Psi - \frac{\partial ^2 _0 \Psi }{2m} - iq \frac{A^0 \partial _0 \Psi }{m} & - iq \frac{\partial _0 A^0 }{2m} \Psi + q^2 \frac{(A^0 )^2 }{2m} \\
 & = \frac{1}{2m}  \sum _j (i\partial _j + q A^j )(i \partial _j + q A^j ) \Psi + q A^0 \Psi
\end{align}
$$

Using the non-relativistic limit $ p \ll m $ for the Einstein relation

$$
\begin{equation}
 E = \sqrt{p^2 + m^2} \approx \frac{p^2}{2m} + m
\end{equation}
$$

we have

$$
\begin{equation}
 |i\partial _0 \Psi | = | (E - m) \Psi | \approx \left | \frac{p^2}{2m} \Psi \right | \ll | m \Psi |
\end{equation}
$$

and supposing that $ \mid \, q A^0 \mid \,\ll m $, we make these approximations in $ \eqref{3} $ to obtain

$$
\begin{equation}\label{4}
 i \frac{\partial \Psi}{\partial t} = \frac{1}{2m} (i\nabla + q \mathbf{A}) \cdot (i\nabla + q \mathbf{A}) \Psi + q A^0 \Psi \tag{4}
\end{equation}
$$

## Quantum mechanics 

If we interpret $ \Psi (x) $ in $ \eqref{4} $ as the probability amplitude to find a spin-less particle (with electric charge $q$) between $ \mathbf{x} $ and $ \mathbf{x} + \mathrm{d} \mathbf{x} $ at a time $ t $, $ A^0 \equiv \varphi $ as the electric potential, and $ \mathbf{A} $ as the magnetic potential, we obtain the *Schrödinger equation with minimal coupling*[^3]

$$
\begin{equation}\label{5}
 i \frac{\partial }{\partial t} \Psi (t, \mathbf{x}) = \left [ \frac{1}{2m} (\mathbf{p} - q \mathbf{A}) \cdot (\mathbf{p} - q \mathbf{A}) + q \varphi \right ] \Psi (t, \mathbf{x}) \tag{5}
\end{equation}
$$

where

$$
\begin{equation}
 H \equiv \frac{1}{2m} (\mathbf{p} - q \mathbf{A}) \cdot (\mathbf{p} - q \mathbf{A}) + q \varphi
\end{equation}
$$

and $ \mathbf{p} = -i\nabla $ is identified as the canonical momentum operator. At a classical level, this Hamiltonian, where $ \mathbf{p} = m\dot{\mathbf{x}} $, comes from the Lagrangian

$$
L = \frac{1}{2m} (m\dot{\mathbf{x}} - q \mathbf{A}) ^2 + q \varphi
$$

via a Legendre transformation[^4]. The conjugate momentum is defined as[^4]

$$
\begin{equation}
 \mathbf{P} = \frac{\partial{L}}{\partial \dot{\mathbf{x}}} = m \dot{\mathbf{x}} - q \mathbf{A}
\end{equation}
$$

also, this is the conserved quantity of the system following from invariance under translations using the Noether theorem[^4]. Using these arguments, we can define the new conjugate momentum operator by

$$
\begin{equation}
 \mathbf{P} = \mathbf{p} - q \mathbf{A} = -i\nabla - q \mathbf{A}
\end{equation}
$$

and write $ \eqref{5} $ as

$$
\begin{equation}
 i \frac{\partial }{\partial t} \Psi (t, \mathbf{x}) = \left ( \frac{1}{2m} \mathbf{P}^2 + q \varphi \right ) \Psi (t, \mathbf{x})
\end{equation}
$$

### Ehrenfest theorem

The Ehrenfest theorem states[^1] that the time evolution of the expected value for some operator $O$ is given by

$$
\begin{equation}
 \frac{\mathrm{d} }{\mathrm{d} t}\langle O \rangle = -i \langle [O, H]\rangle + \left \langle \frac{\partial O}{\partial t} \right \rangle
\end{equation}
$$

For the position operator we obtain

$$
\begin{equation}
 \frac{\mathrm{d} }{\mathrm{d} t}\langle \mathbf{x} \rangle = -i \langle [\mathbf{x}, H]\rangle = \frac{1}{m} \left \langle \mathbf{p} - q \mathbf{A} \right \rangle = \frac{1}{m} \langle \mathbf{P} \rangle 
\end{equation}
$$

and

$$
\begin{equation}
 m  \frac{\mathrm{d}^2 }{\mathrm{d} t^2 }\langle \mathbf{x} \rangle = \frac{\mathrm{d} }{\mathrm{d} t}\langle \mathbf{P} \rangle
\end{equation}
$$

supporting the definition of the conjugate momentum operator introduced above. Using the Ehrenfest theorem for this operator

$$
\begin{equation}
 \frac{\mathrm{d} }{\mathrm{d} t}\langle \mathbf{P} \rangle = -i \left \langle [\mathbf{P} , H] \right \rangle + \left \langle \frac{\partial \mathbf{P}}{\partial t} \right \rangle
\end{equation}
$$

and after a lot of calculations, we end up with

$$
\begin{equation}
 \frac{\mathrm{d} }{\mathrm{d} t}\langle \mathbf{P} \rangle = \frac{q}{2m} \left \langle \mathbf{P} \times (\nabla \times \mathbf{A}) - (\nabla \times \mathbf{A}) \times \mathbf{P} \right \rangle + q \left \langle - \nabla \varphi - \frac{\partial \mathbf{A}}{\partial t} \right \rangle
\end{equation}
$$

Remembering that $ \mathbf{B} = \nabla \times \mathbf{A} $ and $ \mathbf{E} = -\nabla \varphi  - \partial \mathbf{A} / \partial t $, we finally obtain

$$
\begin{equation}
 m  \frac{\mathrm{d}^2 }{\mathrm{d} t^2 }\langle \mathbf{x} \rangle = \frac{q}{2m} \left \langle \mathbf{P} \times \mathbf{B} - \mathbf{B} \times \mathbf{P} \right \rangle + q \left \langle \mathbf{E} \right \rangle 
\end{equation}
$$

which can be identified as the quantum-mechanical version of the Newton second law with the Lorentz force.

---

## References

[^1]: Schwichetenberg, J. *Physics from symmetry*. Springer.
[^2]: Jackson, J. *Classical Electrodynamics*. Wiley & Sons.
[^3]: Landau, L.; Lifshitz, E. *Quantum Mechanics, non-relativistic theory*. Pergamon.
[^4]: Goldstein, H.; Poole, C.; Safko, J. *Classical Mechanics*. Addison Wesley.
