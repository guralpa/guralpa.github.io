---
layout: page
title: fib-functor
description: mathematics formalization
img: assets/img/fib-functor-cover.png
importance: 1
category: work
related_publications: true
---

The natural numbers, with unique morphisms *n* -> *m* whenever *n* divides *m*, is an example of an abstract mathematical structure called a category. The Fibonacci sequence, viewed as a function, is an example of a functor on this category. The 'Fibonacci Entry Sequence', defined for each natural number *n* to be the smallest number *k* such that *n* divides *F(k)*, is also a functor, and is in fact the left adjoint of the Fibonacci Functor. 

My work began with instantiating the category structure on the natural numbers, and the functor structure on the fibonacci sequence. From there, I defined the Fibonacci Entry Sequence, since it was not already present in Mathlib. The well-definedness of this sequence relies on the fact that the Fibonacci Sequence is periodic modulo a natural number *m*, the most straightforward proof of which utilizes a pigeonhole argument. This was somewhat difficult due to the rigidly formal nature of Lean, but I was able to complete the first half of the argument and am now finalizing the second of two cases in the second half.

At the same time, I set up the category-theoretic arguments necessary to show the adjunction between these two functors, leaving `sorry`'s where a number-theoretic property was necessary. It turns out that showing the existence of a left adjoint of the Fibonacci Functor is *more difficult* than showing that the Fibonacci Entry Functor is, in fact, the left adjoint, so that is what I ended up doing. This is also a work in progress at the moment.