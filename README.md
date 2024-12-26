# Fine-Tuned Text Generation Models for a Low-Resource Language

This repository contains my work on fine-tuning two powerful language models (BloomZ and mT5-small) for text generation in Haitian Creole, a low-resource language. The models are specifically adapted to understand prompts and generate contextually appropriate responses in Haitian Creole. Both models were trained using an Alpaca-style instruction dataset to enhance their generation abilities. Both models were trained using an Alpaca-style instruction dataset to enhance their ability to understand and generate Haitian Creole text.

## Models Overview

### 1. Fine-Tuned BloomZ Model
**Model Repository:** [`sprab4/bloomz_fine_tuned_model`](https://huggingface.co/sprab4/bloomz_fine_tuned_model)

The BloomZ model, originally designed for multilingual tasks, has been fine-tuned to generate fluent and contextually accurate text specifically in Haitian Creole. The base model's multilingual capabilities make it particularly suitable for this task.

### 2. Fine-Tuned mT5-Small Model
**Model Repository:** [`sprab4/mt5_fine_tuned_model`](https://huggingface.co/sprab4/mt5_fine_tuned_model)

The mT5-Small model, which supports over 100 languages including Haitian Creole, has been fine-tuned for text generation tasks. Its architecture is particularly well-suited for text-to-text generation tasks in Haitian Creole.

## Training Details

Both models were trained using similar approaches but with different hyperparameters optimized for their respective architectures.

### BloomZ Training Configuration
- **Base Model:** `bigscience/bloomz`
- **Training Process:**
  - 2 epochs using Hugging Face Trainer
  - Validation-based performance monitoring
  - Alpaca-style instruction-response format
- **Hyperparameters:**
  - Learning rate: 5e-5
  - Per device train batch size: 2
  - Gradient accumulation steps: 8
  - FP16: False
  - Weight decay: 0.1
  - Warmup steps: 500

### mT5-Small Training Configuration
- **Base Model:** `google/mt5-small`
- **Training Process:**
  - 2 epochs using Hugging Face Trainer
  - Validation-based performance monitoring
  - Alpaca-style instruction-response format
- **Hyperparameters:**
  - Learning rate: 1e-4
  - Per device train batch size: 4
  - Gradient accumulation steps: 4
  - FP16: False
  - Weight decay: 0.05
  - Warmup steps: 100

## Performance Evaluation

Both models were evaluated using BERTScore on various prompts. Here's a comparison using a sample prompt:

**Sample Prompt:**
```
Solèy la ap kouche ak yon bèl solèy kouche vizib nan orizon an, dekri li nan de fraz
```
(English: The sun is setting and a beautiful sunset is visible on the horizon, describe it in two sentences)

### BloomZ Performance
- BERTScore Precision: 0.7526
- BERTScore Recall: 0.7445
- BERTScore F1: 0.7485

### mT5-Small Performance
- BERTScore Precision: 0.6636
- BERTScore Recall: 0.6542
- BERTScore F1: 0.6589

## Example Outputs

### BloomZ Output
**Prediction:** Solèy la ap kouche ak yon bèl solèy kouche vizib nan orizon an, dekri li nan de fraz Kouchè la se koupyè nan ouviyon an. Li se fè kouyèl nan fòmèl an a. Lè se vèk la a, ak li se pèmèt pou fòm la. Kouche la te kòt pou kòm la, li te pòmè pou vòk li. La te fèt li, ki te lès pou lè li anpè.

### mT5-Small Output
**Prediction:** ak yon lòd efè yo fè

## Repository Structure
- `training.ipynb`: Jupyter notebook containing the training code and process
- `evaluation.ipynb`: Jupyter notebook containing evaluation metrics and testing
- Model files are hosted on Hugging Face:
  - BloomZ: [sprab4/bloomz_fine_tuned_model](https://huggingface.co/sprab4/bloomz_fine_tuned_model)
  - mT5: [sprab4/mt5_fine_tuned_model](https://huggingface.co/sprab4/mt5_fine_tuned_model)

