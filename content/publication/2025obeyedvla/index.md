---
title: 'Clutter-Resistant Vision-Language-Action Models through Object-Centric and Geometry Grounding'

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

summary: 'OBEYED-VLA improves robotic manipulation robustness in cluttered real-world scenes by grounding perception before action.'

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

Recent Vision-Language-Action models often perform well on clean demonstrations but become brittle once the scene contains distractors, missing targets, background shifts, or unseen objects. OBEYED-VLA addresses that failure mode by separating perceptual grounding from action prediction: it first identifies the task-relevant object regions, then emphasizes their geometry, and only then feeds those grounded observations into the control policy.

## TL;DR

- **Status:** Under submission at IEEE Transactions on Robotics (T-RO).
- **Problem:** End-to-end VLAs often lose reliable language-vision grounding in clutter, absent-target cases, background shifts, and unseen-object scenes.
- **Method:** OBEYED-VLA combines VLM-based object-centric grounding with masked-depth geometric grounding before action prediction.
- **Key result:** The model stays focused on the instructed object under heavy clutter and generalizes better than strong VLA baselines across multiple real-world failure modes.

## Qualitative Result: Cluttered Scenes with Distractor Objects

<div style="display: flex; justify-content: center; margin: 1.5rem 0;">
  <img src="distractor_demo.gif" alt="OBEYED-VLA distractor-scene demo" style="width: 100%; max-width: 900px; height: auto; border-radius: 6px;">
</div>

In this distractor-scene example, the grounded observations suppress irrelevant objects and preserve the task-relevant target, allowing the policy to stay aligned with the instruction instead of drifting toward visually salient clutter.

## Project Page

For the full method, additional videos, and quantitative experiments, see the [OBEYED-VLA project page](https://uark-aicv.github.io/OBEYED_VLA/).
