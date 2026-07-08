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
hero_image: "/papers/commonaccent/architecture.png"
hero_caption: "The AccentID classification system: fine-tune a self-supervised wav2vec 2.0 / XLSR encoder (or an ECAPA-TDNN) with a statistics-pooling accent head."
stats:
  - value: "95.1%"
    label: "accent-ID accuracy (wav2vec 2.0-XLSR, English)"
  - value: "★"
    label: "Best Student Paper **nominee**, Interspeech 2023"
  - value: "4"
    label: "languages benchmarked (EN, DE, ES, IT)"
problem: |
  Recognizing *which accent* a speaker has is useful for fairer ASR, targeted TTS, and dialect research, but accent-classification benchmarks were fragmented and hard to reproduce. It was also unclear whether the large self-supervised encoders that had transformed ASR would help for a paralinguistic task like accent identification.
approach: |
  I built **CommonAccent**, a reproducible recipe on top of the Common Voice dataset, and compared two families of models: a strong speaker-embedding model (ECAPA-TDNN) and fine-tuned self-supervised encoders (wav2vec 2.0 / XLSR), each with a statistics-pooling accent head and data augmentation. The recipe extends cleanly from English to German, Spanish, and Italian.
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
contribution: |
  First-author work during my PhD. I designed the benchmark and recipe, ran the model comparison and multilingual extension, and released the **fine-tuned accent-ID model on HuggingFace** plus the full training code, so anyone can reproduce or build on it. The paper was a **Best Student Paper nominee** at Interspeech 2023.
achievements:
  - "**95.1% → 97.1%** English accent-ID accuracy with self-supervised models + augmentation"
  - "A single **reproducible recipe** that extends across four languages"
  - "Open model on HuggingFace and full code, so results are immediately reusable"
impact: |
  CommonAccent gave the community a clean, reproducible accent-classification baseline and showed that self-supervised speech representations transfer strongly to paralinguistic tasks, not just transcription.
links:
  - name: arxiv
    url: "https://arxiv.org/abs/2305.18283"
  - name: code
    url: "https://github.com/JuanPZuluaga/accent-recog-slt2022"
  - name: model
    url: "https://huggingface.co/Jzuluaga/accent-id-commonaccent_ecapa"
---
