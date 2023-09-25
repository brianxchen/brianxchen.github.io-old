---
layout: post
title: Heisenberg uncertainty principle, proved with just math
tags:
  - physics
  - math
---
## Intro
This was a homework problem that I had for my mathematical methods for physics class, and I really enjoyed it! It was good practice using bra-ket notation and derives a really, really fundamental property about the world. It's really amazing how an inequality concerning physical observables -- the position of an object, its momentum, etc. -- have a profound relationship that can be expressed through pure math. This comes about by virtue of the idea that these quantities are treated as "operators" (like multiplication and division) acting on a wave function $\psi$ in quantum mechanics.

## Part 1 -- Schwarz inequality
For hermitian operators $A$, $B$, we want to show \ $$|\bra{\psi}AB\ket{\psi}|^2 \le \bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}$$.

The [Schwarz inequality](https://en.wikipedia.org/wiki/Cauchy%E2%80%93Schwarz_inequality) for vectors $a$, $b$ of an inner product space states that \
$$|\braket{a|b}| \le \sqrt{\braket{a|a}\braket{b|b}}$$.

Since $A$ and $B$ are operators, when we operate on some vector $\psi$ by either of these, we get a vector. Consider $a=A\psi$ and $b=B\psi$.

Plugging this into the Schwarz inequality yields \ $$|\braket{A\psi|B\psi}| \le \sqrt{\braket{A\psi|A\psi}\braket{B\psi|B\psi}}$$ \ $$|\bra{\psi}AB\ket{\psi}|^2 \le \bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}$$.

## Part 2 -- Triangle inequality

Our next goal is to show \ $$|\bra{\psi}[A,B]\ket{\psi}|^2 \le 4\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}$$ \, where $[A,B]$ is the commutator of the operators $A$, $B$ given by \ $$[A,B] = AB - BA$$.
We expand the left hand side: \
$$|\bra{\psi}[A,B]\ket{\psi}|^2 $$ \ $$=|\bra{\psi}AB-BA\ket{\psi}|^2 $$ \ $$=|\bra{\psi}AB\ket{\psi}-\bra{\psi}BA\ket{\psi}|^2$$. \ Note that both of these terms are just complex numbers, as they are the inner product of vector $\psi$ with another vector $AB\ket{\psi}$.

Expanding the left side of the inequality gives \ $$|\bra{\psi}AB-BA\ket{\psi}|^2 \le 4\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}$$ \ $$|\bra{\psi}AB\ket{\psi}-\bra{\psi}BA\ket{\psi}|^2 \le 4\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}$$.

Now, consider the triangle inequality for complex numbers $a$, $b$. We have \ $$|a+b| \le |a| + |b| \space \forall a, b \in \mathbf{C}$$. \ Since the two terms on the left hand side, $\bra{\psi}AB\ket{\psi}$ and $\bra{\psi}BA\ket{\psi}$, are just complex numbers, we can use the triangle inequality. \
$$|\bra{\psi}AB\ket{\psi}-\bra{\psi}BA\ket{\psi}| \le |\bra{\psi}AB\ket{\psi}| +|\bra{\psi}BA\ket{\psi}|$$. \
Squaring both sides, \ $$|\bra{\psi}AB\ket{\psi}-\bra{\psi}BA\ket{\psi}|^2 \le |\bra{\psi}AB\ket{\psi}|^2 +|\bra{\psi}BA\ket{\psi}|^2+2|\bra{\psi}AB\ket{\psi}||\bra{\psi}BA\ket{\psi}|$$

We can combine the terms on the right hand sign since again, $\bra{\psi}AB\ket{\psi}$ and $\bra{\psi}BA\ket{\psi}$ are just complex numbers, so they commute and they also obey the same inequality from part 1. Thus, \ $$\begin{equation}|\bra{\psi}[A,B]\ket{\psi}|^2 \le 4\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}\end{equation}$$.

## Part 3 -- Defining some useful operators

