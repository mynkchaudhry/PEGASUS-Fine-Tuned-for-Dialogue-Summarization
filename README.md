# PEGASUS Fine-Tuned for Dialogue Summarization

## Introduction

This project demonstrates the fine-tuning of the PEGASUS model for the task of dialogue summarization. The fine-tuning is performed on the SAMSum dataset, which consists of conversational dialogues paired with summaries. The workflow includes data preparation, model training, evaluation using ROUGE metrics, and visualization of token lengths. The final model and tokenizer are saved and shared on the Hugging Face Model Hub for public use and further experimentation.

## Model Overview

- **Base Model:** [google/pegasus-cnn_dailymail](https://huggingface.co/google/pegasus-cnn_dailymail)
- **Fine-Tuned On:** SAMSum dataset
- **Model Type:** Sequence-to-Sequence (Seq2Seq)
- **Task:** Dialogue Summarization

## Performance

The fine-tuned PEGASUS model has been evaluated using the ROUGE metric, which measures the quality of generated summaries against reference summaries. The ROUGE scores provide an indication of how well the model performs in summarizing dialogues. The metrics are as follows:

| ROUGE Metric |  Score     |
|--------------|------------|
| ROUGE-1      | `0.015558` |
| ROUGE-2      | `0.000301` |
| ROUGE-L      | `0.015546` |
| ROUGE-Lsum   | `0.015532` |


## Usage

To use the fine-tuned PEGASUS model for summarizing dialogues, follow these steps:

1. **Install Dependencies:** Ensure that you have the necessary libraries installed, including `transformers`, `datasets`, and others.
2. **Load the Model:** Use the Hugging Face `pipeline` function to load the model and tokenizer.
3. **Generate Summaries:** Pass the dialogue text to the model to obtain the summary.

## Installation

To set up the environment and install the required dependencies, use the following command:

```bash
pip install transformers[sentencepiece] datasets sacrebleu rouge_score py7zr huggingface_hub
