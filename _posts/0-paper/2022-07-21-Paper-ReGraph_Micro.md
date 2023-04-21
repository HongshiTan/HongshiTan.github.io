---
layout: post
title: "ReGraph: Scaling Graph Processing on HBM-enabled FPGAs with Heterogeneous Pipelines"
author: "Xinyu Chen, Yao Chen, Feng Cheng, <b>Hongshi Tan</b>, Bingsheng He, and Weng-Fai Wong."
conf_full: "The International Symposium on Microarchitecture."
desp: "Full paper accepted by "
conf: "<b>MICRO'22</b> (Acceptance rate: 22%)."
tags: "Paper"
---


## Abstract
The use of FPGAs for efficient graph processing has attracted significant interest. Recent memory subsystem upgrades including the introduction of HBM in FPGAs promise to further alleviate memory bottlenecks. However, modern multi-channel HBM requires much more processing pipelines to fully utilize its bandwidth potential.
Due to insufficient resource efficiency, existing designs do not scale well, resulting in underutilization of the HBM facilities even when all other resources are fully consumed.

In this paper, we propose ReGraph, which customizes heterogeneous pipelines for diverse workloads in graph processing, achieving better resource efficiency, instantiating more pipelines and improving performance.
We first identify workload diversity exists in processing graph partitions and classify them into two types: dense partitions established with good locality and sparse partitions with poor locality. 
Subsequently, we design two types of pipelines: Little pipelines with burst memory access technique to process dense partitions and Big pipelines tolerating random memory access latency to handle sparse partitions.
Unlike existing monolithic pipeline designs, our heterogeneous pipelines are tailored for more specific workload characteristics and hence more lightweight, allowing the architecture to scale up more effectively with limited resources.
We also present a graph-aware task scheduling method that schedules partitions to the right pipeline types, generates the most efficient pipeline combination and balances workloads. ReGraph surpasses state-of-the-art FPGA accelerators by 1.6x--5.9x in performance and 2.5x--12.3x in resource efficiency. 