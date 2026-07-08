---
title: "CommonAccent: Accent Classification with Self-Supervised Models"
url: "/work/commonaccent/"
weight: 30
venue: "Interspeech"
year: 2023
award: "Best Student Paper nominee"
authors: "<strong>J. P. Zuluaga</strong>, S. Sarfjoo, A. Prasad, I. Nigmatulina, P. Motlicek, K. Ondrej, O. Ohneiser, H. Helmke."
arxiv: "https://arxiv.org/abs/2305.18283"
tldr: "A benchmark and open model for spoken-accent classification on Common Voice, reaching **95%+ accuracy** with self-supervised models. Best Student Paper nominee at Interspeech 2023."
tags: ["Accent ID", "Self-supervised", "Benchmark"]
description: "CommonAccent: an accent classification benchmark on Common Voice using large self-supervised models, reaching 95%+ accuracy. Best Student Paper nominee at Interspeech 2023, with an open model on HuggingFace."
images: ["/papers/commonaccent/og.png"]
tldr_points:
  - "**Problem:** accent-classification benchmarks were fragmented, and it was unclear whether self-supervised encoders would help for a paralinguistic task."
  - "**Idea:** a reproducible Common Voice recipe comparing an ECAPA-TDNN against fine-tuned wav2vec 2.0 / XLSR, extended to four languages."
  - "**Result:** **95.1% → 97.1%** accuracy, an open model, and a Best Student Paper nomination."
flow:
  title: "How it works"
  steps:
    - label: "Speech utterance"
      sub: "Common Voice"
    - label: "Self-supervised encoder"
      sub: "wav2vec 2.0-XLSR"
      highlight: true
    - label: "Stat-pooling head"
      sub: "accent classifier"
    - label: "Accent label"
      sub: "95%+ accuracy"
hero_image: "/papers/commonaccent/architecture.png"
hero_caption: "The AccentID classification system: fine-tune a self-supervised wav2vec 2.0 / XLSR encoder (or an ECAPA-TDNN) with a statistics-pooling accent head."
stats:
  - value: "95.1%"
    label: "accent-ID accuracy (wav2vec 2.0-XLSR, English)"
  - value: "★"
    label: "Best Student Paper **nominee**, Interspeech 2023"
  - value: "4"
    label: "languages benchmarked (EN, DE, ES, IT)"
results:
  title: "Accent-ID accuracy on English Common Voice (higher is better)"
  unit: "%"
  bars:
    - label: "ECAPA-TDNN"
      value: 79.0
    - label: "wav2vec 2.0-XLSR"
      value: 95.1
      highlight: true
    - label: "wav2vec 2.0-XLSR + augmentation"
      value: 97.1
      highlight: true
  note: "Self-supervised representations decisively outperform the speaker-embedding baseline; data augmentation adds a further robustness gain."
achievements:
  - "**95.1% → 97.1%** English accent-ID accuracy with self-supervised models + augmentation"
  - "A single **reproducible recipe** that extends across four languages"
  - "Open model on HuggingFace and full code, so results are immediately reusable"
impact: "Gave the community a clean, reproducible accent-classification baseline and showed that self-supervised speech representations transfer strongly to paralinguistic tasks, not just transcription."
role: "**First author**, PhD work. I designed the benchmark and recipe, ran the model comparison and multilingual extension, and released the accent-ID model on HuggingFace."
links:
  - name: arxiv
    url: "https://arxiv.org/abs/2305.18283"
  - name: code
    url: "https://github.com/JuanPZuluaga/accent-recog-slt2022"
  - name: model
    url: "https://huggingface.co/Jzuluaga/accent-id-commonaccent_ecapa"
---
