---
layout: page
title: hierarchical determinisitc wallets
description: Hierarchical deterministic wallet implementation for secure crypto holding platform
img: assets/img/hd-wallet.png
importance: 5
category: internships/research
---

*[Project for Dreams-AI, a UK-based startup]*

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hd-wallet.png" title="HD-Wallet Setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example setup of a hierarchical determinstic wallet for bitcoin addresses.
</div>

**Goal:** Create a secure crypto depositing scheme, in which users deposit cryptocurrency by sending money to the public address associated with their account in our system. 

**Motivation:** This project came about in the midst of the crypto boom of summer 2020. Our client was facing a lot of issues with security and deposits and wanted to build a cryptocurrency deposit framework to standardize everything. Long-term there was also the motivation of becoming a crypto lending platform.

**TLDR:**
I worked on several parts of this project, which was on an accelerated timeline because of security issues with our client:
1. Coming up with an hd-wallet schema, namely a system for generating public/private keys for parent/child addresses in a deterministic but secure way
2. Minimizing the overall number of transactions executed on the blockchain (to save on gas fees)
3. Integrating schema with the existing system and making it generalizable to other clients
4. Connecting a frontend that can interface with the backend, which was executing everything on the blockchain

Results
- successful testing and demo on ropsten test network
- successful deployment of deposit schema within 2 months on ERC chain

**Code:** proprietary :')
