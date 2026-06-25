---
layout: post
title: "Approaching Shannon Bound with Lossless LLM Weight Compression"
author: "<b>Hongshi Tan</b>, Yao Chen, Gustavo Alonso, Weng-Fai Wong, and Bingsheng He."
conf_full: "The 53rd Annual International Symposium on Computer Architecture. <b>Top-tier conference in computer architecture.</b>"
desp: "Full paper accepted by "
conf: "<b>ISCA'26</b>."
tags: "Paper"
date: 2026-06-14
venue: "The 53rd Annual International Symposium on Computer Architecture (ISCA)"
pdf: "/pdfs/ISCA26-ShannonBound.pdf"
authors:
  - "Hongshi Tan"
  - "Yao Chen"
  - "Gustavo Alonso"
  - "Weng-Fai Wong"
  - "Bingsheng He"
---

## Abstract
Large language models (LLMs) now scale to trillions of parameters, driving weight storage into the terabyte regime and creating an acute mismatch with GPU memory capacity. Although lossless compression is widely effective in other domains, it remains underutilized in LLM systems. Through a comprehensive entropy study across models from 1.5B to 405B parameters and numeric formats ranging from bf16 to int4 and AWQ/SQ8, we find that LLM weights contain far less intrinsic randomness than their stored bitwidth implies, their effective entropy is 2-10x lower, indicating that up to a 10x footprint reduction is theoretically achievable without altering any weight values. Leveraging this insight, we introduce a tile-level, on-the-fly lossless decompression framework based on Asymmetric Numeral Systems that aligns decoding with the GEMM tiling pattern of GPU inference. Our design achieves bit-rates within 0.01-0.1 bits of the Shannon limit across a wide range of LLM numerical formats, demonstrating that nearly all statistical redundancy is eliminated. Integrated into the SGLang serving framework with multi-GPU support, our approach increases the maximum batch size of Qwen-14B from 47 to 75, improving throughput by up to 1.2x. On Mixtral-176B, the feasible batch size increases from 20 to 95 (4.8x), yielding up to 1.6x throughput improvement. Compared to state-of-the-art lossless compression approaches NeuZip and DFloat11, our design further improves throughput by up to 11x.

<a href="/pdfs/ISCA26-ShannonBound.pdf">[Paper]</a>
