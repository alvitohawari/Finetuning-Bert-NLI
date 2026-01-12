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
