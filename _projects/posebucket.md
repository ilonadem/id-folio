---
layout: page
title: pose from home
description: Building a medical device for at-home motion capture analysis to track neurodegenerative diseases (Brenner Lab)
img: assets/img/coral2.jpg
# redirect: https://unsplash.com
importance: 1
category: internships/research
---
*[Project with Prof. Brenner at Harvard and doctors at Boston Children's Hospital]*

**Goal:** Build a device capable of monitoring the movements of patients at home.

**Motivation:** Researchers at Boston Children's Hospital are developing drugs for treating neurodegenerative diseases at the invidivudal level. Testing the efficacy of such treatments is difficult because it is impossible to conduct large-scale clinical trials, and it is unfeasible to have patients come in every month to perform detailed motion-lab analysis. Furthermore, for privacy reasons these devices cannot store any video data for patients, and must perform instead perform immedeate pose analysis.

**Method:** There are several aspects of this project that we are focusing on:
- fine-tuning existing pose models to better fit patients with movement abnormalities
- determining which pose information correlates with disease progress
- setting up a data pipeline for regularly uploading motion information to the cloud (and accounting for potential crashes or device restarts)

**Code:** <a href="https://github.com/ilonadem/posebucket">PoseBucket Github repo</a> (at the moment very bare-bones, as we are still developing the fine-tuned model)

We are currently deploying our model on a  <a href="https://coral.ai/">Google coral device</a> and fine-tunning a <a href="https://github.com/ilonadem/project-posenet">PoseNet model</a> by comparing to time-series data taken in Harvard's 3D motion capture lab. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <center>
        {% include figure.html path="assets/img/coral.jpg" title="coral1" class="img-fluid rounded z-depth-1" %}
    </center>
    </div>
</div>
<div class="caption">
    poseing in the lab!
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <center>
        {% include figure.html path="assets/img/motioncapture.jpg" title="coral1" class="img-fluid rounded z-depth-1" %}
    </center>
    </div>
</div>
<div class="caption">
    poseing in Harvard's motion capture lab!
</div>