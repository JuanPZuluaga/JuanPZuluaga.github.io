---
title: "Contextual Semi-Supervised Learning: An Approach to Leverage Air-Surveillance and Untranscribed ATC Data in ASR Systems"
collection: publications
permalink: /publication/2021-Contextual Semi-Supervised Learning: An Approach to Leverage
excerpt: 'This paper is about the Automatic Speech Recognition for Air-traffic Control Communications'
date: 2021-08-28
venue: 'Interspeech 2021'
paperurl: 'https://isca-speech.org/archive/interspeech_2021/zuluagagomez21_interspeech.html'
citation: 'Zuluaga-Gomez, J., Nigmatulina, I., Prasad, A., Motlicek, P., Veselý, K., Kocour, M., Szöke, I. (2021) Contextual Semi-Supervised Learning: An Approach to Leverage Air-Surveillance and Untranscribed ATC Data in ASR Systems. Proc. Interspeech 2021, 3296-3300, doi: 10.21437/Interspeech.2021-1373.'
---

Air traffic management and specifically air-traffic control (ATC) rely mostly on voice communications between Air Traffic Controllers (ATCos) and pilots. In most cases, these voice communications follow a well-defined grammar that could be leveraged in Automatic Speech Recognition (ASR) technologies. The callsign used to address an airplane is an essential part of all ATCo-pilot communications. We propose a two-step approach to add contextual knowledge during semi-supervised training to reduce the ASR system error rates at recognizing the part of the utterance that contains the callsign. Initially, we represent in a WFST the contextual knowledge (i.e. air-surveillance data) of an ATCo-pilot communication. Then, during Semi-Supervised Learning (SSL) the contextual knowledge is added by second-pass decoding (i.e. lattice re-scoring). Results show that ‘unseen domains’ (e.g. data from airports not present in the supervised training data) are further aided by contextual SSL when compared to standalone SSL. For this task, we introduce the Callsign Word Error Rate (CA-WER) as an evaluation metric, which only assesses ASR performance of the spoken callsign in an utterance. We obtained a 32.1% CA-WER relative improvement applying SSL with an additional 17.5% CA-WER improvement by adding contextual knowledge during SSL on a challenging ATC-based test set gathered from LiveATC.

[Download paper here](https://github.com/JuanPZuluaga/JuanPZuluaga.github.io/blob/master/files/pdf/2021_Contextual%20Semi-Supervised%20Learning:%20An%20Approach%20to%20Leverage%20Air-Surveillance%202021.pdf)

Recommended citation: 

- Cite as: Zuluaga-Gomez, J., Nigmatulina, I., Prasad, A., Motlicek, P., Veselý, K., Kocour, M., Szöke, I. (2021) Contextual Semi-Supervised Learning: An Approach to Leverage Air-Surveillance and Untranscribed ATC Data in ASR Systems. Proc. Interspeech 2021, 3296-3300, doi: 10.21437/Interspeech.2021-1373
- BibTeX:
@inproceedings{zuluagagomez21_interspeech,
  author={Juan Zuluaga-Gomez and Iuliia Nigmatulina and Amrutha Prasad and Petr Motlicek and Karel Veselý and Martin Kocour and Igor Szöke},
  title={{Contextual Semi-Supervised Learning: An Approach to Leverage Air-Surveillance and Untranscribed ATC Data in ASR Systems}},
  year=2021,
  booktitle={Proc. Interspeech 2021},
  pages={3296--3300},
  doi={10.21437/Interspeech.2021-1373}
}
