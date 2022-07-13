---
layout: page
title: At-home posenet
description: At-home pose monitoring on Google Coral device
img: # assets/img/7.jpg
# redirect: https://unsplash.com
importance: 3
category: research
---

Goal: build a device capable of monitoring the movements of patients at home in order to assess the efficacy of neurodegenerative disease treatment.

Researchers at Boston Children's Hospital are developing drugs for treating neurodegenerative diseases at the invidivudal level. Testing the efficacy of such treatments is difficult because it is impossible to conduct large-scale clinical trials, and it is unfeasible to have patients come in every month to perform detailed motion-lab analysis. Furthermore, for privacy reasons these devices cannot store any video data for patients, and must perform instead perform immedeate pose analysis.

There are several aspects of this project that we are focusing on:
- fine-tuning existing pose models to better fit patients with movement abnormalities
- determining which pose information correlates with disease progress
- setting up a data pipeline for regularly uploading motion information to the cloud (and accounting for potential crashes or device restarts)

Github repo: <a href="https://github.com/ilonadem/posebucket">PoseBucket</a>

We are currently deploying our model on a  <a href="https://coral.ai/">Google coral device</a> and fine-tunning a <a href="https://github.com/ilonadem/project-posenet">PoseNet model</a>