---
layout: page
title: pose from home
description: Building a medical device for at-home motion capture analysis to track neurodegenerative diseases (Brenner Lab)
img: assets/img/coral2.jpg
# redirect: https://unsplash.com
importance: 1
category: internships/research
---
<center>
*[Project with Prof. Brenner at Harvard and doctors at Boston Children's Hospital]*
</center>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <center>
        {% include figure.html path="assets/img/animation.gif" title="Coral Demo" class="img-fluid rounded z-depth-1" %}
    </center>
    </div>
</div>
<div class="caption">
    Human, as seen through keypoint analysis.
</div>

**Goal:** Build a device capable of monitoring the movements of patients at home.

**Motivation:** Continuous monitoring of patients in clinical trials has the potential to revolutionize the field of medicine and drug discovery. For privacy reasons, devices for doing this cannot store any video data for patients, and must instead perform immedeate pose analysis.

**Method:** There are several aspects of this project that we are focusing on:
- fine-tuning existing pose models to better fit patients with movement abnormalities
- determining which pose information correlates with disease progress
- setting up a data pipeline for regularly uploading motion information to the cloud (and accounting for potential crashes or device restarts)

**Code:** <a href="https://github.com/ilonadem/posebucket">PoseBucket Github repo</a> (at the moment very bare-bones, as we are still putting finishing touches on our models and filling out proper documentation etc.)

We are currently deploying our model on a  <a href="https://coral.ai/">Google coral device</a> and fine-tunning a <a href="https://github.com/ilonadem/project-posenet">PoseNet model</a> by comparing to time-series data taken in Harvard's 3D motion capture lab. The device is set to be used in an upcoming funded clinical trial for a neurodogenerative disease treatment drug. 

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
    Poseing in Harvard's motion capture lab! We used 3d motion capture lab data to finetune the 2d pose estimation models on our device. 
</div>