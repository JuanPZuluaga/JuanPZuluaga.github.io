---
title: "Boosting of Contextual Information in ASR for Air-Traffic Call-Sign Recognition"
collection: publications
permalink: /publication/2021-Boosting of Contextual Information in ASR for Air-Traffic Call-Sign Recognition
excerpt: 'This paper is about the Automatic Speech Recognition for Air-traffic Control Communications'
date: 2021-08-28
venue: 'Interspeech 2021'
paperurl: 'https://isca-speech.org/archive/interspeech_2021/kocour21_interspeech.html'
citation: 'Kocour, M., Veselý, K., Blatt, A., Gomez, J.Z., Szöke, I., Černocký, J., Klakow, D., Motlicek, P. (2021) Boosting of Contextual Information in ASR for Air-Traffic Call-Sign Recognition. Proc. Interspeech 2021, 3301-3305, doi: 10.21437/Interspeech.2021-1619.'
---

Contextual adaptation of ASR can be very beneficial for multi-accent and often noisy Air-Traffic Control (ATC) speech. Our focus is call-sign recognition, which can be used to track conversations of ATC operators with individual airplanes. We developed a two-stage boosting strategy, consisting of HCLG boosting and Lattice boosting. Both are implemented as WFST compositions and the contextual information is specific to each utterance. In HCLG boosting we give score discounts to individual words, while in Lattice boosting the score discounts are given to word sequences. The context data have origin in surveillance database of OpenSky Network. From this, we obtain lists of call-signs that are made more likely to appear in the best hypothesis of ASR. This also improves the accuracy of the NLU module that recognizes the call-signs from the best hypothesis of ASR.


[Download paper here](https://github.com/JuanPZuluaga/JuanPZuluaga.github.io/blob/master/files/pdf/2021_Boosting%20of%20contextual%20information%20in%20ASR%20for_2021.pdf)

Recommended citation: 

- Cite as: Kocour, M., Veselý, K., Blatt, A., Gomez, J.Z., Szöke, I., Černocký, J., Klakow, D., Motlicek, P. (2021) Boosting of Contextual Information in ASR for Air-Traffic Call-Sign Recognition. Proc. Interspeech 2021, 3301-3305, doi: 10.21437/Interspeech.2021-1619

- BibTeX:

<pre>
@inproceedings{kocour21_interspeech,
  author={Martin Kocour and Karel Veselý and Alexander Blatt and Juan Zuluaga Gomez and Igor Szöke and Jan Černocký and Dietrich Klakow and Petr Motlicek},
  title={{Boosting of Contextual Information in ASR for Air-Traffic Call-Sign Recognition}},
  year=2021,
  booktitle={Proc. Interspeech 2021},
  pages={3301--3305},
  doi={10.21437/Interspeech.2021-1619}
}
</pre>