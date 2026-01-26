---
layout: post
title: " Efficient Graph Data Access for Out-of-Memory GPU Streaming Graph Processing"
author: "Qiange Wang, Yongze Yan, <b>Hongshi Tan</b>, Cheng Chen, Cheng Zhao, Jiaming Tian, Jiaxin Jiang"
conf_full: "Very Large Data Bases."
desp: "Full paper accepted by "
conf: "<b>VLDB'25</b>."
tags: "Paper"
---


## Abstract
Leveraging GPUs’ high parallelism can significantly improve the real-time computation efficiency of streaming graph processing. However, when a large-scale graph exceeds GPU memory capacity, CPU-GPU cooperative processing often results in substantial and irregular CPU-to-GPU data transfer overhead. This stems from the extensive redundant graph accesses during continuous computation, which can hardly be addressed by existing out-of-memory graph processing techniques. In this work, we present Grapin, an out-of-memory GPU streaming graph processing system designed to minimize graph data transfer via two effective techniques for eliminating redundant accesses:(1) Extending advanced incremental processing algorithms to GPUs by converting their heavyweight data dependency processing into GPU-friendly forms, thereby eliminating redundant graph accesses from the computation side; and (2) providing a lightweight yet efficient GPU hot subgraph management framework that finely reuses the frequently accessed dynamic subgraphs on the GPU in a vertex-centric manner. Experimental results demonstrate that Grapin can efficiently process large-scale streaming graphs with billions of edges on a single NVIDIA A5000 GPU. Enabling incremental computation reduces data transfer by 61%, and the integration of GPU hot subgraph reuse further reduces the remaining transfer by 72%, resulting in a total reduction of 89%. Compared with CPU-based solutions, Grapin achieves speedups ranging from 1.8 x to 96.9 x (17.9 x on average). PVLDB Artifact Availability:
