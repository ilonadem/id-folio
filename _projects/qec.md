---
layout: page
title: cnn for quantum error correction
description: Using convolutional neural networks to improve quantum error correction on IBM quantum computers (PHY160 final project)
img: assets/img/qec.png
importance: 4
category: coursework
---

**Goal:** Implement a quantum conovlutional neural network that can be used for quantum error correction without logical qubit wavefunction collapse. The goal is to maximize the recovery fidelity of a quantum circuit.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/quantum_error_gate.png" title="HD-Wallet Setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    QCNN (from Cong et al., 2019)
</div>

**Motivation:** Quantum computers present a powerful new computational paradigm, but they currently face many roadblocks such as qubit decoherence and imperfect logical gates. These are usually accounted for by quantum error correction, which designed to correct a single qubit error. Quantum error correction however breaks down for asymmetric errors and correlated errors, which is where QCNNs come in!

A Quantum CNN is a quantum circuit with parametrized untitaries that act as layers in the neural network with an input quantum state $$ \rho_{01}$$

**TLDR:**
We trained a CNN to find an optimal rotation axis over which to perform quantum state reconstruction, and tested our algorithm in a 9 qubit IBM quantum computer.

**Overview:**
We propose to maximize the recovery fideltiy:

\begin{align}
\sum_{\ket\psi_l \in\{\ket{\pm x,y,z}\}}  f_q = \bra \psi_{l} M_{q}^{-1} (N(M_q( \bra\psi_{l} \ket\psi_{l})))\ket\psi_{l}
\end{align}

By optimizing on the following parameters on a 3-qubit system:
1. Axis of rotation
2. Arbitrary unitaries (including both angle of rotation and axis of rotation)
With the goal of correctly classifying all of the +/- Pauli eigenstates

For our purposes, we assumed:
- ideal gates
- bit/phase flip errors happen between the two separators in the middle of the circuit

There were several phases to our experiments:
1. Correcting arbitrary bit flips
2. Correcting bit and phase errors

We corrected for these errors using an arbitrary rotation U3 gate and defined a cost function that evaluated the overlap of an input eigenstate with the state that is outputted by the circuit. Next we performed stochastic gradient descentto optimize the theta paramter that maximized this overlap.


**Code:** link to qiskit notebook