---
title: 'Clutter-Robust Vision-Language-Action Models through Object-Centric and Geometry Grounding'

authors:
  - Khoa Vo
  - Taisei Hanyu
  - Yuki Ikebe
  - Trong Thang Pham
  - Nhat Chung
  - Minh Nhat Vu
  - Duy Nguyen Ho Minh
  - Anh Nguyen
  - Anthony Gunderman
  - Chase Rainwater
  - Ngan Le

publishDate: '2025-12-27T00:00:00Z'

publication: 'arXiv preprint (2025), under submission at IEEE Transactions on Robotics (T-RO)'

abstract: ''

summary: 'OBEYED-VLA disentangles perceptual grounding from action reasoning to improve robustness in cluttered real-world robotic manipulation.'

tags:
  - Vision-Language-Action Model
  - Robotic Manipulation
  - arXiv

featured: true

url_preprint: 'https://arxiv.org/abs/2512.22519'
url_code: 'https://github.com/UARK-AICV/OBEYED_VLA'
url_project: 'https://uark-aicv.github.io/OBEYED_VLA/'
url_pdf: 'https://arxiv.org/pdf/2512.22519'
url_poster: ''
url_slides: ''

image:
  focal_point: ''
  preview_only: true

projects: []

slides: ""
---

## Overview

Recent Vision-Language-Action models have made strong progress by post-training large Vision-Language Models for action prediction, but many still entangle perception and control in a single monolithic pipeline. In practice, that weakens language-conditioned grounding: policies may over-grasp when the target is absent, drift toward clutter, or overfit to background appearance. OBEYED-VLA addresses this by explicitly separating perceptual grounding from action reasoning before control.

## TL;DR

- **Status:** Under submission at IEEE Transactions on Robotics (T-RO).
- **Problem:** Monolithic VLAs can erode language-conditioned grounding, leading to failure in clutter, absent-target cases, background shifts, and unseen-object manipulation.
- **Method:** OBEYED-VLA disentangles perception from control by grounding multi-view inputs into task-conditioned object-centric and geometry-aware observations before VLA action prediction.
- **Key result:** On a real-world UR10e tabletop setup, the method improves robustness over strong VLA baselines across distractor-heavy, absent-target, background-shift, and unseen-object regimes.

## Qualitative Result: Cluttered Scenes with Distractor Objects

<div style="display: flex; justify-content: center; margin: 1.5rem 0;">
  <img src="distractor_demo.gif" alt="OBEYED-VLA distractor-scene demo" style="width: 100%; max-width: 900px; height: auto; border-radius: 6px;">
</div>

In this distractor-scene example, the grounded observations suppress irrelevant objects and preserve the task-relevant target, helping the executor stay aligned with the instruction instead of drifting toward visually salient clutter.

## Project Page

For the full method, additional videos, and quantitative experiments, see the [OBEYED-VLA project page](https://uark-aicv.github.io/OBEYED_VLA/).
