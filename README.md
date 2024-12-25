# Translation-and-Evaluation-using-BLOOMZ-and-mT5-Small

---

## Overview

This project implements and evaluates two powerful multilingual transformer models—**BLOOMZ** and **mT5-Small**—to handle translation tasks. It involves training, testing, and comparing these models' performances on multilingual datasets. The repository includes two Jupyter notebooks:

1. **`NLP_FinalProject.ipynb`** - The main notebook for loading data, fine-tuning the models, and performing translation tasks.
2. **`NLP_FinalProject_Evaluation.ipynb`** - Dedicated to evaluating the models using various metrics and visualization techniques.

---

## Key Features

- **Pre-trained Models**:
  - **BLOOMZ**: A multilingual open fine-tuned language model.
  - **mT5-Small**: A lightweight multilingual variant of the T5 (Text-to-Text Transfer Transformer) model.

- **Translation Tasks**:
  - Focused on multilingual data (e.g., English and Haitian Creole).
  - Fine-tuned for specific translation tasks to improve performance.

- **Evaluation**:
  - Comparative performance analysis using metrics like BLEU and ROUGE.
  - Detailed visualization of results.

---

## Notebooks Overview

### 1. `NLP_FinalProject.ipynb`

#### Features:
- **Data Preparation**:
  - Loads and preprocesses multilingual datasets.
  - Handles tokenization and preparation for BLOOMZ and mT5-Small.
- **Fine-tuning**:
  - Customizes both models for the translation task.
  - Optimizes using hyperparameters specific to each model.
- **Translation**:
  - Performs translation using both BLOOMZ and mT5-Small.
  - Logs intermediate and final translations for comparison.

---

### 2. `NLP_FinalProject_Evaluation.ipynb`

#### Features:
- **Metric Calculation**:
  - Computes BLEU, ROUGE, and other standard metrics to evaluate translation quality.
  - Analyzes performance on the test set.
- **Visualization**:
  - Displays metric trends and comparisons in graphs.
- **Comparative Analysis**:
  - Summarizes the strengths and weaknesses of BLOOMZ and mT5-Small.

---

## Requirements

### Software
- Python 3.9+
- Jupyter Notebook
- PyTorch
- Transformers (Hugging Face)
- Datasets (Hugging Face)
- BLEU and ROUGE metric libraries

### Hardware
- **GPU Recommended** for training and fine-tuning the transformer models.

---

## Hyperparameters

- Learning Rate: 1e-4
- Batch Size: 16
- Epochs: 3
- Maximum Sequence Length: 128

---

## Results

- **BLOOMZ**:
  - High-quality translations with a focus on low-resource languages.
  - Demonstrated robust generalization.

- **mT5-Small**:
  - Lightweight model with faster inference times.
  - Performs well but slightly less accurate than BLOOMZ for complex translations.

Key Metrics:
- BLEU and ROUGE scores for both models.
- Visual comparison of performance.

---

## Usage

1. **Clone Repository**:
   ```bash
   git clone https://github.com/username/NLP-Final-Project.git
   cd NLP-Final-Project
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Training**:
   - Open `NLP_FinalProject.ipynb` in Jupyter Notebook.
   - Execute cells to fine-tune the models.
4. **Evaluate Models**:
   - Open `NLP_FinalProject_Evaluation.ipynb`.
   - Run the evaluation pipeline for performance metrics.

---

## Future Work

- Incorporate more languages to test scalability.
- Experiment with larger variants of BLOOMZ and mT5.
- Add domain-specific fine-tuning for specialized translation tasks.

---

