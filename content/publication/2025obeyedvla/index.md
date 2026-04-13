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

publication: 'arXiv preprint (2025)'

abstract: 'Recent Vision-Language-Action (VLA) models have made impressive progress toward general-purpose robotic manipulation by post-training large Vision-Language Models (VLMs) for action prediction. Yet most VLAs entangle perception and control in a monolithic pipeline optimized purely for action, which can erode language-conditioned grounding. In our real-world tabletop tests, policies over-grasp when the target is absent, are distracted by clutter, and overfit to background appearance. To address these issues, we propose OBEYED-VLA (OBject-centric and gEometrY groundED VLA), a framework that explicitly disentangles perceptual grounding from action reasoning. Instead of operating directly on raw RGB, OBEYED-VLA augments VLAs with a perception module that grounds multi-view inputs into task-conditioned, object-centric, and geometry-aware observations. This module includes a VLM-based object-centric grounding stage that selects task-relevant object regions across camera views, along with a complementary geometric grounding stage that emphasizes the 3D structure of these objects over their appearance. The resulting grounded views are then fed to a pretrained VLA policy, which we fine-tune exclusively on single-object demonstrations collected without environmental clutter or non-target objects. On a real-world UR10e tabletop setup, OBEYED-VLA substantially improves robustness over strong VLA baselines across four challenging regimes and multiple difficulty levels: distractor objects, absent-target rejection, background appearance changes, and cluttered manipulation of unseen objects. Ablation studies confirm that both semantic grounding and geometry-aware grounding are critical to these gains. Overall, the results indicate that making perception an explicit, object-centric component is an effective way to strengthen and generalize VLA-based robotic manipulation.'

summary: 'OBEYED-VLA improves robotic manipulation robustness by grounding VLA perception in task-relevant objects and geometry.'

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

projects:
  - example

slides: example
---

## TL;DR

- **Problem:** End-to-end VLAs often lose reliable language-vision grounding in real clutter, absent-target cases, background shifts, and unseen-object scenes.
- **Idea:** OBEYED-VLA decouples perception from control using frozen VLM-based object-centric grounding plus masked-depth geometric grounding, then fine-tunes a VLA only on clean single-object demonstrations.
- **Results:** OBEYED-VLA improves robustness across clutter, absent-target rejection, background appearance changes, and unseen-object manipulation, with ablations showing that both semantic and geometry-aware grounding are critical.

## Project Page

See the full project page for the method overview, videos, and experiments: [OBEYED-VLA](https://uark-aicv.github.io/OBEYED_VLA/).
