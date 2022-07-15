---
layout: page
title: encrypted image models
description: Homomorphic Encryption for image models using Microsoft's SEAL library
img: assets/img/tenseal.png
importance: 2
category: internships/research
---
*[Project for Disney Research Studios]*

**Goal:** Encrypt sensitive image data in a way that allows for training models on powerful but potentially insecure cloud servers.

**Motivation:** Homomorphic encryption (HE) is an encryption technique that encrypts data in a way that allows for operarations on the encrypted data whose decrypted result is identical to what we would have gotten had we performed these operations on the original data to begin with. 

**TLDR:** I am running several experiments:
- fully encrypted training using the CKKS encryption scheme on a simple autoencoder
- training a regular autoencoder with a subset of the model layers being encrypted (via the CKKS encryption scheme)
- encrypting data and labels as a preprocessing step and training standard pytorch-based models that work on both encrypted and unencrypted data

**Code:** quite proprietary :")
