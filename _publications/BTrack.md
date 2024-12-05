---
title: "BLE Location Tracking Attacks by Exploiting Frequency Synthesizer Imperfection"
collection: publications
permalink: /publication/RT-BLE
excerpt: 
date: 2024-5-20
venue: 'IEEE INFOCOM'
paperurl: 'http://sada45.github.io/files/BTrack.pdf'
citation: 'Li, Yeming, et al. "BLE Location Tracking Attacks by Exploiting Frequency Synthesizer Imperfection." IEEE INFOCOM 2024.'
---

In this paper, we introduce a novel physical-layer fingerprint named Transient Dynamic Fingerprint (TDF), which originated from the negative feedback control process of the frequency synthesizer. Because of the hardware imperfection, the dynamic features of the frequency synthesizer are different, making TDF unique among different devices, even with the same model. Furthermore, TDF keeps stable under different thermal conditions. Based on TDF, we propose BTrack, a practical BLE device tracking system and evaluate its tracking performance in different environments. The results show BTrack works well once BLE beacons are effectively received. The identification accuracy is 35.38%-57.41% higher than the existing method, and stable over temperatures, distances, and locations.

Open-source Code: https://github.com/sada45/BTrack

# Key Idea
When we using a USRP to demodulate the BLE signal, we find there is always a phase change before the preamble.
![TDF](http://sada45.github.io/images/paper_imag/BTrack-phase.png "Transient Phase Change Before Preamble")

It is originated from the negative response procedure in the frequency synthesizer. Because of the hardware imperfection, the transient phase of each chip is different and can be used to identify different devices.
![Frequency Synthesizer](http://sada45.github.io/images/paper_imag/BTrack-frequency.png "Frequency Synthesizer of BLE")
