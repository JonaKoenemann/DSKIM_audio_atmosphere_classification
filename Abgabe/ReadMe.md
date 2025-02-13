# Audio Classification with AST Model

This repository contains scripts for training and evaluating an Audio Spectrogram Transformer (AST) model on an audio classification task. The project focuses on handling class imbalance through label merging, data augmentation, and class-weighted loss functions.

## Project Overview

- **Objective**: Classify audio clips into emotion-based categories (e.g., "Celebration", "Disappointment").
- **Challenges**: 
  - Class imbalance in the dataset.
  - Difficulty distinguishing between similar labels (e.g., "Excitement" vs. "Celebration").
- **Solutions**:
  - Merging similar labels to reduce complexity.
  - Data augmentation for underrepresented classes.
  - Class-weighted loss to address imbalance.

---

## Files Description

### 1. `AST_class_weights_reduce_DataLabels.py`
- **Purpose**: Explore label merging and data augmentation to improve metrics.
- **Key Features**:
  - Merges labels like "Celebration" & "Excitement" to reduce model complexity.
  - Augments "Disappointment" with noise, pitch shifting, and time stretching.
  - Evaluates accuracy and confusion matrices after each modification.

### 2. `AST_class_weights.py`
- **Purpose**: Baseline training script for the AST model with class-weighted loss.
- **Key Features**:
  - Uses `MIT/ast-finetuned-audioset` pre-trained model.
  - Applies class weights to handle imbalanced data.
  - Includes training logs, loss curves, and evaluation metrics.

### 3. `data_exploration.py`
- **Purpose**: Exploratory data analysis (EDA) for audio dataset.
- **Key Features**:
  - Visualizes waveforms, spectrograms, and frequency spectra.
  - Analyzes label distribution.
  - Plays audio samples for each class.

### 4. `Labels_data_aug.py`
- **Purpose**: Augment specific labels ("Excitement" and "Disappointment") to improve differentiation.
- **Key Features**:
  - Applies noise, pitch shifting, and time stretching.
  - Trains model on augmented data and evaluates confusion matrices.

### 5. `AST_class_weights_reduce_DataLabels.py`
- **Purpose**: Merging Labels together to improve differentiation.
- **Key Features**:
  - Merging "Excitement" and "Celebration"
  - Merging "Disappointment" and "Boring"