---
layout: post
title: "RidgeBridge: Random Access Optimized Interconnect Architecture for Scalable Graph Random Walks"
author: "<b>Hongshi Tan</b>, Yao Chen, Xinyu Chen, Qizhen Zhang, Weng-Fai Wong, and Bingsheng He."
conf_full: "The 59th IEEE/ACM International Symposium on Microarchitecture. <b>Top-tier conference in computer architecture.</b>"
desp: "Full paper accepted by "
conf: "<b>MICRO'26</b>."
tags: "Paper"
date: 2026-06-27
venue: "2026 59th IEEE/ACM International Symposium on Microarchitecture (MICRO)"
authors:
  - "Hongshi Tan"
  - "Yao Chen"
  - "Xinyu Chen"
  - "Qizhen Zhang"
  - "Weng-Fai Wong"
  - "Bingsheng He"
---

## Abstract
Graph Random Walks (GRWs) are fundamental to applications such as recommendation, fraud detection, and graph-enhanced AI, creating an urgent need for distributed solutions that can keep pace with the exponential growth of real-world graphs. Existing scale-out frameworks predominantly rely on RDMA over Converged Ethernet (RoCEv2), which performs well for bulk-transfer algorithms such as BFS and PageRank, but collapses to only 2--5% link utilization on GRWs due to the massive number of small, unpredictable requests. To address this gap, we propose RidgeBridge, the first interconnect architecture designed specifically for GRWs. RidgeBridge leverages a spine--leaf fabric with well-grounded randomized routing and timeout-driven batching to sustain near line-rate throughput on commodity high-speed Ethernet. We prototype RidgeBridge on FPGAs with 100 GbE and demonstrate linear scalability across nodes with near-optimal goodput utilization, enabling billion-scale GRW processing across multiple FPGAs. When scaling existing GRW accelerators, RidgeBridge scales linearly with the number of FPGAs, delivering an average ~16x speedup over direct scale-out using a state-of-the-art multi-FPGA framework, and up to 3.5x higher throughput compared to the state-of-the-art multi-GPU solution.
