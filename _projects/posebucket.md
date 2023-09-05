---
layout: page
title: pose from home
description: Building a medical device for at-home motion capture analysis to track neurodegenerative diseases (Brenner Lab)
img: assets/img/coral2.jpg
# redirect: https://unsplash.com
importance: 1
category: internships/research
---
Project with Prof. Brenner at Harvard and clinicians at Boston Children's Hospital + Mass General Hospital

<!-- <centering>
    <image src="assets/img/security_preserving_data_pipeline.png" width="250" /> 
</centering> -->

 <div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <centering>
        {% include figure.html path="assets/img/security_preserving_data_pipeline.png" title="Coral Demo" class="img-fluid rounded z-depth-1" %}
    </centering>
    </div>
</div>

**Abstract:** 

Children with neurodegenerative diseases are home- bound and cannot make regular office visits. This is prohibitive for running clinical trials for testing novel and potentially life-saving treatments.
- Want a compact device that replicates motion capture lab gait analysis for use in neurological assessment settings.
- Current use case: n-of-1 clinical trial for a Dentatorubral Pallidoluysian Atrophy (DRPLA) treatment at Boston Children’s Hospital.
- To do this, need to benchmark existing human pose estimation (HPE) models and determine a minimum frame resolution for gait analysis.

**Method Overview:**

- We are developing a method for performing neurological gait assessments of patients from the comfort of their own homes. To do this, we deploy a compressed human pose estimation model on a TinyML device (Google Coral dev board) connected to a USB camera.
- The device sends 24-hour keypoint time-series data to an encrypted cloud server without saving any video.
- The device costs $100 to make and is not a wearable, instead installed somewhere in a patient’s home.

 <div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <center>
        {% include figure.html path="assets/img/animation.gif" title="Coral Demo" class="img-fluid rounded z-depth-1" width="250" %}
    </center>
    </div>
</div>

**Pose Models Used:**
- PoseNet
- PoseNet .tflite (model on the device)
- MoveNet Thunder
- MoveNet Lightning
- OpenPose (pending)


