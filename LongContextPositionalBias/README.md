# Long Context Positional Bias

This project investigates positional bias in instruction-tuned Large Language Models (LLMs) when processing long contexts. Specifically, it analyzes phenomena such as **primacy effects**, **recency effects**, and **performance degradation in middle-context retrieval**.

## Overview

We evaluate how well models can retrieve a specific target fact (a five-digit identifier code for a fictional project) hidden amidst varying numbers of distractor facts. The difficulty of the retrieval task is scaled by introducing:
- Confusable project names (e.g., Aurora vs. Aurora-Prime)
- Semantically similar distractor keys (e.g., "access code" vs. "identifier token")
- Variable context lengths (Short: 20 distractors, Medium: 60 distractors, Long: 120 distractors)

The location of the target evidence is systematically varied across three positions: **Beginning**, **Middle**, and **End**.

## Evaluated Models

The experiments evaluate models of varying capacities to observe how positional bias interacts with model size and capability:
- TinyLlama
- Llama 3.2 1B
- Llama 3.2 3B
- Llama 3 8B

## Methodology

- **Task**: Zero-shot question answering prompting the model to extract exactly one five-digit numerical value.
- **Evaluation Metric**: Exact-match accuracy.
- **Inference Setup**: Deterministic decoding (temperature=0, top-p=1) to ensure reproducibility.

## Code Structure

- `algorithm/Code.ipynb`: The primary notebook containing the experimental setup, data generation pipeline, model evaluation logic, and visualization code.

## How to Run

1. Open `algorithm/Code.ipynb` in your environment.
2. Ensure you have the required dependencies for running local inference (e.g., Hugging Face Transformers or an equivalent local API endpoint).
3. The notebook will guide you through dataset generation, executing the model evaluations, and visualizing the aggregated positional bias metrics.
