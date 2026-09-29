---
title: Inverse Reinforcement Learning with Switching Rewards and History Dependency
  for Characterizing Animal Behaviors
authors:
- Jingyang Ke
- Feiyang Wu
- admin
- Jeffrey Markowitz
- Anqi Wu
date: '2025-01-01'
publishDate: '2025-06-19T12:09:25.041378Z'
publication_types:
- paper-conference
publication: 'Proceedings of the 42nd International Conference on Machine Learning (ICML), 2025'
publication_short: ICML 2025
featured: true
weight: 3
method: SWIRL
research_focus: Learning behavioral intentions
teaser:
  image: swirl-model.png
  alt: 'SWIRL graphical model linking hidden modes, actions, and states over time, with state-dependent mode transitions and history-dependent actions.'
  caption: 'Figure 1: SWIRL models changing goals and history-dependent actions.'
summary: 'Recovering time-varying, history-dependent rewards from long behavioral trajectories with switching inverse reinforcement learning.'
tags: [Inverse Reinforcement Learning, Reward Inference, Behavior Modeling]
url_pdf: /publication/ke-2025-inverse/paper.pdf
url_code: https://github.com/BRAINML-GT/SWIRL
links:
  - name: Proceedings
    url: https://proceedings.mlr.press/v267/ke25b.html
---

## Inferring the intentions behind behavior

**SWIRL (Switching Inverse Reinforcement Learning)** infers changing goals from behavioral trajectories. It models long sequences as transitions between hidden decision-making modes, each with its own reward function and policy.

## Method

- **Goal switching:** transitions between hidden modes depend on the previous mode and the animal’s current state.
- **Behavioral memory:** rewards and policies can depend on recent states, capturing how past experience shapes actions.
- **Joint inference:** expectation–maximization alternates between inferring behavioral modes and learning their transitions, rewards, and policies.

## Experimental findings

- **Gridworld:** combining both levels of history dependence improves reward recovery and behavioral segmentation.
- **Mouse navigation:** recovers interpretable water-seeking, home-seeking, and exploration modes in a 127-node labyrinth.
- **Spontaneous behavior:** outperforms autoregressive HMM baselines in held-out likelihood. State-dependent switching helps, while adding action-level history does not improve this dataset.

## Research connection

This work connects learning from demonstrations with interpretable reward inference, offering a way to study changing intentions under the complicated behavior.
