---
layout: page
title: surrogate modeling
description: Surrogate models for faster SPICE and PWL simulation of power supply circuits
img: assets/img/pspice.jpg
importance: 5
category: internships/research
---
*[Internship project for Cadence Design Systems]*

**Goal:** Automate the development of surrogate models for generic power supply circuits based on SPICE simulation data.

**Motivation:** As the race to build smaller and more powerful computer chips continues, Moore's Law is starting to give out as we brush up against quantum limits. As a result, we can no longer rely on the one-size-fits-all principle, and must increasingly build customized chips and computer boards for specific tasks. Given a set of tech specs, the goal is to come up with an optimal schema by searching over simulation outputs from possible schemas. To do so, we need to come up with a way to simulate the circuit outputs of possible schemas, a nontrivial task that requires solving nonlinear differential equations. 

Simulating high performance computing circuit boards is often non-convergent or prohibitively computationally expensive. The goal is to model SPICE (simulation program with IC emphasis) simulations quickly and accurately via surrogate models. 

**Code:** proprietary :'), but this project contained a lot of:
- python wrapped C++ of SPICE model simulation outputs
- <a href="https://github.com/ray-project/ray">Ray</a> parallelization infrastructure
- virtual machines