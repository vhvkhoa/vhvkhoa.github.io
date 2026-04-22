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

abstract: 'Recent Vision-Language-Action (VLA) models have made impressive progress toward general-purpose robotic manipulation by post-training large Vision-Language Models (VLMs) for action prediction. Yet most VLAs entangle perception and control in a monolithic pipeline optimized purely for action, which can erode language-conditioned grounding. In our real-world tabletop tests, policies over-grasp when the target is absent, are distracted by clutter, and overfit to background appearance. To address these issues, we propose OBEYED-VLA (OBject-centric and gEometrY groundED VLA), a framework that explicitly disentangles perceptual grounding from action reasoning. Instead of operating directly on raw RGB, OBEYED-VLA augments VLAs with a perception module that grounds multi-view inputs into task-conditioned, object-centric, and geometry-aware observations. This module includes a VLM-based object-centric grounding stage that selects task-relevant object regions across camera views, along with a complementary geometric grounding stage that emphasizes the 3D structure of these objects over their appearance. The resulting grounded views are then fed to a pretrained VLA policy, which we fine-tune exclusively on single-object demonstrations collected without environmental clutter or non-target objects. On a real-world UR10e tabletop setup, OBEYED-VLA substantially improves robustness over strong VLA baselines across four challenging regimes and multiple difficulty levels: distractor objects, absent-target rejection, background appearance changes, and cluttered manipulation of unseen objects. Ablation studies confirm that both semantic grounding and geometry-aware grounding are critical to these gains. Overall, the results indicate that making perception an explicit, object-centric component is an effective way to strengthen and generalize VLA-based robotic manipulation.'

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
  preview_only: false

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

![OBEYED-VLA distractor-scene demo](distractor_demo.gif)

In this distractor-scene example, the grounded observations suppress irrelevant objects and preserve the task-relevant target, allowing the policy to stay aligned with the instruction instead of drifting toward visually salient clutter.

## Why It Matters

- Robust object grounding helps when the target is surrounded by distractors.
- Geometry-aware inputs reduce dependence on texture and background appearance.
- The same framework also improves absent-target rejection and unseen-object manipulation.

## Project Page

For the full method, additional videos, and quantitative experiments, see the [OBEYED-VLA project page](https://uark-aicv.github.io/OBEYED_VLA/).
