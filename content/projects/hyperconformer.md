---
title: "HyperConformer"
date: 2023-01-01
weight: 40
featured: true
hook: "A Conformer variant where attention is replaced with HyperMixer, matched accuracy, less compute."
tags: ["ASR", "Architecture", "Efficient ML"]
description: "HyperConformer replaces quadratic self-attention in Conformer ASR encoders with a linear-complexity HyperMixer, achieving matched WER on Librispeech while reducing compute, especially for long-form and streaming speech recognition."
summary: "Attention is the expensive part of Conformer-based ASR models. HyperConformer swaps it for a multi-head HyperMixer, which scales linearly in sequence length rather than quadratically. Same WER as Conformer at a meaningful compute cut."
links:
  - name: paper
    url: "https://arxiv.org/abs/2305.18281"
  - name: github
    url: "https://github.com/speechbrain/speechbrain"
---

## Why

Conformer has become the default ASR encoder, but its self-attention scales quadratically with sequence length, a real bottleneck for streaming and long-form recognition. HyperMixer is a linear-complexity alternative to attention that had been shown to work well on NLP tasks; we asked whether it generalizes to speech.

## What we did

Replaced Conformer's self-attention with a **multi-head HyperMixer** block, keeping the convolutional module and macaron feedforward layers unchanged. Trained on Librispeech and CommonVoice with SpeechBrain.

## Results

- **On par with Conformer** on Librispeech (same WER, no regression)
- **Better than Conformer** on limited-data settings (CommonVoice)
- **Linear time complexity**: meaningful wins for longer utterances

## Status

Merged into SpeechBrain recipes. Interspeech 2023.
