---
title: "Improving callsign recognition with air-surveillance data in air-traffic communication"
collection: publications
permalink: /publication/2021-Improving-callsign-recognition
excerpt: 'This paper is about the Automatic Speech Recognition in Air-traffic Control Communications'
date: 2021-10-01
venue: 'ArXiv'
paperurl: 'https://arxiv.org/abs/2108.12156'
citation: 'Nigmatulina, I., Braun, R., Zuluaga-Gomez, J. and Motlicek, P., 2021. Improving callsign recognition with air-surveillance data in air-traffic communication. arXiv preprint arXiv:2108.12156.'
---

Abstract: Automatic Speech Recognition (ASR) can be used as the assistance of speech communication between pilots and air-traffic controllers. Its application can significantly reduce the complexity of the task and increase the reliability of transmitted information. Evidently, high accuracy predictions are needed to minimize the risk of errors. Especially, high accuracy is required in recognition of key information, such as commands and callsigns, used to navigate pilots. Our results prove that the surveillance data containing callsigns can help to considerably improve the recognition of a callsign in an utterance when the weights of probable callsign n-grams are reduced per utterance. In this paper, we investigate two approaches: (1) G-boosting, when callsigns weights are adjusted at language model level (G) and followed by the dynamic decoder with an on-the-fly composition, and (2) lattice rescoring when callsign information is introduced on top of lattices generated using a conventional decoder. Boosting callsign n-grams with the combination of two methods allowed us to gain 28.4% of absolute improvement in callsign recognition accuracy and up to 74.2% of relative improvement in WER of callsign recognition.


[Download paper here](https://github.com/JuanPZuluaga/JuanPZuluaga.github.io/blob/master/files/pdf/2021_Improving%20callsign%20recognition%20with%20air-surv%202021.pdf)

**Recommended citation**: 

Nigmatulina, I., Braun, R., Zuluaga-Gomez, J. and Motlicek, P., 2021. Improving callsign recognition with air-surveillance data in air-traffic communication. arXiv preprint arXiv:2108.12156.
{: .notice}

- BibTeX:

<pre>
@article{nigmatulina2021improving,
  title={Improving callsign recognition with air-surveillance data in air-traffic communication},
  author={Nigmatulina, Iuliia and Braun, Rudolf and Zuluaga-Gomez, Juan and Motlicek, Petr},
  journal={arXiv preprint arXiv:2108.12156},
  year={2021}
}
</pre>