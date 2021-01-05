<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
        }
    });
</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript">
</script>
---
layout: post
title:  "Derivative of an Absolute Value"
date:   2021-01-05 18:56:24
category: study
---

#### Explanation:
absolute value function like  $ y=|x-2| $
can be written like this: $y=\sqrt{(x-2)^2}$

#### apply differentiation:

$ y' = \cfrac{2(x-2)}{2 \sqrt{(x-2)^2}} \to power\ rule  \tag {1}$

#### simplify,

$ y' = \cfrac{x-2}{|x-2|}$  where $x \neq 2 $
so in general $ \cfrac{d}{dx}u=\cfrac{u}{|u|} \cdot \cfrac{du}{dx}$

#### For Derivative (1)

For the function of  $y=\sqrt{(x-2)^2}$

Let $W=(x-2)^2$, then $y'=W' \cdot \cfrac{1}{2} \cdot \cfrac{1}{W^\frac{1}{2}}$

We now solve the $W'$

Let $V=x-2$ , so, the solution of the $W'$ is $W' = V' \cdot 2 * V$.

We know that $V'=1$ , $W=(x-2)^2$ and $V=x-2$.

Finally. We get the solution of the $y'$, which is
$ y' = 1 \cdot 2 \cdot (x-2) \cdot\frac{1}{2} \cdot \cfrac{1}{\sqrt{(x-2)^2}} $

Equally, $y' = \cfrac{x-2}{|x-2|}$