---
layout: post
title: "Muon: An optimizer for hidden layers in neural networks"
---

Muon is a placeholder name for an optimizer that targets hidden-layer updates.
The goal is to illustrate card layout, summaries, and reading-time metadata.

We can define a generic update:

$$
W_{t+1} = W_t - \eta \nabla_W \mathcal{L}(W_t)
$$

and compare variants under the same step size budget.
