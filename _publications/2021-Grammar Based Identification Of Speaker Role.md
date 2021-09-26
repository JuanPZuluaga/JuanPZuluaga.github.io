---
title: "Grammar Based Identification Of Speaker Role For Improving ATCO And Pilot ASR"
collection: publications
permalink: /publication/2021-Grammar Based Identification Of Speaker Role
excerpt: 'This paper is about the Automatic Speech Recognition for Air-traffic Control Communications'
date: 2021-10-01
venue: 'ArXiv'
paperurl: 'https://arxiv.org/abs/2108.12175'
citation: 'Prasad, A., Zuluaga-Gomez, J., Motlicek, P., Ohneiser, O., Helmke, H., Sarfjoo, S. and Nigmatulina, I., 2021. Grammar Based Identification Of Speaker Role For Improving ATCO And Pilot ASR. arXiv preprint arXiv:2108.12175.'
---

Assistant Based Speech Recognition (ABSR) for air traffic control is generally trained by pooling both Air Traffic Controller (ATCO) and pilot data. In practice, this is motivated by the fact that the proportion of pilot data is lesser compared to ATCO while their standard language of communication is similar. However, due to data imbalance of ATCO and pilot and their varying acoustic conditions, the ASR performance is usually significantly better for ATCOs than pilots. In this paper, we propose to (1) split the ATCO and pilot data using an automatic approach exploiting ASR transcripts, and (2) consider ATCO and pilot ASR as two separate tasks for Acoustic Model (AM) training. For speaker role classification of ATCO and pilot data, a hypothesized ASR transcript is generated with a seed model, subsequently used to classify the speaker role based on the knowledge extracted from grammar defined by International Civil Aviation Organization (ICAO). This approach provides an average speaker role identification accuracy of 83% for ATCO and pilot. Finally, we show that training AMs separately for each task, or using a multitask approach is well suited for this data compared to AM trained by pooling all data.


[Download paper here](https://github.com/JuanPZuluaga/JuanPZuluaga.github.io/blob/master/files/pdf/2021_Grammar%20Based%20Identification%20Of%20Speaker%20Role%20For%20Im%202021.pdf)

Recommended citation: 

- Harvard: Prasad, A., Zuluaga-Gomez, J., Motlicek, P., Ohneiser, O., Helmke, H., Sarfjoo, S. and Nigmatulina, I., 2021. Grammar Based Identification Of Speaker Role For Improving ATCO And Pilot ASR. arXiv preprint arXiv:2108.12175.

- BibTeX:

<pre>
@article{prasad2021grammar,
  title={Grammar Based Identification Of Speaker Role For Improving ATCO And Pilot ASR},
  author={Prasad, Amrutha and Zuluaga-Gomez, Juan and Motlicek, Petr and Ohneiser, Oliver and Helmke, Hartmut and Sarfjoo, Saeed and Nigmatulina, Iuliia},
  journal={arXiv preprint arXiv:2108.12175},
  year={2021}
}
</pre>