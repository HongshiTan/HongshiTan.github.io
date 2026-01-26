---
layout: post
title: "RidgeWalker: Perfectly Pipelined Graph Random Walks on FPGAs"
author: "<b>Hongshi Tan</b>, Yao Chen, Xinyu Chen, Qizhen Zhang, Cheng Chen, Weng-Fai Wong, Bingsheng He"
conf_full: "IEEE International Symposium on High-Performance Computer Architecture."
desp: "Full paper accepted by "
conf: "<b>HPCA'26</b>."
tags: "Paper"
---


## Abstract
Graph Random Walks (GRWs) offer efficient approximations of key graph properties and have been widely adopted in many applications. However, GRW workloads are notoriously difficult to accelerate due to their strong data dependencies, irregular memory access patterns, and imbalanced execution behavior. While recent work explores FPGA-based accelerators for GRWs, existing solutions fall far short of hardware potential due to inefficient pipelining and static scheduling. This paper presents RidgeWalker, a high-performance GRW accelerator designed for datacenter FPGAs. The key insight behind RidgeWalker is that the Markov property of GRWs allows decomposition into stateless, fine-grained tasks that can be executed out-of-order without compromising correctness. Building on this, RidgeWalker introduces an asynchronous pipeline architecture with a feedback-driven scheduler grounded in queuing theory, enabling perfect pipelining and adaptive load balancing. We prototype RidgeWalker on datacenter FPGAs and evaluated it across a range of GRW algorithms and real-world graph datasets. Experimental results demonstrate that RidgeWalker achieves an average speedup of 7.0x over state-of-the-art FPGA solutions and 8.1x over GPU solutions, with peak speedups of up to 71.0x and 22.9x, respectively. The source code is publicly available at https://github.com/Xtra-Computing/RidgeWalker.