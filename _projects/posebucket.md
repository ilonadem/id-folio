---
layout: page
title: Devices for at-home motion analysis
description: Building a medical device for at-home motion capture analysis (Michael Brenner Lab)
img: assets/img/posenet.png
# redirect: https://unsplash.com
importance: 2
category: internships/research
---

**Goal:** Build a device capable of monitoring the movements of patients at home.

**Motivation:** Researchers at Boston Children's Hospital are developing drugs for treating neurodegenerative diseases at the invidivudal level. Testing the efficacy of such treatments is difficult because it is impossible to conduct large-scale clinical trials, and it is unfeasible to have patients come in every month to perform detailed motion-lab analysis. Furthermore, for privacy reasons these devices cannot store any video data for patients, and must perform instead perform immedeate pose analysis.

**Method:** There are several aspects of this project that we are focusing on:
- fine-tuning existing pose models to better fit patients with movement abnormalities
- determining which pose information correlates with disease progress
- setting up a data pipeline for regularly uploading motion information to the cloud (and accounting for potential crashes or device restarts)

**Code:** <a href="https://github.com/ilonadem/posebucket">PoseBucket Github repo</a> (at the moment very bare-bones, as we are still developing the fine-tuned model)

We are currently deploying our model on a  <a href="https://coral.ai/">Google coral device</a> and fine-tunning a <a href="https://github.com/ilonadem/project-posenet">PoseNet model</a> by comparing to time-series data taken in Harvard's 3D motion capture lab. 