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
tldr_points:
  - "**Problem:** serving TTS at scale runs an autoregressive code-predictor **and** a waveform decoder per request, each with its own latency budget."
  - "**What I do:** **20+ merged PRs** across the vLLM-Omni TTS stack, from GPU kernels up to the request scheduler."
  - "**Result:** faster, streamable, production-stable omni-modal serving, all upstreamed to a widely used project."
flow:
  title: "The TTS serving path"
  steps:
    - label: "Text request"
    - label: "Code Predictor"
      sub: "autoregressive"
    - label: "Code2Wav decoder"
      sub: "CUDA Graph · Triton"
      highlight: true
    - label: "Streaming audio"
      sub: "low time-to-first-audio"
stats:
  - value: "20+"
    label: "merged PRs to vLLM-Omni"
  - value: "Qwen3-TTS"
    label: "& OmniVoice serving paths"
  - value: "prod"
    label: "high-concurrency, low-latency serving"
achievements:
  - "**Streaming & low-latency TTS**: real-time token-by-token output and dynamic time-to-first-audio tuning"
  - "**GPU kernel optimization**: CUDA Graph capture, Triton kernel fusion, and `torch.compile` with static shapes"
  - "**Voice cloning & speaker management**: a global speaker cache with LRU eviction and reference-audio upload"
  - "**Prefix-cache hardening**: OOM guards and fixes for silent cache corruption under long-context load"
impact: "Makes open, omni-modal TTS serving genuinely production-ready: faster, streamable, and stable at concurrency. It maps directly to the generative-audio serving I do day to day, and it is all upstreamed."
links:
  - name: github
    url: "https://github.com/vllm-project/vllm-omni"
  - name: my commits
    url: "https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga"
---
