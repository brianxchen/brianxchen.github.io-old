---
layout: post
title: How Maxwell's Equations hide the Wave Equation
tags:
  - physics
  - math
---
### Introduction
Every so often I'll be in a physics class, or a math class, and we'll talk about something that bridges the two in a beautiful WOW moment. Math is of course the natural language of physics, but sometimes I forget that they are linked as fundamentally as they are. A moment like this happened today that I thought was especially interesting because not only does it connect the abstract and general wave equation from partial differential equations to actual electromagnetic waves, it also makes manifest the fundamental relationship between the speed of light and electricity and magneticsm. It's that observation -- the ubiquity of the speed of light in all of E&M -- that motivated Einstein's discovery of special relativity.

I want to make this post as accessible as possible to those without much math background. In some ways jargon is inevitable, but I will do my best to explain what it means along the way! Because this is a truly deep observation that I think warrants the effort it takes to understand it.

### The Wave Equation

The wave equation in mathematics is an equation that governs how waves, like sound waves, water waves, and anything of a "periodic" or "wavey" sort evolves over time. 

Mathematically, it is writen as the following: 
$$\frac{\partial^2 u}{\partial t^2}=c^2\frac{\partial^2 u}{\partial x^2}$$. 
Let's go through these terms and see what they mean:

$$\frac{\partial^2 u}{\partial t^2}$$ is an example of a **partial derivative** -- specifically, the second partial derivative of $$u$$ with respect to **time**. $$u$$ tells us how tall or short the wave is at any time -- in other words, it is a *function* that indicates the shape of the wave. Taking the "derivative" of something means seeing how that thing changes -- in this case, we're seeing how the shape of the wave changes over time. For anyone who has taken a calculus or calculus-based physics class, you may recognize that taking the "second derivative" of position with respect to time is acceleration.

$$c^2$$ indicates how **fast** the wave is travelling. This is literally the speed of the wave.

Finally, we have a second partial derivative term: $$\frac{\partial^2 u}{\partial x^2}$$. This can be thought of the "curvature" of the wave, or how straight or curvy the wave is at any point along it.

### Maxwell's equations
Physics is full of laws. You may recognize some of the more famous ones, like

