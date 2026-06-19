---
title: "vLLM-Omni"
date: 2026-01-01
weight: 5
featured: true
hook: "Active contributor to vLLM-Omni — the inference engine for omni-modality models (text, speech, audio, vision)."
tags: ["Inference", "TTS", "Open-source", "vLLM"]
description: "Juan Pablo Zuluaga is an active contributor to vLLM-Omni, the omni-modality inference engine. Contributions include Qwen3-TTS streaming, Code2Wav batched decoding, CUDA Graph + torch.compile optimization, OmniVoice voice cloning, and high-concurrency TTS throughput improvements."
summary: "Ongoing contributions to vLLM-Omni's Qwen3-TTS and OmniVoice paths: streaming output, Code2Wav batched decoding, CUDA Graph + torch.compile, voice cloning, and throughput/latency optimization for high-concurrency TTS serving."
links:
  - name: github
    url: "https://github.com/vllm-project/vllm-omni"
  - name: my commits
    url: "https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga"
---

[vLLM-Omni](https://github.com/vllm-project/vllm-omni) is a framework for efficient inference of omni-modality models — text, speech, audio, and vision. I'm an active contributor, mostly on the TTS serving path.

## What I've shipped

- **OmniVoice voice cloning** — end-to-end voice cloning support in the OmniVoice TTS path.
- **Qwen3-TTS streaming** — incremental token-by-token output, dynamic TTFA based on Code2Wav load, flexible initial chunking.
- **Code2Wav performance** — batched decoding, Triton SnakeBeta kernel, CUDA Graph, and `torch.compile` (reduce-overhead, dynamic-shape off).
- **High-concurrency throughput** — large wins on model throughput and latency at high concurrency for Qwen3-TTS.
- **Voice / speaker management** — voice cache manager refactor, `speaker_id`/`voices` loading from model config, `ref_text` handling.
- **Bug fixes** — chunk-transfer adapter deque mutation, CodePredictor CUDA Graph pool issue, streaming initial-chunk recomputation.

## Why it matters

Serving omni-modality models at production scale has a very different shape than pure-LLM serving: a TTS request carries an autoregressive code-predictor and a waveform decoder (Code2Wav), each with its own batching and latency budget. The work above is focused on making that path fast, streamable, and low-TTFA for real-world usage — which directly maps to the TTS/generative audio work I do in my day job.

Full commit list: [github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga](https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga).
