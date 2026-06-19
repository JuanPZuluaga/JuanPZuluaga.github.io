---
title: "ATCO2 Corpus"
date: 2023-01-01
weight: 10
featured: true
hook: "5,000 hours of Air Traffic Control communications — the largest open ATC speech dataset."
tags: ["Speech", "ASR", "Dataset", "NLU"]
description: "ATCO2 is a 5,000-hour multilingual corpus of Air Traffic Control speech with transcripts, speaker role labels, and contextual metadata — the largest open ATC dataset for ASR and NLU research."
summary: "A multilingual, semi-automatically labeled corpus built to advance ASR and natural language understanding on one of the hardest real-world speech domains. Includes audio, transcripts, speaker role annotations, and a preprocessing pipeline. Used as a benchmark by follow-up work across Europe."
links:
  - name: github
    url: "https://github.com/idiap/atco2-corpus"
  - name: paper
    url: "https://arxiv.org/abs/2211.04054"
---

ATCO2 is a four-year effort (2020–2024) funded by the European SESAR Joint Undertaking, aiming to produce a large-scale open corpus of Air Traffic Control communications.

## What's in it

- **~5,000 hours** of audio from live VHF recordings across European airspace
- **Transcripts** (semi-automatic, manually verified on a subset)
- **Speaker role labels** (pilot vs. air traffic controller)
- **Contextual metadata** (callsigns, commands, waypoints — linked to surveillance data)
- **Four subsets:** 4 hours gold-standard · 1 hour test-full · the full 5k-hour pool · ATCO2-PL (pilot-only)

## Why it matters

ATC speech is uniquely hard for ASR: channel noise, rapid speech, heavy code-switching between English and local languages, and a strictly domain-specific vocabulary. Before ATCO2, the largest open ATC dataset was a few dozen hours — too small to train modern self-supervised systems. ATCO2 makes it possible to study domain-shift behavior of large pretrained models at a realistic scale.

## Downstream use

The corpus has been used as a training set or benchmark by follow-up work on contextual ASR, speaker diarization, callsign recognition, and speech translation. It's available on [ELRA](http://catalog.elra.info/) for research use.
