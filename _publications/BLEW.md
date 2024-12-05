---
title: "Combating BLEWeak Links with Adaptive Symbol Extension and DNN-based Demodulation"
collection: publications
permalink: /publication/RT-BLE
excerpt: 
date: 2024-5-20
venue: 'IEEE INFOCOM'
paperurl: 'http://sada45.github.io/files/BLEW.pdf'
citation: 'Li, Yeming, et al. "Combating BLEWeak Links with Adaptive Symbol Extension and DNN-based Demodulation." ACM SenSys  2024.'
---

# Errata
The Eq. 10 should be corrected as $n_{\text{AIP}} = \left\lceil {(n_{\text{max}}+N_{\text{f}}) \times 8} / {n_{\text{bit}}} \right\rceil$.
This correct the goodput calculation in the Tab. 1 and Fig. 17, should be:
![Goodput](http://sada45.github.io/images/paper_imag/BLEW-throughput.png#pic_center =x400)
![Energy](http://sada45.github.io/images/paper_imag/BLEW-energy.png#pic_center =x400)


# Key Idea

1. The short BLE symbol can be easily overwhelmed by the noise and interference. BLEW can extend the symbol by repeating transmit each symbol for several times. 
![Symbol Extension](http://sada45.github.io/images/paper_imag/BLEW-extent.png "Using Symbol Extension to Combat Weak Links")

2. We use a DNN model to extract both time-domain and frequency-domain features to demodulate the symbols.
![DNN-based Demodulator](http://sada45.github.io/images/paper_imag/BLEW-DNN.png "DNN-based Demodulator")