---
title: "BERTraffic: BERT-based Joint Speaker Role and Speaker Change Detection for Air Traffic Control Communications"
collection: publications
permalink: /publication/2022-BERTraffic A Robust BERT Based Approach
excerpt: 'This paper is about Automatic Speech Recognition in Air-traffic Control Communications'
date: 2022-12-01
venue: 'IEEE SLT'
paperurl: 'https://arxiv.org/abs/2110.05781'
citation: 'Juan Zuluaga-Gomez, Seyyed Saeed Sarfjoo, Amrutha Prasad, Iuliia Nigmatulina, Petr Motlicek, Karel Ondrej, Oliver Ohneiser, Hartmut Helmke, 2022. BERTraffic: BERT-based Joint Speaker Role and Speaker Change Detection for Air Traffic Control Communications. 2022 IEEE Spoken Language Technology Workshop (SLT), Doha, Qatar.'
---

Abstract: Automatic speech recognition (ASR) allows transcribing the communications between air traffic controllers (ATCOs) and aircraft pilots. The transcriptions are used later to extract ATC named entities e.g., aircraft callsigns, command types, or values. One common challenge is Speech Activity Detection (SAD) and diarization system. If one of them fails then two or more single speaker segments remain in the same recording, jeopardizing the overall system's performance. We propose a system that combines the segmentation of a SAD module with a BERT model that performs speaker change detection (SCD) and speaker role detection (SRD) by chunking ASR transcripts i.e., diarization with a defined number of speakers together with SRD. The proposed model is evaluated on real-life ATC test sets. It reaches up to 0.90/0.95 F1-score on ATCO/pilot SRD, which means a 27% relative improvement on diarization error rate (DER) compared to standard acoustic-based diarization. Results are measured on ASR transcripts of challenging ATC test sets with ∼13% word error rate, and the robustness of the system is even validated on noisy ASR transcripts.


[Download paper here](https://arxiv.org/abs/2110.05781)

**Recommended citation**: 

Zuluaga-Gomez, J., Sarfjoo, S. S., Prasad, A., Nigmatulina, I., Motlicek, P., Ondrej, K., Ohneiser, O., & Helmke, H. (2021). BERTraffic: BERT-based Joint Speaker Role and Speaker Change Detection for Air Traffic Control Communications. 2022 IEEE Spoken Language Technology Workshop (SLT), Doha, Qatar.{: .notice}

- BibTeX:

<pre>
@article{zuluagabertraffic,
  title={BERTraffic: BERT-based Joint Speaker Role and Speaker Change Detection for Air Traffic Control Communications (submitted to @ SLT-2022)},
  author={Zuluaga-Gomez, Juan and Sarfjoo, Seyyed Saeed and Prasad, Amrutha and Nigmatulina, Iuliia and Motlicek, Petr and Ohneiser, Oliver and Helmke, Hartmut},
  journal={2022 IEEE Spoken Language Technology Workshop (SLT), Doha, Qatar},
  year={2022}
}
</pre>