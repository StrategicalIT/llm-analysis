# llm-analysis

> Latency and Memory Analysis of Transformer Models for Training and Inference


## Overview

Many formulas or equations are floating around in papers, blogs, etc., about how to calculate training or inference latency and memory for Large Language Models (LLMs) or Transformers. Rather than doing math on papers or typing in Excel sheets, `let's automate the boring stuff with llm-analysis` :gear:!

Given the specified model, GPU, data type, and parallelism configurations, llm-analysis estimates the latency and memory usage of LLMs for training or inference. With llm-analysis, one can easily try out different training/inference setups theoretically, and better understand the system performance for different scenarios.

llm-analysis helps answer questions such as:
- what batch size, data type, parallelism scheme to use to get a `feasible` (not getting OOM) and `optimal` (maximizing throughput with a latency constraint) setup for training or inference
- `time` it takes with the given setup to do training or inference and the `cost` (GPU-hours)
- how the latency/memory changes if using a different model, GPU type, number of GPU, data type for weights and activations, parallelism configuration (suggesting the performance benefit of `modeling change`, `hardware improvement`, `quantization`, `parallelism`, etc.)


- To install this development build:

  ```sh
  pip install --upgrade git+https://github.com/strategicalit/llm-analysis.git@main
  ```

