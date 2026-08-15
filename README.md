# VocabPrune

[![Paper](https://img.shields.io/badge/IEEE%20Access-Published-blue.svg)](https://doi.org/10.1109/ACCESS.2026.3679735)
[![DOI](https://img.shields.io/badge/DOI-10.1109%2FACCESS.2026.3679735-blue.svg)](https://doi.org/10.1109/ACCESS.2026.3679735)
[![Models](https://img.shields.io/badge/Models-HuggingFace-orange.svg)](https://huggingface.co/collections/muchad/pruned-mdeberta)
[![License](https://img.shields.io/badge/License-Apache--2.0-green.svg)](LICENSE)

Official implementation and model checkpoints for the paper **"Efficient Transformer Models via Language-Aware Frequency-Based Vocabulary Pruning"**, published in **IEEE Access**.

## 📌 Overview

Multilingual Transformer architectures, such as `mDeBERTa-v3-base`, incur substantial embedding-parameter overhead due to their large multilingual vocabularies, where many embedding parameters are redundant for specific language-dependent downstream tasks.

**VocabPrune** introduces a deterministic, language-aware, frequency-based vocabulary pruning strategy that substantially reduces model storage and memory footprint without architectural modifications or additional large-scale pre-training.

### 🌟 Key Results

* **~29% Peak GPU Memory Reduction:** Reduces peak GPU inference memory from 6.64 GB to 4.70 GB with a 30k-token vocabulary.
* **Minimal Performance Degradation:** Average F1-score degradation is less than 1.5% across Named Entity Recognition (NER) and Sentiment Analysis (SA) tasks.
* **Low Subword Fertility (~1.008):** The hybrid vocabulary configuration maintains low word fragmentation while preserving substantial cross-lingual subword overlap.

## 🚀 Released Checkpoints

Pre-pruned and fine-tune ready model weights are available on Hugging Face:

| Model | Vocab Size | Description / Target Setup | Hugging Face Link |
| :--- | :---: | :--- | :--- |
| **mDeBERTa-Hybrid-30k** | 30k | **Recommended:** Hybrid vocabulary (70% ID / 30% EN) for balanced Indonesian–English coverage | [🤗 Model Card](https://huggingface.co/muchad/mdeberta-hybrid-30k) |
| **mDeBERTa-ID-30k** | 30k | Monolingual Indonesian vocabulary | [🤗 Model Card](https://huggingface.co/muchad/mdeberta-id-30k) |
| **mDeBERTa-ID-20k** | 20k | Aggressive pruning for resource-constrained deployment | [🤗 Model Card](https://huggingface.co/muchad/mdeberta-id-20k) |

🔗 **Browse all models:** [Hugging Face Collection: Pruned mDeBERTa](https://huggingface.co/collections/muchad/pruned-mdeberta)

## 💻 Reproduce the Pruning Process

To reproduce the pruning process, run the provided notebook:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/muchad/VocabPrune/blob/main/VocabPrune.ipynb)

The notebook includes steps for corpus downloading, frequency analysis, and tokenizer reconstruction.

## 📚 Citation

If you use the **VocabPrune methodology**, the pruning code, or any of the released vocabulary-pruned models in your research, please cite:

### IEEE Style

```text
M. Fuadi, A. D. Wibawa, and S. Sumpeno,
"Efficient Transformer Models via Language-Aware Frequency-Based
Vocabulary Pruning," IEEE Access, vol. 14, pp. 50993–51006, 2026,
doi: 10.1109/ACCESS.2026.3679735.
```

### BibTeX

```bibtex
@article{fuadi2026efficient,
  author  = {Fuadi, Mukhlish and Wibawa, Adhi Dharma and Sumpeno, Surya},
  title   = {Efficient Transformer Models via Language-Aware
             Frequency-Based Vocabulary Pruning},
  journal = {IEEE Access},
  volume  = {14},
  pages   = {50993--51006},
  year    = {2026},
  doi     = {10.1109/ACCESS.2026.3679735}
}
```
