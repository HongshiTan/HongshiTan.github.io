---
layout: post
title: "XtraMAC: An Efficient MAC Architecture for Mixed-Precision LLM Inference on FPGA"
author: "Feng Yu, <b>Hongshi Tan</b>, Yao Chen, Weng-Fai Wong, and Bingsheng He."
conf_full: "The 53rd Annual International Symposium on Computer Architecture. <b>Top-tier conference in computer architecture.</b>"
desp: "Full paper accepted by "
conf: "<b>ISCA'26</b>."
tags: "Paper"
date: 2026-05-07
venue: "The 53rd Annual International Symposium on Computer Architecture (ISCA)"
pdf: "/pdfs/ISCA26-XtraMAC.pdf"
authors:
  - "Feng Yu"
  - "Hongshi Tan"
  - "Yao Chen"
  - "Weng-Fai Wong"
  - "Bingsheng He"
---

## Abstract
The widespread adoption of mixed-precision quantization in large language models (LLMs) has created demand for hardware that can efficiently perform multiply-accumulate (MAC) operations across mixed datatypes and switch datatypes at runtime. Existing FPGA-based MAC solutions fall short due to limitations in fixed-datatype design, inefficient spatial or temporal resource sharing, and poor support for mixed-precision execution. These limitations collectively lead to under-utilization of DSP resources, limiting achievable parallelism and throughput. In this work, we present XtraMAC, a novel MAC architecture that unifies integer, floating-point, and mixed-precision operations within a single, datatype-adaptive microarchitecture. XtraMAC decomposes all supported MAC formats into a shared integer mantissa product with lightweight sign and exponent handling, enabling dynamic operand packing and efficient DSP resource sharing with constant latency and initiation interval of one across all datatypes. Evaluated on an AMD Xilinx U55c FPGA, XtraMAC achieves 1.4-2.0x higher compute density, reduces per-operation LUT, FF, and DSP consumption by 27-51%, and delivers up to 1.9x greater energy efficiency and 1.2x speedup on representative mixed-precision LLM workloads. The implementation of XtraMAC is open-sourced at [Github](https://github.com/Xtra-Computing/XtraMAC).

<a href="/pdfs/ISCA26-XtraMAC.pdf">[Paper]</a>
