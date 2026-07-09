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
tldr_points:
  - "**Problem:** ATC speech is safety-critical and uniquely hard, yet the largest open datasets were only a few dozen hours."
  - "**Idea:** an end-to-end pipeline to collect, auto-transcribe, quality-filter, and annotate live VHF ATC audio at scale."
  - "**Result:** a **5,000-hour** open corpus, now a standard benchmark across Europe."
flow:
  title: "The data pipeline"
  steps:
    - label: "Live VHF audio"
      sub: "European airspace"
    - label: "Auto-transcribe & filter"
      sub: "pseudo-labeling"
    - label: "Role labels + metadata"
      sub: "callsigns, commands"
    - label: "5,000 h corpus"
      sub: "open release"
      highlight: true
stats:
  - value: "5,000 h"
    label: "of live air traffic control audio"
  - value: "4-year"
    label: "EU project (SESAR Joint Undertaking)"
  - value: "1st"
    label: "open ATC corpus at this scale"
achievements:
  - "**5,000 hours** of real ATC audio, orders of magnitude larger than prior open sets"
  - "Transcripts, **speaker-role labels**, and surveillance-linked contextual metadata"
  - "Released in tiers (gold-standard test → full pool) and used as a benchmark across Europe"
impact: "Turned a data-starved field into one where large pretrained models can be studied at realistic scale. ATCO2 is now a standard benchmark for ATC speech research and is available for research use through ELRA."
links:
  - name: arxiv
    url: "https://arxiv.org/abs/2211.04054"
  - name: code
    url: "https://github.com/idiap/atco2-corpus"
  - name: data
    url: "https://www.atco2.org/data"
---
