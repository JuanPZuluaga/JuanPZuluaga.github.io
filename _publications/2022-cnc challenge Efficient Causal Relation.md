---
title: "IDIAPers @ Causal News Corpus 2022: Efficient Causal Relation Identification Through a Prompt-based Few-shot Approach"
collection: publications
permalink: /publication/2022-cnc challenge Efficient Causal Relation
excerpt: 'In this paper, we describe our participation in the subtask 1 of CASE-2022 (at EMNLP), Event Causality Identification with Casual News Corpus'
date: 2022-12-02
venue: 'ArXiv'
paperurl: 'https://arxiv.org/abs/2209.03895'
citation: 'Burdisso, Sergio and Zuluaga-Gomez, Juan and Villatoro-Tello, Esau and Fajcik, Martin and Singh, Muskaan and Smrz, Pavel and Motlicek, Petr, 2022. IDIAPers@ Causal News Corpus 2022: Efficient Causal Relation Identification Through a Prompt-based Few-shot Approach. The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022). Association for Computational Linguistics'
---

Abstract: In this paper, we describe our participation in the subtask 1 of CASE-2022, Event Causality Identification with Casual News Corpus. We address the Causal Relation Identification (CRI) task by exploiting a set of simple yet complementary techniques for fine-tuning language models (LMs) on a small number of annotated examples (i.e., a few-shot configuration). We follow a prompt-based prediction approach for fine-tuning LMs in which the CRI task is treated as a masked language modeling problem (MLM). This approach allows LMs natively pre-trained on MLM problems to directly generate textual responses to CRI-specific prompts.
We compare the performance of this method against  ensemble techniques trained on the entire dataset. Our best-performing submission was fine-tuned with only 256 instances per class, 15.7% of the all available data, and yet obtained the second-best precision (0.82), third-best accuracy (0.82), and an F1-score (0.85) very close to what was reported by the winner team (0.86). Code available at {https://github.com/idiap/cncsharedtask.


[Download paper here](https://arxiv.org/abs/2209.03895)

**Recommended citation**: 

Burdisso, Sergio and Zuluaga-Gomez, Juan and Villatoro-Tello, Esau and Fajcik, Martin and Singh, Muskaan and Smrz, Pavel and Motlicek, Petr, 2022. IDIAPers@ Causal News Corpus 2022: Efficient Causal Relation Identification Through a Prompt-based Few-shot Approach. The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022). Association for Computational Linguistics.{: .notice}

- BibTeX:

<pre>
@inproceedings{idiap_subtaskA,
    title = "{IDIAPers} @ Causal News Corpus 2022: Efficient Causal Relation Identification Through a Prompt-based Few-shot Approach",
    author = "Burdisso, Sergio and Zuluaga-Gomez, Juan and Fajcik, Martin and Villatoro-Tello, Esau and Singh, Muskaan and Motlicek, Petr and Smrz, Pavel",
    booktitle = "The 5th Workshop on Challenges and Applications of Automated Extraction of Socio-political Events from Text (CASE @ EMNLP 2022)",
    year = "2022",
    publisher = "Association for Computational Linguistics",
}
</pre>