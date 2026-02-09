# BSAN6070_Machine_Learning_CA02# CA02: Email Spam Classification using Naive Bayes

## Overview

Email spam classifier using **Gaussian Naive Bayes** algorithm. Trained on 702 emails, tested on 260 emails, achieving **~96.5% accuracy**.

---

## Dataset

- **Training**: 702 emails (351 spam, 351 non-spam)
- **Testing**: 260 emails
- **Files**: `.txt` format
  - Spam: `spmsga1.txt`, `spmsga162.txt`, etc.
  - Non-spam: `3-1msg1.txt`, `7-2msg3.txt`, etc.

---

## Setup

### Required Libraries
```bash
pip install numpy scikit-learn jupyter
```

### Directory Structure
```
CA02/
├── CA02_NB_assignment.ipynb
├── train-mails/  (702 files)
└── test-mails/   (260 files)
```

---

## How to Run

### Local Jupyter
```bash
# 1. Extract Data.zip to get train-mails and test-mails folders
# 2. Place folders in same directory as notebook
jupyter notebook CA02_NB_assignment.ipynb
# 3. Run all cells
```

### Google Colab
1. Upload notebook and data folders to Google Drive
2. Open notebook in Colab
3. Mount Drive and navigate to your folder
4. Run all cells

---

## Algorithm

**Naive Bayes** classifier using:
- **Dictionary**: 3000 most frequent words from training data
- **Features**: Word frequency matrix (emails × words)
- **Classification**: Probabilistic model based on Bayes' Theorem

---

## Expected Results
```
Accuracy: 0.9653846153846154 (~96.5%)
Correctly classified: 251/260 emails
Misclassified: 9 emails
```

---

## Key Functions

- `make_Dictionary(root_dir)`: Extracts 3000 most common words
- `extract_features(mail_dir)`: Converts emails to numerical feature matrix
- Model training: `GaussianNB().fit(features, labels)`
- Prediction: `model.predict(test_features)`

---

## Author

**Course**: Machine Learning / Data Mining  
**Assignment**: CA02 - Naive Bayes Spam Classification  
**Date**: February 2026

---

## Important Notes

- Use relative paths: `./train-mails` and `./test-mails`
- Do NOT modify original data files
- Results may vary slightly (96-97%) depending on file order
