---
title: Leveraging Dale’s Principle as an Inductive Bias in Recurrent Neural Networks
date: 2026-09-27
publication_types: [paper-conference]
publication: 'NeurIPS 2026 · Accepted'
publication_short: NeurIPS 2026
featured: true
weight: 2
authors:
  - admin
  - Chenxiao Yang
  - Yujia Zhao
  - Jingzhao Zhang
  - Lu Mi
# Add public paper/code links when available.
summary: 'Learnable excitatory–inhibitory separation improves recurrent learning stability, continual learning, and reinforcement learning control.'
tags: [Reinforcement Learning, Continual Learning, NeuroAI]
method: EISep
research_focus: Stable learning & control
teaser:
  image: eisep-teaser.png
  alt: 'Simple and EISep recurrent networks before and after training. EISep neurons have exclusively excitatory or inhibitory outputs, with learnable neuron identities.'
  caption: 'Figure 1: EISep learns excitatory–inhibitory neuron identities while preserving Dale’s principle.'
---

## A biological principle for more stable learning

Biological neurons send either excitatory or inhibitory outputs. **EISep RNN** incorporates this constraint, known as Dale’s principle, into recurrent networks while allowing each neuron’s excitatory or inhibitory identity to be learned.

## Method

The architecture combines a learnable sign assignment using Gumbel–Softmax. These choices let the network adapt its excitatory–inhibitory organization during training while improving optimization stability.

## Experimental findings

- **Multi-task learning:** competitive performance on a 20-task cognitive benchmark, with more stable gradients and recurrent dynamics.
- **Continual learning:** reduced task interference and stronger resistance to catastrophic forgetting across sequential cognitive tasks.
- **Reinforcement learning:** improved recurrent advantage actor–critic performance on Lunar Lander and HalfCheetah, covering discrete and continuous control.
- **Interpretable structure:** sparse, modular connectivity emerges from the excitatory–inhibitory constraint.

## Research connection

Reliable policy learning depends on stable optimization and representations that can be reused across tasks. This work explores architectural inductive biases for those properties.
