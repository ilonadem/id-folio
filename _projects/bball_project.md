---
layout: page
title: basketball pose analysis
description: Detecting and analyzing human pose throughout freethrow motion
img: assets/img/bball.jpg
importance: 2
category: internships/research
---

**Goal:** Build an application that analyzes basketball free throws from input smartphone video. 

**Motivation:** We were approached by an NBA client for basketball analysis applications for both players and fans.

**Method:** There were three parts to this implementation
1. Identifying human pose markers, basketball hoop, and basketball
2. Classifying freethrow start and whether ball successfully went through hoop
3. Estimating freethrow statistics (e.g. release angle, shot angle, bounce)

We fine-tuned Facebook's <a href="https://github.com/facebookresearch/detectron2">Detectron2 model</a> as well as trained our own model on an internal dataset of annotated ball and hoop images in MSCOCO format. We next developed several heuristics for classifying the success of the shot as well as player stats.

An interesting extension of this project would be mapping the video to a well-known player, or giving suggestions (the literature suggests that the release angle is highly correlated with the success of the shot).

**Code:** proprietary :')

But here is a fun demo (of me) being analyzed:
