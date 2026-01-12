# Fine-tuning BERT for Natural Language Inference (NLI)

## 👥 Team Information
**Course**: Deep Learning  
**Institution**: Telkom University  

| Name | NIM |
|------|-----|
| Alvito Kiflan Hawari | 1103220235 |
| Nafal Rifky Atsilah Maulana | 1103223106 |

---

## 🎯 Purpose
This repository contains the implementation of a **Natural Language Inference (NLI)** project using **BERT**.

The objective of this project is to fine-tune a pre-trained **BERT** model to determine the logical relationship between two sentences: whether a hypothesis is **entailed**, **contradicted**, or **neutral** with respect to a given premise.

---

## 🔍 Project Overview

### The Task: Natural Language Inference
Natural Language Inference (NLI), also known as **Recognizing Textual Entailment (RTE)**, is a core task in Natural Language Processing (NLP).

Given:
- **Premise**: A statement assumed to be true
- **Hypothesis**: A statement to be evaluated

The model predicts one of the following relationships:
- **Entailment** – the hypothesis is true given the premise
- **Contradiction** – the hypothesis is false given the premise
- **Neutral** – the relationship is unclear

---

## 📚 Dataset

The model is trained on an **NLI dataset** (such as SNLI or MNLI format), consisting of sentence pairs annotated with inference labels.

- **Input**:  
- **Output Labels**:
- Entailment
- Contradiction
- Neutral
- **Task Type**: Multi-class sentence-pair classification

---

## 🤖 Model Description

### The Model: BERT-base
- **Base Model**: `bert-base-uncased`
- **Architecture**: Encoder-only Transformer
- **Pre-training Objectives**:
- Masked Language Modeling (MLM)
- Next Sentence Prediction (NSP)

### Fine-tuning Strategy
- A classification head is added on top of the `[CLS]` token
- The full BERT model is fine-tuned end-to-end
- Cross-entropy loss is used for optimization

---

## 📊 Technical Approach

### Model Configuration
- **Base Model**: `bert-base-uncased`
- **Tokenizer**: `BertTokenizerFast`
- **Framework**: PyTorch & Hugging Face Transformers
- **Task Type**: Sentence-pair classification

### Training Configuration
- **Batch Size**: 16
- **Learning Rate**: 2e-5
- **Epochs**: 3
- **Optimizer**: AdamW
- **Loss Function**: Cross-Entropy Loss
- **Evaluation Metrics**:
- Accuracy
- Precision
- Recall
- F1-score

---

## 📁 Repository Structure
finetuning-bert-nli/
│
├── notebooks/
│ └── Finetuning-Bert-NLI.ipynb # Main Jupyter Notebook for NLI training
│
├── models/
│ └── bert-nli.pt # Saved fine-tuned model
│
└── README.md # Project documentation
