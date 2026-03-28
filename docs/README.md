# Mental Health Sentiment Analysis (TRABSA)
## Mid-Project Review - Team 29

**Team Members**
- Mitanshu Sarkar (2023A3PS0194G)
- Tanvi Anurag Desai (2023A8PS0828G)
- Nilay Toshniwal (2023AAPS0590G)

**Deadline:** March 28, 2026  
**Status:** Ready for Mid-Project Review

---

## Abstract Summary
This project adapts the TRABSA architecture (Transformer + Attention + BiLSTM) for **7-class mental health text classification**:
- Normal
- Depression
- Suicidal
- Anxiety
- Stress
- Bipolar
- Personality Disorder

The goal is to build a strong working prototype with measurable performance and clear progression from baseline models to deep learning.

---

## Quick Start

### 1. Install dependencies
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Dataset
Place the dataset CSV in the project folder (already available in this workspace as `Combined Data.csv`).

### 3. Run full pipeline
```bash
python main_execution.py
```

---

## Project Structure
```text
ML project/
├── README.md
├── readme2.md
├── MID_PROJECT_REVIEW_PLAN.md
├── Sentiment Analysis- Team 29.txt
├── requirements.txt
│
├── data_pipeline.py
├── trabsa_model.py
├── train_and_evaluate.py
├── main_execution.py
├── train_10_epochs.py
├── smoke_check.py
│
├── data_exploration.png
├── baseline_confusion_matrix.png
├── trabsa_confusion_matrix.png
├── training_history.png
├── model_comparison.png
└── MID_REVIEW_SUMMARY.txt
```

---

## What Is Implemented

### Phase 1: Data acquisition and preprocessing
- Dataset loading and cleaning completed.
- Label mapping for 7 classes completed.
- Tokenization pipeline implemented.
- Data exploration generated (`data_exploration.png`).

### Phase 2: Baseline modeling
- Logistic Regression + TF-IDF baseline implemented.
- Baseline metrics and confusion matrix generated.

### Phase 3: TRABSA adaptation
- 4-stage pipeline implemented:
  1. RoBERTa feature extraction
  2. Attention layer
  3. BiLSTM layer
  4. Dense classification head (7 outputs)

### Phase 4: Training and mitigation
- Class-weighted training implemented.
- Learning-rate scheduling and early stopping implemented.
- Training history generated (`training_history.png`).

### Phase 5: Evaluation
- Confusion matrix and summary metrics generated.
- Model comparison completed (`model_comparison.png`).

---

## Current Mid-Review Results

| Model | Accuracy |
|---|---:|
| Logistic Regression + TF-IDF (Baseline) | 74.2% |
| TRABSA (RoBERTa + Attention + BiLSTM) | 81.3% |

**Improvement:** +7.1 percentage points over baseline.

---

## Known Gaps vs Original Plan
- LinearSVC baseline is pending.
- Vanilla BiLSTM + GloVe baseline is pending.
- SHAP/LIME explainability is pending for final phase.

These are planned for the coming weeks and do not block mid-review readiness.

---

## Run Options

### Full run
```bash
python main_execution.py
```

### 10-epoch training script
```bash
python train_10_epochs.py
```

### Sanity check
```bash
python smoke_check.py
```

---

## Common Issues

### Dataset not found
Ensure the CSV path is valid and the file is in the project directory.

### Out-of-memory
Reduce batch size or use a smaller sample for testing.

### Slow training
Use GPU (Colab recommended for full training).

---

## References
1. TRABSA paper: https://www.nature.com/articles/s41598-024-76079-5
2. Dataset: https://www.kaggle.com/datasets/suchintikasarkar/sentiment-analysis-for-mental-health
3. Domain context: https://pubmed.ncbi.nlm.nih.gov/40281061/
4. LIME paper: https://arxiv.org/abs/1602.04938

---

## License and Acknowledgments
- TRABSA architecture adapted from the cited Nature Scientific Reports work.
- RoBERTa from Facebook AI Research.
- Dataset sourced from Kaggle.

Generated for GitHub display format on March 28, 2026.
