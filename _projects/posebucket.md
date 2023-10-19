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

<div class="caption">
    Fig 1. Privacy-preserving data transfer pipeline.
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

**Motion Capture Lab Analysis for Pose Model Benchmarking and Analysis:**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <centering>
        {% include figure.html path="assets/img/MCL_trips.png" title="Coral Demo" class="img-fluid rounded z-depth-1" %}
    </centering>
    </div>
</div>

**Device Installation and Data Capture in Patient Homes and Neurological Clinics:**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <centering>
        {% include figure.html path="assets/img/coral_home.png" title="Coral Demo" class="img-fluid rounded z-depth-1" %}
    </centering>
    </div>
</div>

 <div class="row">
    <div class="col-sm mt-3 mt-md-0">
    <center>
        {% include figure.html path="assets/img/fullanim300_COM.gif" title="Coral Demo" class="img-fluid rounded z-depth-1" width="400" %}
    </center>
    </div>
</div>

<div class="caption">
    Patient keypoint animation.
</div>

**Current Results:**

- Minimum processing requirement of 30fps for resolving individual steps within keypoint data.
- Raw pose model data is insufficient for extracting gait cycles due to noise, but we can resolve strides after filtering out low and high frequency signals.
- Successful deployment of devices in patient’s home, enabling remote collection of patient data. Successful deployment of device data collection in neurological clinic at Boston Children’s.
- Gait signals most resolvable from straight-on and angles<45 degrees, and best when patient motion is unobstructed for several steps.
- Gait analysis presents an interpretable metric for evaluating human pose model accuracy.

**Ongoing + Future Work:**
- Developing gait analysis algorithms for extracting metrics of interest (step time, step size, center of mass motion).
- Determining whether compact pose models at device
frame rates (necessary for TinyML devices) are sufficient for resolving gait metrics with clinical accuracy.
- Combining keypoint signals from multiple cameras to augment data into 3D for spatiotemporal gait metrics.
- Benchmarking and fine-tuning existing pose models for increased accuracy for knee, hip joint estimation.
- Continuing data collection in ongoing Nof1 drug development trial. Tracking changes in gait over time and separating patient signal from other household members.
- Pushing on-device processing speeds for increased accuracy.

**Pose Models Used:**
- PoseNet
- PoseNet .tflite (model on the device)
- MoveNet Thunder
- MoveNet Lightning
- OpenPose (pending)

***References***

1. Lukasz Kidzinski, B. Yang, J. L. Hicks, A. Rajagopal, S. L. Delp, and M. H. Schwartz, “Deep neural networks enable quantitative movement analysis using single-camera videos,” Nature Communications, vol. 11, 12 2020.
2. S. Tsuji, “Chapter 41 - dentatorubral–pallidoluysian atrophy,” in Ataxic Disorders (S. H. Subramony and A. Du ̈rr, eds.), vol. 103 of Handbook of Clinical Neurology, pp. 587– 594, Elsevier, 2012
3. M. G. D’Angelo, M. Berti, L. Piccinini, M. Romei, M. Guglieri, S. Bonato, A. Degrate, A. C. Turconi, and N. Bresolin, “Gait pattern in duchenne muscular dystrophy,” Gait posture, vol. 29, no. 1, pp. 36–41, 2008.
4. R. David, J. Duke, A. Jain, V. Janapa Reddi, N. Jeffries, J. Li, N. Kreeger, I. Nappier, M. Natraj, T. Wang, et al., “Tensorflow lite micro: Embedded machine learning for tinyml systems,” Proceedings of Machine Learning and Systems, vol. 3, pp. 800–811, 2021.
5. C. E. Zheng, W. Wu, C. Chen, M. Shah, C. Zheng, T. Yang, S. Zhu, J. Shen, and N. Kehtarnavaz, “Deep learning-based human pose estimation: A survey; deep learning- based human pose estimation: A survey,” J. ACM, vol. 37, 2018.