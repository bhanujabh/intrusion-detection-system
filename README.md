# Intrusion Detection System using Hybrid Deep Learning Models

## Overview
This project implements a **network intrusion detection system** using the **CIC-IDS-2017 dataset**.  
It combines **CNN, GRU, and Transformer models** to detect malicious network activity and employs **Focal Loss** to handle class imbalance.  
The project includes **ablation studies**, evaluates multiple architectures, and reports metrics such as accuracy, precision, recall, F1-score, confusion matrix, and ROC curves.

## Dataset
- **Source:** [CIC-IDS-2017 on Kaggle](https://www.kaggle.com/datasets)  
- Contains network traffic data with labeled normal and attack traffic.  
- **Number of samples:** ~225,000  
- **Features:** 78 after preprocessing and feature selection  

## Preprocessing
- Handled missing values and infinite values.  
- **Feature selection** performed using **Boruta** to retain most relevant features.  
- Standardized features using **StandardScaler**.  
- Encoded labels using **LabelEncoder**.  

## Models
- **CNNEncoder:** Tiny 1D CNN for extracting local feature patterns  
- **GRUEncoder:** GRU to capture sequential patterns in feature vectors  
- **TransformerEncoder:** Transformer to model global dependencies  
- **CombinedModel:** Hybrid model concatenating embeddings from different encoders  

## Training
- Loss: **Focal Loss** for class imbalance  
- Optimizer: **Adam** 
- Experiments: Ablation studies for combinations like `CNN`, `GRU`, `Transformer`, `CNN+GRU`, etc.  

## Evaluation
- Metrics reported:  
  - **Accuracy**  
  - **Precision**  
  - **Recall**  
  - **F1-score**  
  - **Confusion Matrix**  
  - **ROC Curve**  

