
# Qwen3 TinyStories Tokenizer & Model Training

## Overview

This project implements a **complete Qwen3-based language model training pipeline** using the **TinyStories dataset**.
It covers **tokenization, model architecture, training, and text generation**, optimized for efficiency and memory usage.

---

## Features

* **Qwen3 Tokenizer** – Latest tokenizer with fallback support to Qwen2.5
* **Custom Qwen3 Architecture** – Grouped Query Attention (GQA), SwiGLU, RMSNorm, Rotary Positional Encodings (RoPE)
* **Optimized Training** – Mixed precision, gradient accumulation, cosine learning rate decay
* **Memory Efficient** – Optimized batch loading and processing for large context lengths
* **Model Generation** – Built-in text generation for evaluation

---

## Model Configuration

* **Parameters:** ~283M (optimized for efficiency)
* **Architecture:** Qwen3 with GQA, SwiGLU, RoPE
* **Context Length:** 32,768 tokens
* **Training:** 150k iterations with cosine decay learning rate

---

## Usage

1. Clone the repository and open the notebook.
2. Run all cells to train the model.
3. The trained model will be saved as `qwen3_slm.pt`.
4. Use the **generation section** to test text outputs.
5. Training progress and **loss plots** are automatically generated.

```bash
# Example (optional)
python train_qwen3.py
```

---

## Performance

* **Training Time:** ~5–6 hours on an A4 GPU
* **Memory Usage:** ~8GB VRAM
* **Final Loss:** Typically 2.5–3.0 on TinyStories
* **Model Size:** ~283M parameters

---

## Results

The model can generate **coherent and creative children's stories** based on the TinyStories dataset.

---

## Requirements

* Python 3.10+
* PyTorch 2.x
* Hugging Face Transformers
* nbformat, tqdm
* GPU with ~8GB VRAM recommended

---

## References

* [TinyStories Dataset](https://huggingface.co/datasets/Skylion007/openwebtext)
* [Qwen3 Architecture](https://github.com/QwenLM/Qwen-Model)

---

## License

This project is intended for **educational purposes**. Please cite original datasets and architectures if reused.