$$\textbf{F}=m\textbf{a}$$ (Newton's second law)

and

$$\textbf{F}=\frac{1}{4\pi \epsilon_0} \frac{q_1 q_2}{r^2}$$ (Coulomb's law).

What's important to note about these kinds of equations is that they are not "laws" in the sense that they can never be broken, but rather they are *empirical equations* that model what people have observed over time. Newton felt an apple fall on his head with the force of 5 newtons, and using the mass of the apple, he found a relationship bewtween the force he felt, the mass of the apple, and how fast the apple was accelerating in the air.

Similarly, the fundamental set of equations that govern electricity and magnetism (at least in the classical sense) are called **Maxwell's equations**. I'll list the four Maxwell's equations here:

1. $$\nabla \cdot \textbf{E}=\frac{\rho}{\epsilon_0}$$ (Gauss' Law) 
$$\textbf{E}$$ = **Electric field**
$$\rho$$ = **charge density**, or how much electric charge is enclosed within a certain volume. 
2. $$\nabla \cdot \textbf{B}=0$$ (no name)
$$\textbf{B}$$ = **Magnetic field**
3. $$\nabla \times \textbf{E}=-\frac{\partial B}{\partial t}$$ (Faraday's Law)
4. $$\nabla \times \textbf{B}=\mu_0\textbf{J}+\mu_0\epsilon_0\frac{\partial \textbf{E}}{\partial t}$$ (Ampere's law with Maxwell's correction)
$$\textbf{J}$$ = **current density**, or how much electric current is enclosed within a certain volume.
$$\mu_0$$ and $$\epsilon_0$$ are fundamental constants.

$$\nabla \cdot \textbf{A}$$ is called the **divergence** of $$\textbf{A}$$ and is a special kind of derivative used in vector calculus. In short, it is a measure of how much something like fluid tends to "move away" from a point.

$$\nabla \times \textbf{A}$$ is called the **curl** of $$\textbf{A}$$, and is also a special kind of derivative. It is a measure of how much something like fluid tends to "circulate around" a point.

### Finding the electromagnetic wave equation
We'll assume that there are **no sources** -- this means $$\rho=0$$ and $$\textbf{J}=0$$. Thus, we reduce the Maxwell's equations to 

1. $$\nabla \cdot \textbf{E}=0$$
2. $$\nabla \cdot \textbf{B}=0$$
3. $$\nabla \times \textbf{E}=-\frac{\partial B}{\partial t}$$
4. $$\nabla \times \textbf{B}=\mu_0\epsilon_0\frac{\partial \textbf{E}}{\partial t}$$

Let's take the curl of equation 3:
$$\nabla \times (\nabla \times \textbf{E})=\nabla \times (-\frac{\partial B}{\partial t})$$

The curl of the curl of a vector field $$\textbf{A}$$ can be reformulated with the following identity:
$$\nabla \times (\nabla \times \textbf{A})=\nabla(\nabla \cdot \textbf{A})-\nabla^2\textbf{A}$$,
where $$\nabla^2\textbf{A}$$ is called the [**Laplacian**](https://en.wikipedia.org/wiki/Laplace_operator) of a vector field $$\textbf{A}$$.

Using that identity, and taking the partial derivative on the right side outside of the parantheses, we get
$$\nabla(\nabla \cdot \textbf{E})-\nabla^2\textbf{E}=-\frac{\partial}{\partial t}(\nabla \times \textbf{B})$$

We defined $$\nabla \cdot \textbf{E}=0$$ so the first term vanishes, and we can use equation 4 on the right side:
$$\cancel{\nabla(\nabla \cdot \textbf{E})}-\nabla^2\textbf{E}=-\frac{\partial}{\partial t}(\mu_0\epsilon_0\frac{\partial \textbf{E}}{\partial t})$$

$$\mu_0\epsilon_0$$ can be taken out of the right side because they are constants, so the partial derivative is not affected by them.
$$\nabla^2\textbf{E}=\mu_0\epsilon_0\frac{\partial^2 \textbf{E}}{\partial t^2}$$

Moving the constants to the other side:
$$\frac{\partial^2 \textbf{E}}{\partial t^2}=\frac{1}{\mu_0\epsilon_0}\nabla^2\textbf{E}$$


Compare this to the general form of the wave equation we found in an earlier part:
$$\frac{\partial^2 u}{\partial t^2}=c^2\frac{\partial^2 u}{\partial x^2}$$

We have the second time derivative on the left side, and a constant multiplied by the second space derivative on the right side. The forms match! Just by manipulating Maxwell's equations, we've found a relationship between the time and space derivatives of electric field. We even see a relationship between the fundamental constants $$\mu_0$$ and $$\epsilon_0$$ and the "wave speed propagation" constant $$c$$ -- in particular,

$$c=\frac{1}{\sqrt{\mu_0\epsilon_0}}$$,

or the speed of electromagnetic waves  is $$\frac{1}{\sqrt{\mu_0\epsilon_0}}$$. If you calculate the right hand side, you'll find that it is about $$3\cdot10^8 \space m/s$$, or the speed of light, and this in fact is how the speed of light is defined today.

### Concluding thoughts
For anyone who's taken a physics class, it can almost feel like a pure math class with the amount of abstract manipulation of equations that occur sometimes. Despite that, I always find it amazing when something we learn about in math suddenly shows up in physics, and this was an especially prominent instance of this -- the wave equation just *popped out* of Maxwell's equations, as if by magic.

I also find it beautiful how these  constants that were originally meant to describe electric and magnetic field -- $$\epsilon_0$$ and $$\mu_0$$, respectively -- instead find themselves describing something as fundamental as the speed of light. These interconnections are not obvious whatsoever, but seeing them in action is just another example of the beauty to be found in math and physics. 

If physicists ever find a [theory of everything](https://en.wikipedia.org/wiki/Theory_of_everything) that unifies general relativity with quantum mechanics, I think it might feel like how I felt in class today -- profound in its simplicity and elegant in its explanatory power. 

Moments like these are what make me love learning physics, and I'm excited for many more. :)



