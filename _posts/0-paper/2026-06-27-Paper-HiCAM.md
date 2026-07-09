---
layout: post
title: "HiCAM: Accelerating Parallel Triangle Counting via Bit-Efficient Content-Addressable Memory on FPGA"
author: "Yao Chen, Feng Yu, <b>Hongshi Tan</b>, Xuanhua Shi, Weng-Fai Wong, Bingsheng He, and Hai Jin."
conf_full: "The 59th IEEE/ACM International Symposium on Microarchitecture. <b>Top-tier conference in computer architecture.</b>"
desp: "Full paper accepted by "
conf: "<b>MICRO'26</b>."
tags: "Paper"
date: 2026-06-27
venue: "2026 59th IEEE/ACM International Symposium on Microarchitecture (MICRO)"
authors:
  - "Yao Chen"
  - "Feng Yu"
  - "Hongshi Tan"
  - "Xuanhua Shi"
  - "Weng-Fai Wong"
  - "Bingsheng He"
  - "Hai Jin"
---

## Abstract
Triangle counting is a fundamental primitive in large-scale graph analytics, yet its execution is bottlenecked by irregular memory access patterns and limited parallelism on conventional architectures. Prior FPGA-based CAM accelerators decouple data representation from matching semantics, wasting on-chip resources and requiring decompression before search. We present HiCAM, a software-hardware co-designed FPGA overlay that unifies graph data compression and associative matching into a single compressed-domain pipeline. HiCAM introduces a parameterizable locality-aware tuple encoding that packs multiple sorted vertex IDs into fixed-width entries aligned with the DSP datapath, and co-designs a bit-efficient CAM cell that searches compressed tuples directly---without runtime decompression. To handle the skewed degree distributions of real-world graphs, HiCAM employs run-time adaptive CAM grouping that trades parallelism for storage depth on a per-vertex basis, and a two-level memory-channel-aware partitioning framework for balanced multi-channel execution. Experimental results on a diverse suite of real-world datasets demonstrate that HiCAM achieves up to 10.6x speedup and 5.8x energy reduction over state-of-the-art FPGA baselines, and outperforms optimized 32-core CPU solutions by up to 3.8x in speed and 9.0x in energy efficiency.
