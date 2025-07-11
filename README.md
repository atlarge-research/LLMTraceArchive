# LLM Trace Archive

This repository contains traces of various real-world LLM (Large Language Model) workloads,
leveraged from peer-reviewed articles from various sources. This repository is (constantly) work in progress
and we envision long term progress in collecting and curating LLM traces, also beyond the timeframe and scope 
of the thesis on `The Kavier Vision: Exploring Performance, Sustainability, and Efficiency of LLM Ecosystems under Inference through Cache-Aware Discrete-Event Simulation`

> For the parent repository, see ... todo add here.


---

## Contents
- Marconi-Kavier Enriched Traces
- Kavier Traces
- Marconi Traces
- LMSys-Chat-1M
- BurstGPT  
- Azure

---

#### Marconi-Kavier Enriched Traces
Marconi-Kavier Enriched Traces is an aggregation of the traces release by Pan et al. in their paper 
"Marconi: Prefix Caching for the Era of Hybrid LLMs." We have aggregated all these traces into one large trace file,
and adjusted session_ids accordingly. The overall trace has 3,000 session, with a total of ~100,000 requests.

#### Kavier Traces
Kavier Traces are a collection of traces that are collected for validating Kavier's accuracy and performance.
To collect these traces, we trace infrastructure from SURF, containing a cluster with an NVIDIA A10,
on which we deploy the latest version of vLLM at the time of tracing (v0.9.0), 
serving Llama-3-8B, and maintain the default settings.

We 




which are used to evaluate and validate the Kavier system. The traces are collected from different sources and represent a variety of LLM applications and workloads.
In our work, we use a set of real-world LLM Traces to validate Kavier, and to run simulation-driven experiments with
real-world traces.

Due to storage limitation from GitHub, we host the LLM Traces on Zenodo.

The LLM Trace Archive is available at [Zenodo](https://zenodo.org/record/15858418).

## Available Traces
The LLM Trace Archive contains the following traces:

### [Marconi Traces](Marconi Traces)
Source: Pan et al., 


2. [Marconi Enriched]()