Consider two operators $A'\equiv A-\alpha\mathbf{1}$, $B'\equiv B-\beta\mathbf{1}$, where $\mathbf{1}$ is the identity matrix and $\alpha$, $\beta$ are real numbers. We will show that $A'$ and $B'$ are both hermitian, and thus that $[A',B']=[A,B]$.

Take the hermitian conjugate of $A'$: \
$${A'}^{\dagger}=A^{\dagger}-{\alpha}^{\star}\mathbf{1}^{\dagger}$$. \
$\mathbf{1}^{\dagger}=\mathbf{1}$, ${A}^{\dagger}=A$ since $A$ is hermitian, and ${\alpha}^{\star}=\alpha$ since $\alpha$ is real. Thus, \
$${A'}^{\dagger}=A-{\alpha}\mathbf{1}=A'$$, so $A'$ is hermitian. By symmetry, the same argument applies to $B'$: ${B'}^{\dagger}=B'$.

Now, \ $$[A', B']=A'B'-B'A'$$ \ $$=(A-\alpha\mathbf{1})(B-\alpha\mathbf{1})-(B-\alpha\mathbf{1})(A-\alpha\mathbf{1})$$ \ $$=AB-\beta A-\alpha B + \alpha\beta\mathbf{1}-(BA-\alpha B-\beta A + \alpha\beta\mathbf{1})$$ \ $$=AB-BA$$ \ $$=[A,B]$$.

## Part 4 -- Putting it all together

The expected value of an operator $A_{avg}$ in state $\ket{\psi}$ is defined as $A_{avg}=\bra{\psi}A\ket{\psi}$. Thus, the standard deviation of this measurement, or the "uncertainty", of $A$ in the normalized state $\psi$ is given as such: \ $$\Delta A = \sqrt{\bra{\psi}(A-A_{avg}\mathbf{1})^2|\ket{\psi}}$$ \ $$=\sqrt{\bra{\psi}A'^2|\ket{\psi}}$$, using the result from part 3.

Now, in part 2 we found that \ $$4\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi} \ge |\bra{\psi}[A,B]\ket{\psi}|^2$$ \ $$\rightarrow 2\sqrt{\bra{\psi}A^2\ket{\psi}|\bra{\psi}B^2\ket{\psi}} \ge |\bra{\psi}[A,B]\ket{\psi}|$$.

Since $A'$ and $B'$ are hermitian, we can insert them into this inequality. \ $$2\sqrt{\bra{\psi}A'^2\ket{\psi}|\bra{\psi}B'^2\ket{\psi}} \ge |\bra{\psi}[A',B']\ket{\psi}|$$$$\sqrt{\bra{\psi}A'^2\ket{\psi}|\bra{\psi}B'^2\ket{\psi}} \ge \frac{1}{2}|\bra{\psi}[A',B']\ket{\psi}|$$.\
$[A', B']=[A,B]$ and $\sqrt{\bra{\psi}A'^2|\ket{\psi}}=\Delta A$, and $\sqrt{\bra{\psi}B'^2|\ket{\psi}}=\Delta B$ by definition. Thus, combing all of these into the above inequality yields
\ $$\Delta A \Delta B \ge \frac{1}{2}|\bra{\psi}[A,B]\ket{\psi}|$$ \ for any two generic, hermitian operators $A$ and $B$! Any two operators exhibit an "uncertainty" that is a function of the **commutator** of the two operators. This does seem to make sense; a commutator is just an expression of how much two operators commute, so logically the uncertainty relation should be affected by this quantity.

To derive the so-called "Heisenberg uncertainty principle", which expresses the minimum uncertainty in position and momentum of a particle, we note that $[x,p]=i \hbar$ (this is called the [canonical commutation relation](https://en.wikipedia.org/wiki/Canonical_commutation_relation) between two quantities related by a Fourier transform), and that the [position and momentum operators are hermitian](https://physics.stackexchange.com/questions/593204/showing-that-position-and-momentum-operators-are-hermitian). Thus, \ $$\Delta x \Delta p \ge \frac{1}{2}|\bra{\psi}i\hbar\ket{\psi}|$$ \ $$\Delta x \Delta p \ge \frac{\hbar}{2}$$