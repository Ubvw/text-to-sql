# Text-to-SQL Fine-tuning with Unsloth and Llama-3.2-3B-Instruct

This project demonstrates how to fine-tune the **Llama-3.2-3B-Instruct** model using [Unsloth](https://github.com/unslothai/unsloth) for a text-to-SQL task.

## Project Overview
The goal is to train a model that can generate SQL queries from natural language prompts, given a company database context. The process leverages efficient fine-tuning techniques and open datasets.

## Steps

1. **Setup**
	- Install necessary libraries

2. **Model Loading**
	- Load the Llama-3.2-3B-Instruct model using `FastLanguageModel` from Unsloth.
	- The model is loaded in 4-bit quantization for memory efficiency.

3. **LoRA Configuration**
	- Apply LoRA (Low-Rank Adaptation) to the model for efficient fine-tuning.

4. **Dataset Preparation**
	- Load and format the [`gretelai/synthetic_text_to_sql`](https://huggingface.co/datasets/gretelai/synthetic_text_to_sql) dataset.
    - Largest sql text to sql dataset as of Sept. 18
	- Convert data into a prompt-response format suitable for training.

5. **Trainer Setup**
	- Configure and initialize the `SFTTrainer` from `trl` for supervised fine-tuning.

6. **Training**
	- Train the model on the prepared dataset (example: for a limited number of steps).

7. **Model Saving**
	- Save the fine-tuned model in GGUF format.

8. **Download**
	- Download the saved GGUF model file for inference.

9. **Run**
	- Create a Modelfile and run it with Ollama locally.

## Usage
The resulting fine-tuned model can be used to generate SQL queries from natural language prompts.

---
*For more details, see the notebook in this repository.*
