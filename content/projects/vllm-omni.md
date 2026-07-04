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

**Streaming & low-latency TTS** — real-time token-by-token audio output [[1]](https://github.com/vllm-project/vllm-omni/pull/1438), dynamic TTFA tuning based on Code2Wav load [[2]](https://github.com/vllm-project/vllm-omni/pull/1714), and flexible initial-phase chunking to minimize perceived latency [[3]](https://github.com/vllm-project/vllm-omni/pull/1583).

**GPU kernel optimization** — CUDA Graph capture of Code2Wav and CodePredictor [[4]](https://github.com/vllm-project/vllm-omni/pull/2376), Triton SnakeBeta kernel fusion [[5]](https://github.com/vllm-project/vllm-omni/pull/1797), `torch.compile` with `reduce-overhead` and static shapes [[6]](https://github.com/vllm-project/vllm-omni/pull/1913), and batched waveform decoding for high-concurrency throughput [[7]](https://github.com/vllm-project/vllm-omni/pull/1426).

**Voice cloning & speaker management** — global speaker cache manager with LRU eviction [[8]](https://github.com/vllm-project/vllm-omni/pull/2630), OmniVoice voice cloning [[9]](https://github.com/vllm-project/vllm-omni/pull/2676), and reference audio upload with optional transcription [[10]](https://github.com/vllm-project/vllm-omni/pull/2046).

**Prefix-cache hardening** — OOM guards and hot-buffer fallbacks [[11]](https://github.com/vllm-project/vllm-omni/pull/3689), and fixes for silent cache corruption under long-context requests [[12]](https://github.com/vllm-project/vllm-omni/pull/4317).

## Why it matters

Serving TTS at production scale is different from pure-LLM serving: each request runs an autoregressive code-predictor *and* a waveform decoder (Code2Wav), each with its own batching and latency budget. This work makes that pipeline fast, streamable, and stable under real-world concurrent load.
