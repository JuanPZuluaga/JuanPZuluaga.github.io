---
title: "vLLM-Omni: Production Serving for Omni-Modal Models"
url: "/work/vllm-omni/"
weight: 5
venue: "Open source"
year: 2026
tldr: "**20+ merged PRs** to vLLM-Omni, the production inference engine for text, speech, audio, and vision models, focused on streaming TTS, CUDA-graph kernels, and high-concurrency serving."
tags: ["Inference", "TTS", "CUDA", "vLLM"]
description: "20+ merged PRs to vLLM-Omni, the production inference engine for omni-modal models: streaming TTS, CUDA Graph kernels, torch.compile, voice cloning, and high-concurrency serving."
images: ["/papers/vllm-omni/og.png"]
stats:
  - value: "20+"
    label: "merged PRs to vLLM-Omni"
  - value: "Qwen3-TTS"
    label: "& OmniVoice serving paths"
  - value: "prod"
    label: "high-concurrency, low-latency serving"
problem: |
  Serving omni-modal models at production scale is unlike pure-LLM serving: a text-to-speech request runs an autoregressive code-predictor **and** a waveform decoder (Code2Wav), each with its own batching and latency budget. Making that pipeline fast, streamable, and stable under real concurrent load is a hard systems problem.
approach: |
  I contribute across the [vLLM-Omni](https://github.com/vllm-project/vllm-omni) TTS serving stack, from GPU kernels up to the request scheduler, optimizing for time-to-first-audio and throughput at high concurrency while keeping the system stable under bursty load.
achievements:
  - "**Streaming & low-latency TTS** — real-time token-by-token output and dynamic time-to-first-audio tuning"
  - "**GPU kernel optimization** — CUDA Graph capture, Triton kernel fusion, and `torch.compile` with static shapes"
  - "**Voice cloning & speaker management** — a global speaker cache with LRU eviction and reference-audio upload"
  - "**Prefix-cache hardening** — OOM guards and fixes for silent cache corruption under long-context load"
impact: |
  This work makes open, omni-modal TTS serving genuinely production-ready: faster, streamable, and stable at concurrency. It maps directly to the generative-audio serving I do day to day, and it is all upstreamed to a widely used open-source project.
links:
  - name: github
    url: "https://github.com/vllm-project/vllm-omni"
  - name: my commits
    url: "https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga"
---
