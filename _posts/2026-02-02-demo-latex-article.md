---
layout: post
title: "Demo: A LaTeX-first note on optimization"
---

This is a short, fake article meant to show how math renders.

## Setup

We want to minimize a smooth function $f(\theta)$ with gradient $\nabla f(\theta)$.
A common update is

$$
\theta_{t+1} = \theta_t - \eta \nabla f(\theta_t)
$$

where $\eta$ is a step size.

## A tiny derivation

Assume $f$ is $L$-smooth. Then

$$
\|\nabla f(\theta) - \nabla f(\phi)\| \le L \|\theta - \phi\|.
$$

This implies a standard descent lemma and motivates small step sizes.

## Pseudocode

```python
# gradient descent
for t in range(T):
    theta = theta - eta * grad_f(theta)
```

## Takeaway

LaTeX equations, inline math like $\alpha$ and $\beta$, and code blocks all render cleanly.
