---
title: "RT-BLE: Real-time Multi-Connection Scheduling for Bluetooth Low Energy"
collection: publications
permalink: /publication/RT-BLE
excerpt: 
date: 2023-5-17
venue: 'IEEE INFOCOM'
slidesurl: 'http://sada45.github.io/files/RT-BLE-slides.pdf'
paperurl: 'http://sada45.github.io/files/RT-BLE.pdf'
citation: 'Li, Yeming, et al. "RT-BLE: Real-time Multi-Connection Scheduling for Bluetooth Low Energy." IEEE INFOCOM 2023.'
---

This paper propose RT-BLE, a real-time multi-connection scheduling scheme for BLE. We first formulate the BLE transmission latency in noisy RF environments considering the BLE retransmission mechanism. With this, RT-BLE can get a set of initial connection parameters. Then, RT-BLE uses collision tree based time resource scheduling technology to efficiently manage time resource. Finally, we propose a subrating-based fast connection re-scheduling method to update the connection parameters and the position of anchor points. The result shows RT-BLE can provide reliable service and the error of our model is less than 0.69%. Compare with existing works, the re-scheduling delay is reduced by up to 86.25% and the capacity is up to 4.33× higher.

Open-source Code: https://github.com/sada45/RT-BLE

# Key Idea
1. We segment the time resources as 5ms slots and organize the time resources as a binary-resource tree to indicate the collisions between different connections. 
![RT-BLE Tree](http://sada45.github.io/images/paper_imag/RT-BLE-tree.png "Binary Resource Tree")

2. To achieve quick connection rescheduling, we set the native connection interval to 10ms and using connection subrating to "emulate" different connection intervals. Then, if the anchor point moves even multiple of 10ms, RT-BLE just change the base connection event.
![RT-BLE Rescheduling](http://sada45.github.io/images/paper_imag/RT-BLE-moveanchor.png "Fast Connection Rescheduling")