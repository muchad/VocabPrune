# VocabPrune

[![Status](https://img.shields.io/badge/Status-Under_Review-yellow.svg)](https://github.com/muchad/VocabPrune)
[![HuggingFace](https://img.shields.io/badge/Models-HuggingFace-orange.svg)](https://huggingface.co/collections/muchad/pruned-mdeberta)


> **⚠️ Note:** This research is currently **under review for publication**. The full paper citation will be updated here upon acceptance.

## 🚀 Released Models

We provide three optimized checkpoints ready for deployment:

* **[mDeBERTa-Hybrid-30k](https://huggingface.co/muchad/mdeberta-hybrid-30k)** (Recommended): Balanced hybrid vocabulary (70% ID / 30% EN) for best stability.
* **[mDeBERTa-ID-30k](https://huggingface.co/muchad/mdeberta-id-30k)**: Monolingual Indonesian vocabulary.
* **[mDeBERTa-ID-20k](https://huggingface.co/muchad/mdeberta-id-20k)**: Aggressive pruning for maximum memory efficiency.

🔗 **Full Collection:** [Hugging Face Collection: Pruned mDeBERTa](https://huggingface.co/collections/muchad/pruned-mdeberta)

## 💻 Usage

To reproduce the pruning process, run the provided notebook:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muchad/VocabPrune/blob/main/VocabPrune.ipynb)

The notebook includes steps for corpus downloading, frequency analysis, and tokenizer reconstruction.
