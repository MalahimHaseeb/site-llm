# site-llm

Fine-tuned Qwen3-4B using QLoRA on Google Colab's free T4 GPU, trained on
my own portfolio content (services, project descriptions, FAQ answers).

## Stack
- Base model: unsloth/Qwen3-4B-bnb-4bit
- Method: LoRA (r=16) via Unsloth, 4-bit quantized base
- Data: 59 instruction/output pairs, multiple phrasings per fact
- Training: 15 epochs, 120 steps, final loss 0.066

## What it does well
Answers paraphrased questions about my projects and services correctly,
generalizes beyond exact training phrasings for in-scope topics.

## Files
- `training_notebook.ipynb` — full training run with output logs and debugging steps
