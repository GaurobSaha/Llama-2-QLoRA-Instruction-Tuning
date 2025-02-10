Large Language Models (LLMs) like LLaMA-2 require massive computing power to fine-tune. QLoRA (Quantized LoRA) is a memory-efficient fine-tuning technique that enables instruction-tuning on low-memory GPUs while preserving the full precision of activations.
This repository provides a complete pipeline for fine-tuning LLaMA-2-7B using QLoRA with an instruction dataset. The fine-tuned model can be used for chatbots, task-specific assistants, and custom text generation applications.

- Fine-tunes LLaMA-2-7B for instruction-following tasks
- Uses QLoRA (bitsandbytes 4-bit quantization) for efficient training on low VRAM GPUs
- Supports gradient checkpointing to reduce memory consumption
- Implements cosine learning rate scheduling for stable training
- Saves and uploads the fine-tuned model to Hugging Face Hub
- Optimized for single-GPU training (A100)

## Technologies Used:
- Python
- Hugging Face Transformers
- QLoRA (Quantized LoRA)
- BitsAndBytes (bnb)
- Torch (PyTorch)
- Datasets (Hugging Face Dataset Library)
- PEFT (Parameter-Efficient Fine-Tuning