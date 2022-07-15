---
layout: page
title: replacing backprop
description: Synthetic gradients, forward gradients, and random projections for distributed training
img: assets/img/sg-setup.png
importance: 1
category: internships/research
---
*[Project for Disney Research Studios]*

**Goal:** Efficiently training a network on separate resources, some of which you might not necessarily trust. 

**Motivation:** There is a big advantage to distributing training onto cloud-based computing resources, especially for video processing for movies, but this often infeasible because of security concerns. This project investigates novel training and data encryption methods that would make this possible. Namely we investigate two ideas: 
1. replacing standard backpropagation with methods that allow for certain layers of the model to train without any knoweldge of global context or original data
2. breaking a model into pieces and using message passing and synthetic gradients to inform training

<!-- **TLDR:** Writing custom classes and methods in Pytorch for model training alternatives. -->

**Experiment 1: Forward Gradients**

This was inspired by the algorithm as outlined in <a href="https://arxiv.org/abs/2202.08587">this paper</a> and <a href="https://github.com/orobix/fwdgrad">this community implementation</a>. However, I considered several additional things:
1. Implementing custom learning rate optimizers, as inspired by traditional ones (momentum, Nesterov accelerated gradients, adam, RMSprop) but taking into account the random perturbation aspect of gradient estimation.
2. Tuning the number of random projections: this comes at the cost of epoch speed, since each forward pass now has n random projections instead of 1, but preserves the security aspect of training

**Experiment 2: Synthetic Gradients**
This was inspired by the algorithm as outlined in <a href="https://arxiv.org/abs/1608.05343">this Deepmind paper</a> and <a href="https://github.com/koz4k/dni-pytorch">this community implementation</a>. The basic idea is to break your model into pieces, and have each piece start backpropagating based on *another model's estimate* of what the gradients of the last layer should be.

**Code:** proprietary :')
