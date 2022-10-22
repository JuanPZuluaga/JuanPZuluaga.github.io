---
title: "IDIAPers @ Causal News Corpus 2022: Extracting Cause-Effect-Signal Triplets via Pre-trained Autoregressive Language Model"
collection: publications
permalink: /publication/2022-CNC challenge Extracting Cause Effect Signal
excerpt: 'In this paper, we describe our participation in the subtask 2 of CASE-2022 (at EMNLP), Event Causality Identification with Casual News Corpus'
date: 2022-12-02
venue: 'ArXiv'
paperurl: 'https://arxiv.org/abs/2209.03891'
citation: 'Fajcik, Martin and Singh, Muskaan and Zuluaga-Gomez, Juan and Villatoro-Tello, Esau and Burdisso, Sergio and Motlicek, Petr and Smrz, Pavel, 2022. IDIAPers @ Causal News Corpus 2022: Extracting Cause-Effect-Signal Triplets via Pre-trained Autoregressive Language Model. The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022). Association for Computational Linguistics'
---

Abstract: In this paper, we describe our shared task submissions for Subtask 2 in CASE-2022, Event Causality Identification with Casual News Corpus. The challenge focused on the automatic detection of all cause-effect-signal spans present in the sentence from news-media. We detect cause-effect-signal spans in a sentence using T5, a pre-trained autoregressive language model. We iteratively identify all cause-effect-signal span triplets, always conditioning the prediction of the next triplet on the previously predicted ones. To predict the triplet itself, we consider different causal relationships such as cause -> effect -> signal. Each triplet component is generated via a language model conditioned on the sentence, the previous parts of the current triplet, and previously predicted triplets.
Despite training on an extremely small dataset of 160 samples, our approach achieved competitive performance, being placed second in the competition. Furthermore, we show that assuming either cause ->efffect or effect -> cause order achieves similar results. Code at https://github.com/idiap/cncsharedtask.


[Download paper here](https://arxiv.org/abs/2209.03891)

**Recommended citation**: 

Fajcik, Martin and Singh, Muskaan and Zuluaga-Gomez, Juan and Villatoro-Tello, Esau and Burdisso, Sergio and Motlicek, Petr and Smrz, Pavel, 2022. IDIAPers @ Causal News Corpus 2022: Extracting Cause-Effect-Signal Triplets via Pre-trained Autoregressive Language Model. The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022). Association for Computational Linguistics.{: .notice}

- BibTeX:

<pre>
@inproceedings{idiap_subtaskB,
    title = "IDIAPers @ Causal News Corpus 2022: Extracting Cause-Effect-Signal Triplets via Pre-trained Autoregressive Language Model",
    author = "Fajcik, Martin and Singh, Muskaan and Zuluaga-Gomez, Juan and Villatoro-Tello, Esaú and Burdisso, Sergio and Motlicek, Petr and Smrz, Pavel",
    booktitle = "The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022)",
    year = "2022",
    publisher = "Association for Computational Linguistics",
}
</pre>