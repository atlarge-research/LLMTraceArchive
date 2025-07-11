# LLM Trace Archive

This repository contains traces of various real-world LLM (Large Language Model) workloads,
leveraged from peer-reviewed articles from various sources. This repository is (constantly) work in progress
and we envision long term progress in collecting and curating LLM traces, also beyond the timeframe and scope
of the thesis on `The Kavier Vision: Exploring Performance, Sustainability, and Efficiency of LLM Ecosystems under 
Inference through Cache-Aware Discrete-Event Simulation`

> For the main repository of the thesis,
> see [On Simulating LLM Ecosystems under Inference](https://github.com/Radu-Nicolae/On-Simulating-LLM-Ecosystems-under-Inference)

---

# 0. Link to Zenodo

The LLM Trace Archive is available at [Zenodo](https://zenodo.org/records/15864776?preview=1&token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6IjM2MGM3MTMzLTBiMTYtNGQ4OS04MDE0LWE4MmE5NjM3NzI2YiIsImRhdGEiOnt9LCJyYW5kb20iOiJmYzFjZjU1OTVmMzRlNTA4YjI1ODc3OWE5ZDkxN2I3MiJ9.k1a2tTuJi9Na2x5xFxmGOBsBX3pDymhYt4MHGqS6ivigu5NMqgVKURVMv1webH1I3gESBy14mDB25J1RhX0klQ).

# 1. Contents

1. Marconi-Kavier Enriched Traces
2. Kavier Traces
3. Marconi Traces
4. LMSys-Chat-1M
5. BurstGPT
6. Azure

---

# 2. Overview of LLM Traces

### 2.1 Marconi-Kavier Enriched Traces

Marconi-Kavier Enriched Traces is an aggregation of the traces release by Pan et al. in their paper
"Marconi: Prefix Caching for the Era of Hybrid LLMs." We have aggregated all these traces into one large trace file,
and adjusted session_ids accordingly. The overall trace has 3,000 session, with a total of ~100,000 requests.

- Kavier source: https://github.com/Radu-Nicolae/On-Simulating-LLM-Ecosystems-under-Inference
- Marconi original trace source: https://zenodo.org/records/14970139

### 2.2 Kavier Traces

The Kavier traces are the first in the community to provide information on the relationship between the input (prefill)
and output (decode) token counts, and the input and output latency of the LLM Ecosystem.

Kavier Traces are a collection of traces that are collected for validating Kavier's accuracy and performance.
To collect these traces, we trace infrastructure from SURF, containing a cluster with an NVIDIA A10,
on which we deploy the latest version of vLLM at the time of tracing (v0.9.0),
serving Llama-3-8B, and maintain the default settings.

We collected traces using [Tracer](https://github.com/atlarge-research/tracer), a utilitarian
tool part of the thesis, which we used to trace the deployed LLM Ecosystem.

- Source Kavier: https://github.com/Radu-Nicolae/On-Simulating-LLM-Ecosystems-under-Inference


### 2.3 Marconi Traces

We identify Pan et al.'s work ["Marconi: Prefix Caching for the Era of Hybrid LLMs"](https://arxiv.org/abs/2411.19379)
as a significant contribution to the
open science community.

The released traces contain information on the input and output token counts, input and output tokens, session_id, and
timestamps.

- Source Marconi traces: https://zenodo.org/records/14970139


### 2.4 LMSys-Chat-1M

LMSys-Chat-1M is leveraged from Zheng et al.'s
work ["LMSys-Chat-1M: A Large-Scale Real-World LLM Conversation Dataset"](https://arxiv.org/pdf/2309.11998),
"a large-scale dataset containing one million real-world conversations with 25 state-of-the-art LLMs.  
This dataset is collected from 210K unique IP addresses in the wild on our Vicuna demo and Chatbot Arena website" (Zheng
et al., 2023).

- LMSys article: https://arxiv.org/pdf/2309.11998


### 2.5 BurstGPT

BurstGPT traces, provided by Wang et al. in their paper ["BurstGPT: A Real-World Workload Dataset to
Optimize LLM Serving Systems"](https://arxiv.org/pdf/2401.17644) contains contain six columns: timestamp, model (e.g.,
GPT-4),
request tokens (i.e., prefill tokens), response tokens (i.e., decode tokens), total tokens, and log type
(e.g., conversation log, API log).
Their trace also reveals failures in the LLM inference process, which are caused by various operational phenomena.

- Source BurstGPT traces: https://github.com/HPMLL/BurstGPT/releases/tag/v1.1


### 2.6 Azure

Stojkovic et al. release, the Azure LLM inference trace *2024) which contains three fields: timestamp, ContextTokens
(number of prefill tokens) and GeneratedTokens (number of decode tokens).

- Source Azure trace: https://github.com/Azure/AzurePublicDataset/blob/master/AzureLLMInferenceDataset2024.md

---

### 3. Acknowledgements
Many thanks to the authors these traces for their significant contributions to the open science community. Many thanks to
the Network Institute at VU Amsterdam and to SURF for providing the infrastructure to collect the Kavier traces.

---

### 4. License
This trace is provided under [MIT License](LICENSE.txt). However, the original traces are provided under their own licenses,
which are available in the original repositories. Please refer to the original repositories for more information on the licenses.