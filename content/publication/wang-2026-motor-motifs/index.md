---
title: Learning Reusable Motor Motifs for Continuous Animal Behavior Modeling
date: 2026-09-27
publication_types: [paper-conference]
publication: 'NeurIPS 2026 · Accepted'
publication_short: NeurIPS 2026
featured: true
weight: 1
authors:
  - admin
  - Jingyang Ke
  - Bo Dai
  - Anqi Wu
# Add public paper/code links when available.
summary: 'Discovering reusable motor motifs from offline behavior data and composing them into continuous, interpretable policies.'
tags: [Imitation Learning, Skill Discovery, Behavior Modeling]
method: MCD
research_focus: Reusable motor skills
teaser:
  image: motor-motifs-teaser.png
  alt: 'Side grooming illustrated as a combination of a grooming motif and a turning-side motif.'
  caption: 'Figure 1: complex behaviors emerge from combinations of reusable motor motifs.'
---

## Learning the building blocks of behavior

Complex movements often combine simpler components: an animal can turn while grooming, or sniff while moving forward. **Motif-based Continuous Dynamics (MCD)** learns these reusable motor motifs directly from behavioral trajectories and models behavior as smoothly changing combinations of them.

## Method

- **Learn from offline trajectories.** Use transition-based spectral representation learning to discover a shared basis for dynamics, policies, and rewards.
- **Compose skills continuously.** Represent behavior through time-varying motif weights, allowing multiple motifs to be active together.
- **Infer policies and reward structure.** Connect the learned representation to maximum-entropy policies and inverse reinforcement learning.

## Experimental findings

Evaluated on simulated gridworlds, maze navigation, and real animal behavior data. On the animal behavior benchmark, MCD outperforms Keypoint-MoSeq, SemiSeg, and OPAL in human-annotated behavior decoding accuracy and trajectory discrimination AUC. The learned motifs capture both transitions and simultaneous movements, such as locomotion and sniffing.

## Research connection

This work studies how reusable, compositional skills can be extracted from observed behavior. It informs my broader interest in learning embodied skills from demonstrations. The experiments in this paper concern simulated tasks and animal behavior; transferring this approach to human motion and robots is a future research direction.
