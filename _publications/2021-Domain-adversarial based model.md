---
title: "Domain-Adversarial Based Model with Phonological Knowledge for Cross-Lingual Speech Recognition"
collection: publications
permalink: /publication/2021-Domain-adversarial based model
excerpt: 'This paper is about cross-lingual speech recognition'
date: 2021-12-21
venue: 'Electronics'
paperurl: 'https://www.mdpi.com/2079-9292/10/24/3172'
citation: 'Zhan, Q.; Xie, X.; Hu, C.; Zuluaga-Gomez, J.; Wang, J.; Cheng, H. Domain-Adversarial Based Model with Phonological Knowledge for Cross-Lingual Speech Recognition. Electronics 2021, 10, 3172. https://doi.org/10.3390/electronics10243172'
---

Abstract: Phonological-based features (articulatory features, AFs) describe the movements of the vocal organ which are shared across languages. This paper investigates a domain-adversarial neural network (DANN) to extract reliable AFs, and different multi-stream techniques are used for cross-lingual speech recognition. First, a novel universal phonological attributes definition is proposed for Mandarin, English, German and French. Then a DANN-based AFs detector is trained using source languages (English, German and French). When doing the cross-lingual speech recognition, the AFs detectors are used to transfer the phonological knowledge from source languages (English, German and French) to the target language (Mandarin). Two multi-stream approaches are introduced to fuse the acoustic features and cross-lingual AFs. In addition, the monolingual AFs system (i.e., the AFs are directly extracted from the target language) is also investigated. Experiments show that the performance of the AFs detector can be improved by using convolutional neural networks (CNN) with a domain-adversarial learning method. The multi-head attention (MHA) based multi-stream can reach the best performance compared to the baseline, cross-lingual adaptation approach, and other approaches. More specifically, the MHA-mode with cross-lingual AFs yields significant improvements over monolingual AFs with the restriction of training data size and, which can be easily extended to other low-resource languages.

[Download paper here](https://www.mdpi.com/2079-9292/10/24/3172/pdf)

**Recommended citation**: 

Zhan, Q.; Xie, X.; Hu, C.; Zuluaga-Gomez, J.; Wang, J.; Cheng, H. Domain-Adversarial Based Model with Phonological Knowledge for Cross-Lingual Speech Recognition. Electronics 2021, 10, 3172. https://doi.org/10.3390/electronics10243172.
{: .notice}

- BibTeX:

<pre>
@article{zhan2021domain,
  title={Domain-Adversarial Based Model with Phonological Knowledge for Cross-Lingual Speech Recognition},
  author={Zhan, Qingran and Xie, Xiang and Hu, Chenguang and Zuluaga-Gomez, Juan and Wang, Jing and Cheng, Haobo},
  journal={Electronics},
  volume={10},
  number={24},
  pages={3172},
  year={2021},
  publisher={Multidisciplinary Digital Publishing Institute}
}
</pre>