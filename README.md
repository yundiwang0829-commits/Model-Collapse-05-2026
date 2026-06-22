# Slowing down Early Stage Model Collapse in Language Models through Diversity-Enhancing Decoding

Coursework project containing the report, notebooks, datasets, and experiment results for reproducing the experiments.


## Overview

This repository contains a coursework project on early-stage model collapse in recursive Chinese text generation. The project investigates whether diversity-enhancing decoding strategies can slow down collapse-like symptoms when model-generated continuations are repeatedly reused for fine-tuning.

We compare greedy decoding, temperature sampling, top-p sampling, and Diverse Beam Search using Qwen1.5-0.5B fine-tuned on Chinese Wikipedia data. The current version is a small-scale experimental study, with planned extensions to larger language models, longer recursive chains, and broader Chinese corpora.


## Key Features

- Recursive fine-tuning pipeline for studying early-stage model collapse.
- Chinese Wikipedia continuation task using Qwen1.5-0.5B.
- Comparison of greedy, temperature sampling, top-p sampling, and Diverse Beam Search.
- Evaluation with validation/test perplexity, Distinct-1/2, Self-BLEU, and severe repetition rate.
- Supplementary qualitative examples across decoding strategies and recursive rounds.

## Experimental Pipeline

Human Chinese Wikipedia data  
→ fine-tune Qwen1.5-0.5B  
→ generate continuations with a decoding strategy  
→ construct partially synthetic training data  
→ fine-tune again  
→ repeat for five recursive rounds  
→ evaluate model performance and generation diversity

## Future Work

This repository is currently based on a coursework project. Future development will focus on:

- scaling the experiment to larger language models;
- testing longer recursive fine-tuning chains;
- using broader and less structured Chinese corpora;
- adding semantic, syntactic, and factuality-based evaluation metrics;
- comparing decoding with filtering, repetition penalties, and human-data mixing strategies;
- preparing the project for a more complete research paper.


## Structure

- `codes/`: Google Colab notebooks for dataset preparation and experiment execution.
- `dataset/`: train, validation, and test JSONL datasets.
- `results/`: generated examples and metrics.
- `XQTX8_Report.pdf`: coursework report.
- `CRediT contribution statement.docx`: contribution statement.

## Running the Notebooks

The notebooks are designed to run in Google Colab with a T4 GPU.

- `codes/dataset.ipynb` prepares the Chinese Wikipedia datasets and saves the train, validation, and test sets.
- `codes/main.ipynb` runs the experiments, reads the prepared datasets, and writes outputs to `results/`.
