---
title: "ATCO2: The Largest Open Air Traffic Control Speech Corpus"
url: "/work/atco2-corpus/"
weight: 15
venue: "arXiv"
year: 2023
authors: "<strong>J. P. Zuluaga</strong>, K. Vesely, I. Szoke, P. Motlicek, M. Kocour, M. Rigault, K. Choukri, A. Prasad, S. Sarfjoo, I. Nigmatulina, C. Cevenini, P. Kolcarek, A. Tart, J. Cernocky, D. Klakow."
arxiv: "https://arxiv.org/abs/2211.04054"
tldr: "A **5,000-hour** open corpus of real air traffic control communications, with transcripts, speaker-role labels, and contextual metadata, the largest open ATC dataset for speech recognition and understanding."
tags: ["Dataset", "ASR", "NLU"]
description: "ATCO2 is a 5,000-hour open corpus of air traffic control communications with transcripts, speaker-role labels, and contextual metadata, the largest open ATC dataset for ASR and NLU research."
images: ["/papers/atco2-corpus/og.png"]
stats:
  - value: "5,000 h"
    label: "of live air traffic control audio"
  - value: "4-year"
    label: "EU project (SESAR Joint Undertaking)"
  - value: "1st"
    label: "open ATC corpus at this scale"
problem: |
  Air traffic control speech is a uniquely hard, safety-critical domain, yet before ATCO2 the largest open datasets were only a few dozen hours: far too small to train or fairly evaluate modern self-supervised systems. Progress was bottlenecked by data.
approach: |
  ATCO2 built an end-to-end pipeline to collect, automatically transcribe, and quality-filter live VHF air traffic control audio from across European airspace, then enrich it with **speaker-role labels** (pilot vs. controller) and **contextual metadata** (callsigns, commands, waypoints) linked to surveillance data. The result is released in tiers, from a small gold-standard test set to the full 5,000-hour pool.
contribution: |
  I was a lead author and driving contributor on the corpus: the collection and pseudo-labeling pipeline, the annotation scheme, and the released benchmark splits. It became the backbone of my PhD and of several follow-up projects on contextual ASR, diarization, and callsign recognition.
achievements:
  - "**5,000 hours** of real ATC audio, orders of magnitude larger than prior open sets"
  - "Transcripts, **speaker-role labels**, and surveillance-linked contextual metadata"
  - "Released in tiers (gold-standard test → full pool) and used as a benchmark across Europe"
impact: |
  ATCO2 turned a data-starved field into one where large pretrained models can be studied at realistic scale. It is now a standard benchmark for ATC speech research and is available for research use through ELRA.
links:
  - name: arxiv
    url: "https://arxiv.org/abs/2211.04054"
  - name: code
    url: "https://github.com/idiap/atco2-corpus"
  - name: data
    url: "https://www.atco2.org/data"
---
