---
title: "Automatic Call Sign Detection: Matching Air Surveillance Data with Air Traffic Spoken Communications"
collection: publications
permalink: /publication/2020-Automatic Call Sign Detection: Matching Air Surveillance Data
excerpt: 'This paper is about the Automatic Speech Recognition for Air-traffic Control Communications'
date: 2020-12-03
venue: 'Proceedings of 8th OpenSky Symposium 2020'
paperurl: 'https://www.mdpi.com/2504-3900/59/1/14'
citation: 'Zuluaga-Gomez, J.; Veselý, K.; Blatt, A.; Motlicek, P.; Klakow, D.; Tart, A.; Szöke, I.; Prasad, A.; Sarfjoo, S.; Kolčárek, P.; Kocour, M.; Černocký, H.; Cevenini, C.; Choukri, K.; Rigault, M.; Landis, F. Automatic Call Sign Detection: Matching Air Surveillance Data with Air Traffic Spoken Communications. Proceedings 2020, 59, 14. https://doi.org/10.3390/proceedings2020059014'
---

Voice communication is the main channel to exchange information between pilots and Air-Traffic Controllers (ATCos). Recently, several projects have explored the employment of speech recognition technology to automatically extract spoken key information such as call signs, commands, and values, which can be used to reduce ATCos’ workload and increase performance and safety in Air-Traffic Control (ATC)-related activities. Nevertheless, the collection of ATC speech data is very demanding, expensive, and limited to the intrinsic speakers’ characteristics. As a solution, this paper presents ATCO2, a project that aims to develop a unique platform to collect, organize, and pre-process ATC data collected from air space. Initially, the data are gathered directly through publicly accessible radio frequency channels with VHF receivers and LiveATC, which can be considered as an “unlimited-source” of low-quality data. The ATCO2 project explores employing context information such as radar and air surveillance data (collected with ADS-B and Mode S) from the OpenSky Network (OSN) to correlate call signs automatically extracted from voice communication with those available from ADS-B channels, to eventually increase the overall call sign detection rates. More specifically, the timestamp and location of the spoken command (issued by the ATCo by voice) are extracted, and a query is sent to the OSN server to retrieve the call sign tags in ICAO format for the airplanes corresponding to the given area. Then, a word sequence provided by an automatic speech recognition system is fed into a Natural Language Processing (NLP) based module together with the set of call signs available from the ADS-B channels. The NLP module extracts the call sign, command, and command arguments from the spoken utterance.

[Download paper here](https://github.com/JuanPZuluaga/JuanPZuluaga.github.io/blob/master/files/pdf/2020_Automatic%20Call%20Sign%20Detection:%20Matching%20Air%20Surveillance_2020.pdf)

Recommended citation: 

- Cite as: Zuluaga-Gomez, J.; Veselý, K.; Blatt, A.; Motlicek, P.; Klakow, D.; Tart, A.; Szöke, I.; Prasad, A.; Sarfjoo, S.; Kolčárek, P.; Kocour, M.; Černocký, H.; Cevenini, C.; Choukri, K.; Rigault, M.; Landis, F. Automatic Call Sign Detection: Matching Air Surveillance Data with Air Traffic Spoken Communications. Proceedings 2020, 59, 14. https://doi.org/10.3390/proceedings2020059014


- BibTeX:
@inproceedings{zuluaga2020automatic_callsign,
  title={Automatic call sign detection: Matching air surveillance data with air traffic spoken communications},
  author={Zuluaga-Gomez, Juan and Vesel{\`y}, Karel and Blatt, Alexander and Motlicek, Petr and Klakow, Dietrich and Tart, Allan and Sz{\"o}ke, Igor and Prasad, Amrutha and Sarfjoo, Saeed and Kol{\v{c}}{\'a}rek, Pavel and others},
  booktitle={Multidisciplinary Digital Publishing Institute Proceedings},
  volume={59},
  number={1},
  pages={14},
  year={2020}
}
