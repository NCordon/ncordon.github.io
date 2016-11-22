---
title:  "Vector Space where norms aren't equivalent"
date:   2016-10-02
categories: analysis fourier-series math
---

A week ago, we were asked in Fourier Series class to find a counterexample to prove that norms aren't equivalent in vector space $$L^2(a,b)$$.

The definition for this space is: 

$$L^2(a,b) = \left\{ f\:(a,b)  \rightarrow \mathbb{R} \quad measurable: \int_a^b f^2(x)dx < + \infty \right\}$$

The norm based on the dot product $$<f,g> = \int_a^b f \cdot g$$ is:

$$\|f\|_2 = \sqrt{<f,f>} $$

We can define another norm as: $$ \|f\|_{*} = \int_a^b \lvert f \rvert $$. It's easy to prove that it's a norm.


Let $$f_n: (a,b) \rightarrow \mathbb{R}$$, with $$f_n(x)= e^{nx}$$ for all $$n\in \mathbb{N}$$.

Thus: 

$$ \|f_n\|_2 =  \sqrt{\int_a^b{f_{n}^2}} = \frac{1}{\sqrt{2n}} \cdot e^{n(b-a)} $$

$$ \|f_n\|_{*} = \sqrt{\int_a^b{f_{n}^2}} = \frac{1}{n} \cdot e^{n(b-a)} $$


We remember that for those two norms to be equivalent in $$L^2(a,b)$$ (vector space), there have to be $$\lambda, \delta \in \mathbb{R^{+}}$$, verifying
that: $$ \delta \|f\|_{*} \le \|f\|_2 \le \lambda \|f\|_{*} \quad \forall f\in L^2(a,b)$$.


Therefore:

$$\|f_n\|_{2} \le \lambda \|f_n\|_{*} \Leftrightarrow \lambda\frac{\sqrt{2n}}{n} \ge 1$$

But: 

$$\left\{\frac{\sqrt{2n}}{n}\right\} \rightarrow 0$$

So we arrived at a contradiction.

