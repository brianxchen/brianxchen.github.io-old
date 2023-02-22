---
layout: post
title: Fuzzy objects and ontology
katex: True
tags:
  - philosophy
---
### Introduction
One area of philosophy that is especially interesting to me is metaphysics. Metaphysics is the study of **categories** and **relationships between objects** -- in short, it asks the questions of what is there, what is the nature of thing that exist, and how can we relate those things to each other?

### Fuzzy objects

I'd like to walk through a famous paper in metaphysics concerning what are called "fuzzy objects". What does it mean for an object to be "vague" or "sharp"?

Classically, we could imagine categorizations of things into strict boundaries. Either an object is an apple, or it isn't; either an object is a table, or it isn't. When we look at an object, we think about all of the cateogies of things we have seen in the past -- all of the apples, tables, cats, and more, and try to fit that object into one of these baskets. If we're seeing something we've never seen before, we might invent a new basket -- "unicorn" -- to put the object into. We might even put an object into more than one basket -- that fruit I just saw could probably fit into the "red" basket as well as the "apple" basket.

However, that boundary becomes much less clear with other examples. Imagine we were standing at the base of a mountain, and we are trying to figure out where the mountain "starts". Where should we begin counting what is part of the mountain and what isn't? Is it just when the ground starts getitng higher than that around it? What if the ground starts getting higher, then goes back down, and then goes up again? The metaphysical indeterminacy of what we call the "mountain" perhaps reflects a deeper reality of the world we live in -- physics tells us that the world evolves in a *probabilistic* manner rather than a deterministic one.

The theory of "fuzzy objects" necessarily rejects classical logic. Using the notation of $$\neg$$ to mean "not", it posits that it is possible for an object $$a$$ to belong in category $$a$$, or category $$\neg a$$, or neither $$a$$ nor $$\neg a$$. That part of the ground that we're looking at and trying to fit in the "mountain" or "not mountain" basket could actually fit in a third basket -- "neither part of the mountain nor *not* part of the mountain". In other words, it's possible for an object to "indeterminately" belong to a category; maybe it is part of the mountain, maybe it isn't, but the indeterminacy of this is just a feature of the world.

### Evans' argument against vague objects

A paper in 1978 by philosopher Gareth Evans responded to this argument, and is famous in both its brevity (it's only a page long) and its seemingly watertight argument. Here's the argument:

Let $$a$$ and $$b$$ be singular semantic terms, and $$a=b$$ be of indeterminate truth value.

Let $$\nabla$$ be an operator that expresses indeterminacy. Thus, we can write \
$$(1)\space \nabla(a=b)$$

We also notice that \
$$(2)\stackrel{A}{\times}[\nabla(x=a)]b$$, \
for some property $$\stackrel{A}{\times}$$ ascribed to $$b$$.

However, we can also state \
$$(3)\space\neg\nabla(a=a)$$,

and therefore \
$$(4)\space\neg\stackrel{A}{\times}[\nabla(x=a)]a$$.

By Leibniz' law, (2) and (4) gives us that \
$$(5)\space \neg(a=b)$$,\
which gives us a contradiction with (1), namely that $$a$$ and $$b$$ are not indeterminately identical to each other. 

Therefore, $$a$$ and $$b$$ are definitely distinct. $$\square$$

(Evans, 1978)

### What does that mean?
When written in the language of formal logic, this argument is basically incomprehensible unless you have seen all of these symbols before. However, the argument is actually not that complicated: here it is translated to regular language.

(1) Let's assume $$a$$ and $$b$$, which are two random objects, are indeterminately identical. This is going to be a proof by contradiction. \
(2) Then, we can say $$b$$ has the property of being such that it is indeterminate whether it is equal to $$a$$. In other words, one of the properties that $$b$$ has is that we don't know whether it is identical to $$a$$. \
(3) However, does $$a$$ have that same property? It shouldn't -- logically, $$a$$ should always be determinally identical to itself, regardless of $$b$$ or anything else. \
(4) Therefore, $$a$$ and $$b$$ do not share the same properties, and if two objects do not share the same properties, they must be distinct. \
(5) Thus, it is not indeterminate whether $$a=b$$; they are definitely different.

### So... there are no fuzzy objects?

Not quite. Evans' argument deconstructs the "vague objects" premise via classical logic. But, if we've learned anything from things like quantum mechanics, it's that we can't use classical tools to approach non-classical theories. The existence of fuzzy objects demands a kind of "fuzzy logic" to accompany it, which is a whole other topic that is beyond the scope of both this article and my own understanding of formal logic. However, this iterative development of theories -- both of language, and of the world broadly -- is something that happens all of the time. Quantum computing can break classical encryption schemes like [RSA](https://en.wikipedia.org/wiki/RSA_(cryptosystem)) using [Shor's algorithn](https://en.wikipedia.org/wiki/Shor%27s_algorithm), but in response we would develop [quantum encryption algorithms](https://en.wikipedia.org/wiki/Quantum_cryptography) that would be even *harder* to crack.

I like this argument as an example of the kind of fun analytical games that get played in formal logic and metaphysics. Another instance of this is the [Nelson-Grelling Paradox](https://en.wikipedia.org/wiki/Grelling%E2%80%93Nelson_paradox), which is another example of how it's not so easy to classify objects into either category $$a$$ or category $$\neg a$$ when examining the words "autological" and "heterological". It's also another great piece of evidence supporting the fact that language, and our deployment of it, is not so simple. Even the question of "what is a mountain?" gives rise to a host of fascinating thought experiments, to which there are certainly no easy explanations.
