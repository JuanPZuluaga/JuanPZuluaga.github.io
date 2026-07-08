---
title: "Self-Supervised ASR for Air Traffic Control"
url: "/work/wav2vec2-atc/"
weight: 20
venue: "IEEE SLT"
year: 2022
authors: "<strong>J. P. Zuluaga</strong>, A. Prasad, I. Nigmatulina, S. Sarfjoo, P. Motlicek, M. Kleinert, H. Helmke, O. Ohneiser, Q. Zhan."
arxiv: "https://arxiv.org/abs/2203.16822"
tldr: "Fine-tuning self-supervised speech models (wav2vec 2.0 / XLS-R) for one of the hardest real-world ASR domains, air traffic control, cutting word error rate by **20–40%** over supervised baselines."
tags: ["ASR", "Self-supervised", "Wav2Vec2"]
description: "How fine-tuning wav2vec 2.0 and XLS-R for air traffic control speech recognition achieved 20–40% relative WER reduction under heavy domain shift, with open models on HuggingFace."
images: ["/papers/wav2vec2-atc/og.png"]
tldr_points:
  - "**Problem:** air traffic control is one of the noisiest, most jargon-heavy ASR domains, and open training data was scarce."
  - "**Idea:** fine-tune large self-supervised models (wav2vec 2.0 / XLS-R) instead of training from scratch, across three public ATC corpora."
  - "**Result:** **20–40%** relative WER reduction, plus open models, recipes, and a one-click Colab."
flow:
  title: "How it works"
  steps:
    - label: "Unlabeled speech"
      sub: "thousands of hours"
    - label: "wav2vec 2.0 / XLS-R"
      sub: "self-supervised pretraining"
    - label: "Fine-tune on ATC"
      sub: "ATCOSIM · LDC · UWB"
      highlight: true
    - label: "Robust ATC ASR"
      sub: "20–40% WER ↓"
stats:
  - value: "20–40%"
    label: "relative WER reduction vs. supervised baselines"
  - value: "~6%"
    label: "WER on ATCOSIM (wav2vec 2.0-Large)"
  - value: "3"
    label: "open models released on HuggingFace"
results:
  title: "Relative word error rate (baseline = 100, lower is better)"
  bars:
    - label: "Supervised Conformer baseline"
      value: 100
    - label: "wav2vec 2.0 fine-tuned"
      value: 68
      highlight: true
  note: "Representative of the **20–40% relative WER reduction** measured across in-domain ATC test sets; the exact figure varies by corpus and model size."
achievements:
  - "**20–40% relative WER reduction** vs. supervised baselines on in-domain ATC test sets"
  - "**Cross-accent generalization** with a single XLS-R model trained on mixed European ATC data"
  - "Open models, recipes, and a **run-in-a-minute Colab**, adopted by follow-up work"
impact: "Among the first studies to show how self-supervised pretraining transfers to a safety-critical, heavily domain-shifted setting. The released models became a practical baseline for ATC ASR research, and the recipe generalizes to other low-resource, noisy domains."
role: "**First author**, PhD work at Idiap and EPFL. I designed the benchmark, ran the fine-tuning experiments across model sizes and corpora, and released the models, recipes, and Colab."
links:
  - name: arxiv
    url: "https://arxiv.org/abs/2203.16822"
  - name: code
    url: "https://github.com/idiap/w2v2-air-traffic"
  - name: models
    url: "https://huggingface.co/Jzuluaga"
  - name: colab
    url: "https://colab.research.google.com/github/idiap/w2v2-air-traffic/blob/main/src/eval_xlsr_atc_model.ipynb"
---
