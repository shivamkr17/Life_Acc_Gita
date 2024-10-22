# Fine-Tuning LLaMA-2 Model using QLoRA

This repository contains code and instructions for fine-tuning the LLaMA-2-7b-chat model using QLoRA (Quantized Low-Rank Adaptation) on a custom dataset. By leveraging Parameter-Efficient Fine-Tuning (PEFT), this approach significantly reduces the hardware requirements, allowing for fine-tuning of large models with minimal VRAM.

## Table of Contents
- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Dataset Preparation](#dataset-preparation)
- [Fine-Tuning with QLoRA](#fine-tuning-with-qlora)
- [Training Configuration](#training-configuration)
- [Results and Evaluation](#results-and-evaluation)
- [How to Use the Fine-Tuned Model](#how-to-use-the-fine-tuned-model)
- [Acknowledgements](#acknowledgements)

## Project Overview

The objective of this project is to fine-tune the LLaMA-2-7b-chat model using a custom dataset formatted according to the LLaMA-2 prompt template. We utilize QLoRA to enable efficient fine-tuning in a memory-constrained environment, using 4-bit precision and LoRA (Low-Rank Adaptation) techniques.

This fine-tuning process is demonstrated using the [OpenAssistant-Guanaco](https://huggingface.co/datasets/timdettmers/openassistant-guanaco) dataset reformatted according to the LLaMA-2 prompt format, along with additional datasets such as the [Bhagavad Gita Instruction Dataset](https://huggingface.co/datasets/Pranay17/bhagvad_gita).

## Prerequisites

Before starting, ensure you have the following installed:
- Python 3.7+
- GPU-enabled environment (Google Colab or local machine with CUDA)
- Required Python libraries: `transformers`, `peft`, `trl`, and `bitsandbytes`

You can install the required packages using the following command:

```bash
!pip install -q accelerate==0.21.0 peft==0.4.0 bitsandbytes==0.40.2 transformers==4.31.0 trl==0.4.7

### Key Points in the README:

1. **Project Overview** explains the aim and gives an overview of the fine-tuning process.
2. **Prerequisites** lists out all the necessary dependencies and hardware requirements.
3. **Dataset Preparation** describes how to load and format datasets according to LLaMA-2's requirements.
4. **Fine-Tuning with QLoRA** walks through the model and tokenizer setup, the configuration of LoRA, and the training procedure.
5. **Results and Evaluation** explains how to track and interpret training results using TensorBoard.
6. **How to Use the Fine-Tuned Model** shows an example of how to generate text with the trained model.
7. **Acknowledgements** credits the tools, datasets, and techniques used in the project.

This README provides a clear and structured guide to understanding and replicating the entire fine-tuning process.
