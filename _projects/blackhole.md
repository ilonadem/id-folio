---
layout: page
title: visualizing black holes
description: Producing black hole images from event horizon telescope data (APMTH216 final project)
img: assets/img/blackhole.png
importance: 3
category: coursework
blackhole_pdf: 
---

**Goal:** Reconstruct images of the black hole from VLBI data collected by the Event Horizon Telescope.

**Motivation:** Black holes are difficult to image not only because they absorb all visible light, but because they are also located at such great distances away from earth. At observable wavelengths, standard telescopes are not powerful enough to resolve them.

VLBI (very long baseline interferometry) is a technique designed to handle this problem. It combines measurements taken by arrays of telescopes positioned at distances away from each other all around earth, and measures the Fourier components of the sky image on baselines between the telescopes.

The current challenge to interepret these VLBI images and reconstruct an optimal image. More specifically, given a set of sparse measurements, there are infinitely many possible images in the image domain that could produce the sparsely sampled data in the Fourier domain. 

**TLDR:** We explored two algorithms:
- CLEAN: the standard deconvolution algorithm 
- RML (regularized maximum likelihood): this uses a Bayesian model inversion approach, and is powerful because we can incorporate different effects (atmospheric pressure, systematic gain errors, thermal noise).

We added a spin on the standard formulations of these algorithms in our implementations:
- Bispectral data: Using bispectral data for RML (triple products of visibilites, or closure phases), motivated by the successes of the CHIRP algorithm, which also considered bispectral data
- Inverse fourier transform methods: comparing the <a href="https://docs.scipy.org/doc/scipy/tutorial/fft.html">fast fourier transform</a>  and the <a href="https://pythonhosted.org/pyNFFT/tutorial.html"> pynfft fourier transform</a> libraries
- Regularizers: implementing different regularizers in the RML algorithm

**Code:** <a href="https://drive.google.com/file/d/1d-CVcmU2d-tRviDdxkarW_0FlF4vn-ES/view?usp=sharing"> project writeup</a>
