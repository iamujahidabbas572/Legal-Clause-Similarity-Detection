## Overview
This project compares two baseline NLP architectures — **BiLSTM** and **Attention-based Encoder** — using FastText embeddings to predict semantic similarity between legal clauses.

## Architectures
- **Baseline 1:** BiLSTM (bidirectional)
- **Baseline 2:** Attention-based Encoder
- Embedding: FastText (300d)
- Framework: PyTorch

## Dataset
Legal clause similarity dataset (train/val/test split: 80/10/10).  
Dataset stored in Google Drive and loaded into Colab via path `/content/drive/MyDrive/...`.

##  Training
Trained using NVIDIA T4 GPU on Google Colab.  
Batch size = 64, Learning rate = 1e-3, Optimizer = Adam, Epochs = 5.

## Results
| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|:------|:----------|:-----------|:--------|:----------|:---------|
| BiLSTM | 0.9998 | 0.9996 | 1.0000 | 0.9998 | 1.0000 |
| Attention Encoder | 0.9999 | 0.9999 | 1.0000 | 0.9999 | 1.0000 |

##  Example Predictions
-  **Similar:** “The borrower shall repay the loan…” ↔ “The debtor is obligated to return borrowed funds…”
-  **Incorrectly Similar:** “The lender may terminate…” ↔ “The borrower may terminate…” (role confusion)

##  How to Run
1. Open `DL_A2_22I1969.ipynb` in Colab.
2. Mount Google Drive and set dataset path.
3. Run all cells to train and evaluate both models.

---

© 2025 Mujahid Abbas, FAST University – NLP Assignment
