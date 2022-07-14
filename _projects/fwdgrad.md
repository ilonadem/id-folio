---
layout: page
title: Replacing Backprop 
description: Synthetic gradients, forward gradients, and random projections for distributed training
img: assets/img/sg-setup.png
importance: 1
category: internships/research
---

**Goal:** Efficiently training a network on two separate resources, one of which you might not necessarily trust. 

**Motivation:** Train a network on different machines, some of which might potentially be untrusworthy.

**TLDR:** Mainly testing two ideas for training:
1. Forward gradient
2. Synthetic gradients, or message passing between parts of the model


**Code:** proprietary :')
