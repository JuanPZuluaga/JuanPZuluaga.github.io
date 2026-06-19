---
title: "vLLM-Omni"
date: 2026-01-01
weight: 5
featured: true
hook: "Active contributor to vLLM-Omni — the production inference engine for omni-modality models."
tags: ["Inference", "TTS", "CUDA", "Open-source", "vLLM"]
description: "Juan Pablo Zuluaga is an active contributor to vLLM-Omni with 20+ merged PRs across Qwen3-TTS and OmniVoice: streaming output, CUDA Graph + torch.compile, batched Code2Wav decoding, global speaker cache manager, and OOM-safe prefix caching."
summary: "20+ merged PRs across Qwen3-TTS and OmniVoice: streaming output, CUDA Graph + torch.compile, batched Code2Wav decoding, global speaker cache manager, and large throughput & latency wins under high concurrency."
links:
  - name: github
    url: "https://github.com/vllm-project/vllm-omni"
  - name: my commits
    url: "https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga"
---

[vLLM-Omni](https://github.com/vllm-project/vllm-omni) is the production inference engine for omni-modality models — text, speech, audio, and vision. I'm an active contributor with 20+ merged PRs, primarily on the Qwen3-TTS and OmniVoice serving paths.

## What I work on

**Streaming & low-latency TTS** — real-time token-by-token audio output, dynamic time-to-first-audio (TTFA) tuning based on Code2Wav load, and flexible initial-phase chunking to minimize perceived latency.

**GPU kernel optimization** — CUDA Graph capture of Code2Wav and CodePredictor, Triton SnakeBeta kernel fusion, `torch.compile` with `reduce-overhead` and static shapes, and batched waveform decoding for high-concurrency throughput.

**Voice cloning & speaker management** — global speaker cache manager with LRU eviction, OmniVoice voice cloning, reference audio upload, and load-time speaker resolution from model config.

**Prefix-cache hardening** — OOM guards, per-key eviction fallbacks, and fixes for silent cache corruption under long-context requests.

## Why it matters

Serving TTS at production scale is different from pure-LLM serving: each request runs an autoregressive code-predictor *and* a waveform decoder (Code2Wav), each with its own batching and latency budget. This work makes that pipeline fast, streamable, and stable under real-world concurrent load.
