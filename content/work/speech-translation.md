---
title: "End-to-End Speaker-Turn-Aware Speech Translation"
url: "/work/speech-translation/"
weight: 40
venue: "EMNLP"
year: 2023
authors: "<strong>J. P. Zuluaga</strong>, Z. Huang, X. Niu, R. Paturi, S. Srinivasan, P. Mathur, B. Thompson, M. Federico."
paper: "https://aclanthology.org/2023.emnlp-main.493/"
arxiv: "https://arxiv.org/abs/2311.00697"
tldr: "The first **end-to-end** speech translation system that handles speaker turns and overlapping speech on a single channel, built during my internship at **AWS** and published at EMNLP 2023."
tags: ["Speech Translation", "End-to-end", "Diarization"]
description: "An end-to-end speech translation system that jointly handles speaker turns and overlapping speech on a single channel, published at EMNLP 2023. Work done during an AWS internship."
images: ["/papers/speech-translation/og.png"]
tldr_points:
  - "**Problem:** real conversations have people talking over each other on one channel; cascaded pipelines lose overlapping speech."
  - "**Idea:** an end-to-end model that jointly detects speaker turns and translates, directly from single-channel audio."
  - "**Result:** the **first** end-to-end, speaker-turn-aware speech translation system for this setting."
flow:
  title: "How it works"
  steps:
    - label: "Single-channel audio"
      sub: "overlapping speakers"
    - label: "End-to-end model"
      sub: "joint turns + translation"
      highlight: true
    - label: "Per-speaker translation"
      sub: "who said what"
hero_image: "/papers/e2e-translation/waveforms.png"
hero_caption: "Single-channel conversational audio with overlapping speakers (top) decomposed into per-speaker streams: the model translates while tracking who spoke when."
stats:
  - value: "1st"
    label: "end-to-end single-channel, speaker-turn-aware ST"
  - value: "AWS"
    label: "research internship, published at **EMNLP 2023**"
  - value: "open"
    label: "code released for reproducibility"
achievements:
  - "**First** end-to-end system to jointly handle speaker turns and translation on a single channel"
  - "Robust to **overlapping speech**, where cascaded pipelines break down"
  - "Published at **EMNLP 2023**; code released for reproducibility"
impact: "Pushed speech translation toward realistic, conversational audio, the setting that matters for meetings, calls, and live interpretation, and showed that jointly modeling speaker structure and translation beats cascading them."
links:
  - name: paper
    url: "https://aclanthology.org/2023.emnlp-main.493/"
  - name: arxiv
    url: "https://arxiv.org/abs/2311.00697"
  - name: code
    url: "https://github.com/amazon-science/stac-speech-translation"
---
