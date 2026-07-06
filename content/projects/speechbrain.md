---
title: "SpeechBrain 1.0"
date: 2024-01-01
weight: 50
featured: true
hook: "Co-authored the 1.0 release of the open-source conversational AI toolkit."
tags: ["Open Source", "PyTorch", "Speech", "NLP"]
description: "SpeechBrain 1.0 is a PyTorch-based open-source toolkit for speech and language tasks, ASR, TTS, speaker recognition, and dialogue, with stable APIs and reproducible recipes. Juan Pablo Zuluaga contributed ATC ASR recipes, HyperConformer, and accent classification benchmarks."
summary: "SpeechBrain is a PyTorch-based toolkit for speech and language tasks, used by dozens of research groups and startups. The 1.0 release (JMLR 2024) consolidates years of contributions into a stable API with comprehensive recipes for ASR, TTS, speaker recognition, and dialogue understanding."
links:
  - name: github
    url: "https://github.com/speechbrain/speechbrain"
  - name: jmlr
    url: "https://jmlr.org/papers/v25/24-0991.html"
---

SpeechBrain is an open-source toolkit built to make conversational AI research easier. 1.0 is the stable milestone, a coherent API across dozens of tasks, production-ready recipes, and comprehensive documentation.

## My contributions

- **ATC ASR recipes** (Wav2Vec2, XLS-R fine-tuning on air traffic control data)
- **HyperConformer** encoder (see separate project)
- **Accent classification** benchmarks (CommonAccent)
- Bug fixes, documentation, and review across the speech modules

## Why it matters

Before SpeechBrain, building a speech system with PyTorch meant gluing together bits from ESPnet, Kaldi, Fairseq, and custom code. SpeechBrain unifies that into a single toolkit that covers ASR, TTS, speaker recognition, speech enhancement, and dialogue, all with reproducible recipes.

Used by research groups at Idiap, EPFL, Mila, Meta, and dozens of startups.

## Citation

If you use SpeechBrain in your work, please cite the JMLR 2024 paper.
