---
layout: page
title: Research
---

My research is in cloud-native and distributed data processing systems, with a focus on network communication and emerging data center hardware. I study how DPUs (SmartNICs) can help data systems move and process data more efficiently, and how to design practical abstractions and optimizations for heterogeneous hardware.

## Publications

### Data processing with DPUs

**[Making Sense of DPU Performance for Cloud Data Processing](https://fardatalab.org/publications.html){: .publication-link}** — SoCC 2026.  
<u><strong>Jiasheng Hu</strong></u>, Chihan Cui, Yuanfan Chen, Philip A. Bernstein, Jialin Li, Qizhen Zhang.

We benchmark recent production DPUs to characterize their performance and investigate where DPU offloading can benefit database workloads.

**[dpKernels: Harvesting DPU Compute Resources for Data-path Efficiency in Cloud Data Processing](https://fardatalab.org/vldb26-dpkernels.pdf){: .publication-link}** — VLDB 2026. [Code](https://github.com/fardatalab/dpKernels){: .code-link}.  
<u><strong>Jiasheng Hu</strong></u>, Kaiwen Zheng, Anna Li, Sidharth Sankhe, Philip A. Bernstein, Qizhen Zhang.

We introduce dpKernels, a set of portable primitives for accessing DPU accelerators and SoC cores, and dpManager, which manages and schedules those resources across DPU platforms.

**[PD3: Prefetching Data with DPUs for Disaggregated Memory](https://fardatalab.org/nsdi26-pd3.pdf){: .publication-link}** — NSDI 2026. [Code](https://github.com/fardatalab/PD3){: .code-link}.  
Sidharth Sankhe, Felix Zhang, Umayrah Chonee, Sherman Lim, <u><strong>Jiasheng Hu</strong></u>, Jialin Li, Qizhen Zhang.

PD3 uses DPUs and application information to prefetch data from disaggregated memory, avoiding compute-server cache misses and offloading network and DMA work from the host.

**[DPDPU: Data Processing with DPUs](https://fardatalab.org/cidr25-hu.pdf){: .publication-link}** — CIDR 2025.  
<u><strong>Jiasheng Hu</strong></u>, Philip A. Bernstein, Jialin Li, Qizhen Zhang.

This vision paper outlines opportunities and challenges in using DPUs for data processing and proposes a framework for organizing DPU-enabled system designs.

**[DDS: DPU-optimized Disaggregated Storage](https://arxiv.org/pdf/2407.13618){: .publication-link}** — VLDB 2024. [Code](https://github.com/microsoft/dds){: .code-link}.  
Qizhen Zhang, Philip Bernstein, Badrish Chandramouli, <u><strong>Jiasheng Hu</strong></u>, Yiming Zheng.

DDS uses a DPU to process disaggregated-storage requests, combining DMA, zero-copy, and userspace I/O to reduce latency and host CPU use with minimal DBMS changes.

### Database storage and I/O

**[Tuning the Lookahead Distance for PostgreSQL Asynchronous IO](https://www.vldb.org/pvldb/vol19/p3982-wu.pdf){: .publication-link}** — VLDB 2026 Industrial Track.  
[Wentao Wu](https://www.microsoft.com/en-us/research/people/wentwu), <u><strong>Jiasheng Hu</strong></u>, Manoj Syamala, Andres Freund, Vivek Narasayya.

We adaptively tune the lookahead distance used by asynchronous database reads, using I/O completion-time feedback to improve prefetching decisions.
