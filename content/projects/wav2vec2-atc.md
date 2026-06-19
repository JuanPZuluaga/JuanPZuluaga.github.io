---
title: "wav2vec2-atc"
date: 2022-01-01
weight: 20
featured: true
hook: "Self-supervised ASR models fine-tuned for Air Traffic Control, available on HuggingFace."
tags: ["ASR", "Self-supervised", "Wav2Vec2", "HuggingFace"]
description: "A family of Wav2Vec2 and XLS-R models fine-tuned for Air Traffic Control speech recognition, achieving 20–40% relative WER reduction over supervised baselines. Released on HuggingFace with training recipes and a Colab notebook."
summary: "A family of Wav2Vec2 models that achieve 20–40% relative WER reduction on ATC data compared to supervised baselines. Released with training recipes, evaluation scripts, and a Colab notebook for immediate inference. The benchmark paper at SLT 2022 studies self-supervised pretraining behavior under heavy domain shift."
links:
  - name: huggingface
    url: "https://huggingface.co/Jzuluaga"
  - name: github
    url: "https://github.com/idiap/w2v2-air-traffic"
  - name: paper
    url: "https://arxiv.org/abs/2203.16822"
  - name: colab
    url: "https://colab.research.google.com/github/idiap/w2v2-air-traffic/blob/main/src/eval_xlsr_atc_model.ipynb"
---

Wav2Vec2 and XLS-R models fine-tuned on public ATC datasets (ATCOSIM, LDC-ATCC, UWB-ATCC), released through HuggingFace for anyone to benchmark or build on.

## Headline results

- **20–40% relative WER reduction** vs. supervised Conformer baselines on in-domain ATC test sets
- **Cross-accent generalization** via XLS-R — a single model trained on mixed European ATC data
- **~6% WER** on ATCOSIM with the Wav2Vec2-Large fine-tune

## What's released

| Model | Training data | Link |
|-------|--------------|------|
| Wav2Vec2-Large ATC | ATCOSIM | [HuggingFace ↗](https://huggingface.co/Jzuluaga/wav2vec2-large-960h-lv60-self-en-atc-atcosim) |
| Wav2Vec2-Base ATC | LDC-ATCC | [HuggingFace ↗](https://huggingface.co/Jzuluaga/wav2vec2-base-en-atc-ldc-atcc) |
| XLS-R ATC | All public ATC | [HuggingFace ↗](https://huggingface.co/Jzuluaga/xls-r-300m-en-atc) |

## Try it

The Colab notebook loads any of the models and transcribes an audio sample in under a minute — no GPU required for inference.

## Context

This work is part of my PhD at Idiap/EPFL and was presented at IEEE SLT 2022. The accompanying paper systematically studies how self-supervised representations transfer under heavy domain shift — something surprisingly under-studied before we published.
