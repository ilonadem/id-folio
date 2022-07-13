---
layout: page
title: hd wallet
description: Hierarchical deterministic wallet implementation for secure crypto holding platform
img:
importance: 3
category: research
---

Goal: Create a secure crypto depositing scheme, in which users deposit cryptocurrency by sending money to the public address associated with their account in our system. 

I worked on two parts of this project, which was on an accelerated timeline because of security issues with our client:
1. Coming up with an hd-wallet schema and figuring out how to integrate it with the existing system. An additional factor was making this schema generalizable so that we could sell it to other clients as well.
2. Connecting a frontend that can interface with the backend, which was executing everything on the blockchain

Results
- successful testing and demo on ropsten test network
- successful deployment of deposit schema within 2 months on ERC chain

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hd-wallet.png" title="HD-Wallet Setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example setup of a hierarchical determinstic wallet for bitcoin addresses.
</div>

