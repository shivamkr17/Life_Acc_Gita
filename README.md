## Project Overview

The objective of this project is to fine-tune the LLaMA-2-7b-chat model using a custom dataset formatted according to the LLaMA-2 prompt template. We utilize QLoRA to enable efficient fine-tuning in a memory-constrained environment, using 4-bit precision and LoRA (Low-Rank Adaptation) techniques.

This fine-tuning process is demonstrated using the [Bhagavad Gita Instruction Dataset](https://huggingface.co/datasets/Pranay17/bhagvad_gita).



## Training Configuration
The key configurations for fine-tuning are as follows:

- QLoRA Parameters
```
lora_r = 64  # LoRA attention dimension
lora_alpha = 16  # Scaling parameter
lora_dropout = 0.1  # Dropout probability
use_4bit = True  # Enable 4-bit precision
bnb_4bit_compute_dtype = "float16"
bnb_4bit_quant_type = "nf4"
use_nested_quant = False  # Nested quantization
```
## Future Improvements
- Train for more epochs or on larger datasets to further improve accuracy.
- Experiment with higher-rank LoRA or different optimizers.
- Explore 8-bit or mixed-precision training on higher-end GPUs.
4. **Fine-Tuning with QLoRA** walks through the model and tokenizer setup, the configuration of LoRA, and the training procedure.
5. **Results and Evaluation** explains how to track and interpret training results using TensorBoard.
6. **How to Use the Fine-Tuned Model** shows an example of how to generate text with the trained model.
7. **Acknowledgements** credits the tools, datasets, and techniques used in the project.

This README provides a clear and structured guide to understanding and replicating the entire fine-tuning process.
