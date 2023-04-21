---
layout: post
title: "ThunderGP: HLS-based Graph Processing Framework on FPGAs."
author: "Xinyu Chen, <b>Hongshi Tan</b>, Yao Chen, Bingsheng He, Weng-Fai Wong and Deming Chen."
conf_full: "The 29th ACM/SIGDA International Symposium on Field-Programmable Gate Arrays. <b>Top-tier conference in FPGA.</b>"
desp: "Full paper accepted by "
conf: "<b>FPGA'21</b> (Acceptance rate: 20%)."
tags: "Paper"
---

## Abstract
In this paper, we propose ThundeRiNG, a resource-efficient and high-throughput system for generating multiple independent sequences of random numbers (MISRN) on FPGAs. Generating MISRN can be a time-consuming step in many applications such as numeric computation and approximate computing. Despite that decades of studies on generating a single sequence of random numbers on FPGAs have achieved very high throughput and high quality of randomness, existing MISRN approaches either suffer from heavy resource consumption or fail to achieve statistical independence among sequences. In contrast, ThundeRiNG resolves the dependence by using a resource-efficient decorrelator among multiple sequences, guaranteeing a high statistical quality of randomness. Moreover, ThundeRiNG develops a novel state sharing among a massive number of pseudo-random number generator instances on FPGAs. The experimental results show that ThundeRiNG successfully passes the widely used statistical test, TestU01, only consumes a constant number of DSPs (less than 1% of the FPGA resource capacity) for generating any number of sequences, and achieves a throughput of 655 billion random numbers per second. Compared to the state-of-the-art GPU library, ThundeRiNG demonstrates a 10.62x speedup on MISRN and delivers up to 9.15x performance and
26.63x power efficiency improvement on two applications (pi estimation and Monte Carlo option pricing). This work is open-sourced on [Github](https://github.com/Xtra-Computing/ThunderGP.)