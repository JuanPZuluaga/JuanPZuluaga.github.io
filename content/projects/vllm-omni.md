---
title: "vLLM-Omni"
date: 2026-01-01
weight: 5
featured: true
hook: "21+ merged PRs to vLLM-Omni — the production inference engine for omni-modality models."
tags: ["Inference", "TTS", "CUDA", "Open-source", "vLLM"]
description: "Juan Pablo Zuluaga has 21+ merged PRs to vLLM-Omni covering Qwen3-TTS and OmniVoice: streaming output, CUDA Graph + torch.compile, batched Code2Wav decoding, global speaker cache manager, OOM-safe prefix caching, and large throughput/latency gains at high concurrency."
summary: "21+ merged PRs across Qwen3-TTS and OmniVoice: streaming output, CUDA Graph + torch.compile, batched Code2Wav decoding, global speaker cache manager, OOM-safe prefix caching, and large throughput & latency wins under high concurrency."
links:
  - name: github
    url: "https://github.com/vllm-project/vllm-omni"
  - name: my commits
    url: "https://github.com/vllm-project/vllm-omni/commits?author=JuanPZuluaga"
---

[vLLM-Omni](https://github.com/vllm-project/vllm-omni) is the production inference engine for omni-modality models — text, speech, audio, and vision. I'm an active contributor with 21+ merged PRs, primarily on the Qwen3-TTS and OmniVoice serving paths.

## What I've shipped

### Streaming & latency

- **[#1438](https://github.com/vllm-project/vllm-omni/pull/1438) Streaming output for Qwen3-TTS** — real-time token-by-token audio output, enabling low-latency conversational TTS.
- **[#1583](https://github.com/vllm-project/vllm-omni/pull/1583) Flexible initial-phase TTFA reduction** — cut time-to-first-audio by adjusting the initial chunking strategy.
- **[#1714](https://github.com/vllm-project/vllm-omni/pull/1714) Dynamic TTFA based on Code2Wav load** — adaptive initial phase that trades latency for throughput based on real-time decoder utilization.
- **[#1930](https://github.com/vllm-project/vllm-omni/pull/1930) Streaming bugfix** — removed redundant initial-chunk recomputation that was doubling latency on the first audio chunk.

### GPU performance (Code2Wav & CodePredictor)

- **[#1797](https://github.com/vllm-project/vllm-omni/pull/1797) Triton SnakeBeta + CUDA Graph for Code2Wav** — fused the activation kernel and captured the decoder into a CUDA Graph for near-zero kernel launch overhead.
- **[#1426](https://github.com/vllm-project/vllm-omni/pull/1426) Batched Code2Wav decoding** — parallel waveform generation from multiple token sequences; major throughput win at high concurrency.
- **[#1913](https://github.com/vllm-project/vllm-omni/pull/1913) `torch.compile` with `reduce-overhead` + `dynamic=False`** — static-shape compilation of the CodePredictor for consistent kernel reuse across requests.
- **[#2376](https://github.com/vllm-project/vllm-omni/pull/2376) CUDA Graph for Code2Wav decoder (Qwen3-Omni)** — full CUDA Graph capture of the waveform decoder, eliminating CPU-GPU round trips.
- **[#1852](https://github.com/vllm-project/vllm-omni/pull/1852) Big throughput + latency win at high concurrency** — orchestrator and talker optimizations that significantly improved model throughput and P99 latency under concurrent TTS load.

### Voice cloning & speaker management

- **[#2630](https://github.com/vllm-project/vllm-omni/pull/2630) Global speaker cache manager** — centralized, eviction-aware cache for voice embeddings; makes multi-speaker and voice-cloning requests efficient at scale.
- **[#2676](https://github.com/vllm-project/vllm-omni/pull/2676) OmniVoice voice cloning** — end-to-end voice cloning in the OmniVoice TTS path.
- **[#2046](https://github.com/vllm-project/vllm-omni/pull/2046) Voice upload + optional `ref_text`** — REST API support for uploading reference audio with optional transcription for better speaker adaptation.
- **[#1079](https://github.com/vllm-project/vllm-omni/pull/1079) Load `speaker_id`/`voices` from model config** — load-time voice resolution so serving configs stay clean.

### Architecture & shared modules

- **[#2375](https://github.com/vllm-project/vllm-omni/pull/2375) Shared CodePredictor for Qwen3-TTS and Qwen3-Omni** — unified the autoregressive code-prediction module across both model families to avoid duplicate codepaths.
- **[#2108](https://github.com/vllm-project/vllm-omni/pull/2108) Voice cache manager refactor** — cleaner abstraction, correct LRU eviction, and thread-safe access for concurrent serving.

### Prefix caching & OOM hardening

- **[#3688](https://github.com/vllm-project/vllm-omni/pull/3688) Hot-buffer caching with eviction fallback** — cache frequently recomputed talker buffers, fall back gracefully when evicted rather than crashing.
- **[#3689](https://github.com/vllm-project/vllm-omni/pull/3689) Prefix-cache OOM guards + talker/orchestrator micro-opts** — prevents out-of-memory crashes under bursty load while squeezing additional latency out of the hot path.
- **[#4317](https://github.com/vllm-project/vllm-omni/pull/4317) Drop per-key size cap corrupting prefix cache** — bugfix that eliminated silent cache corruption in long-context Qwen3-TTS requests.

### Bugfixes

- **[#2059](https://github.com/vllm-project/vllm-omni/pull/2059) CodePredictor CUDA Graph pool fix** — resolved pool exhaustion under rapid successive requests.
- **[#2102](https://github.com/vllm-project/vllm-omni/pull/2102) Chunk-transfer adapter deque mutation** — fixed a concurrent-modification bug in the streaming adapter.
- **[#1289](https://github.com/vllm-project/vllm-omni/pull/1289) Qwen3-TTS general bugfixes** — early stability fixes in the initial Qwen3-TTS integration.

## Why it matters

Serving omni-modality models at production scale has a different shape than pure-LLM serving: a TTS request carries an autoregressive code-predictor *and* a waveform decoder (Code2Wav), each with its own batching and latency budget. The work above is focused on making that path fast, streamable, and low-TTFA for real-world usage — which directly maps to my day-job work in production TTS and speech LLM serving.
