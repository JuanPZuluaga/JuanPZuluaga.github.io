---
title: "BERTraffic"
date: 2022-01-01
weight: 30
featured: true
hook: "Joint speaker-role and speaker-change detection from ATC transcripts, no audio required."
tags: ["NLP", "BERT", "Diarization", "ATC"]
description: "BERTraffic is a BERT-based text-only speaker diarization system for Air Traffic Control that jointly detects turn boundaries and speaker roles (pilot vs. controller), outperforming audio-based baselines by 27% DER."
summary: "Most ATC diarization systems rely on audio signals, which are low-quality and short. BERTraffic reframes the problem as text classification: given a transcript, predict speaker turns and whether each turn is a pilot or controller. Beats audio-only baselines by 27% DER."
links:
  - name: github
    url: "https://github.com/idiap/bert-text-diarization-atc"
  - name: paper
    url: "https://arxiv.org/abs/2110.05781"
---

## The idea

Traditional speaker diarization ("who spoke when") relies on acoustic features, but for Air Traffic Control, the audio signal is poor: VHF noise, short turns (~2s average), and a single mono channel for both parties.

BERTraffic sidesteps that: take the ASR transcript, finetune BERT on a two-head classification task, and output both (a) turn boundaries and (b) the role of each turn (pilot/controller). Surprisingly, text-only beats the strongest audio-only baselines available.

## Results

- **27% relative DER reduction** vs. audio baseline on ATCO2 test set
- Works with **noisy ASR transcripts**, not just gold text, the model is robust to ~15% WER input
- **Joint training** of the two heads is better than pipelining them

## Released

- Full training / evaluation code on GitHub
- Fine-tuned BERT models on HuggingFace (pilot/controller classifier, turn-change classifier)
