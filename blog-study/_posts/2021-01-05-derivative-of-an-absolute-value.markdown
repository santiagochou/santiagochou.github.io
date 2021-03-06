---
layout: post
title:  "Derivative of an Absolute Value"
date:   2021-01-05 18:56:24
category: study
---

###### Tips：Use “\lvert，\rvert and \vert” to present the absolute value notations.

### Explanation:

absolute value function like  $ y=\lvert x-2 \rvert $ \\
can be written like this: $y=\sqrt{(x-2)^2}$

### apply differentiation:

$$
 y' = \cfrac{2(x-2)}{2 \sqrt{(x-2)^2}} \to power\ rule  \tag {1}
 $$

### simplify,

$ y' = \cfrac{x-2}{\lvert x-2 \rvert}$  where $x \neq 2 $ \\
so in general $ \cfrac{d}{dx}u=\cfrac{u}{\lvert u \rvert} \cdot \cfrac{du}{dx}$

### For Derivative (1)

For the function of  $y=\sqrt{(x-2)^2}$ 

Let $W=(x-2)^2$, then $y'=W' \cdot \cfrac{1}{2} \cdot \cfrac{1}{W^\frac{1}{2}}$

We now solve the $W'$

Let $V=x-2$ , so, the solution of the $W'$ is $W' = V' \cdot 2 * V$.

We know that $V'=1$ , $W=(x-2)^2$ and $V=x-2$.

Finally. We get the solution of the $y'$, which is \\
$ y' = 1 \cdot 2 \cdot (x-2) \cdot\frac{1}{2} \cdot \cfrac{1}{\sqrt{(x-2)^2}} $

Equally, $y' = \cfrac{x-2}{\lvert x-2 \rvert}$

## 一点感想：

导数就表征原函数的瞬时变化率。所以其**x轴的位移与伸缩**和**y轴的位移与伸缩**并不影响其总体趋势，例如，$\cfrac{d}{dx}\{ln(2 \cdot \lvert x -1 \rvert ) \}$ 与 $\cfrac{d}{dx}\{ln(\lvert x \rvert ) \}$ 图像基本相似，而且其 $y$ 轴右侧的图像就与$\{ln(x)\}'$ 一样，其导数为 $\cfrac{1}{x}$ 。所以整体上的变化规律与 $\cfrac{1}{x}$ 一致。事实上，

$\cfrac{d}{dx}\{ln(2 \cdot \lvert x -1 \rvert ) \} = \cfrac{1}{x-1}$