# Diabetic Retinopathy Diagnosis Using Deep Neural Networks

## Overview
This repository contains materials for the research paper:
**"Diabetic Retinopathy Diagnosis Using Deep Neural Networks"**  
DOI: https://doi.org/10.15276/aait.09.2026.01

The project presents a reliability-aware deep learning framework for automated classification of diabetic retinopathy (DR) stages using fundus images, with a focus on **predictive uncertainty and model reliability.

---

## Authors
- **Yelizaveta I. Kabanova**  
  ORCID: https://orcid.org/0009-0001-2692-5066  
  Email: yelizavetakabanova@gmail.com  

- **Nataliia V. Kuznietsova**  
  ORCID: https://orcid.org/0000-0002-1662-1974  
  Scopus Author ID: 56412465200  

- **Kateryna O. Ivanko**  
  ORCID: http://orcid.org/0000-0002-3842-2423  
  Scopus Author ID: 55819298100  

- **Vishwesh Kulkarni**  
  ORCID: https://orcid.org/0000-0002-22858652  
  Scopus Author ID: 7201425741  

---

## Citation
If you use this work, please cite:

> Kabanova Y. I., Kuznietsova V. N., Ivanko K., Kulkarni V.  
> “Diabetic Retinopathy Diagnosis Using Deep Neural Networks”.  
> Applied Aspects of Information Technology, 2026; Vol.9 No.1.
> DOI: https://doi.org/10.15276/aait.09.2026.01  

---

## Abstract
This work addresses the problem of automated diabetic retinopathy diagnosis using deep learning, with a particular focus on prediction reliability and uncertainty estimation.  

A unified framework is proposed that integrates:
- convolutional neural networks with transfer learning;
- adaptive attention mechanisms;  
- preprocessing and class balancing strategies;  
- uncertainty estimation via stochastic inference;  

A systematic experimental study demonstrates that combining advanced preprocessing, oversampling, adaptive attention, and uncertainty estimation significantly improves both classification performance and predictive reliability.

---

## Motivation
Diabetic retinopathy is one of the leading causes of blindness worldwide. Reliable automated diagnosis is critical, as incorrect but highly confident predictions may lead to severe clinical consequences. The aim of this study is to develop and experimentally validate an integrated and uncertainty-aware methodology for diabetic retinopathy (DR) stage classification from fundus images. 

---

## Scientific contributions 
- A comprehensive experimental framework for analyzing preprocessing and class balancing under fixed architecture.
- Systematic comparison of four configurations using DenseNet121.
- Proposed Adaptive CBAM attention mechanism based on feature variability. 
- Integration of Monte Carlo Dropout for uncertainty estimation. 
- Introduction of a novel Reliability Score (RS) metric.

--- 

## Objectives
2. Investigate the characteristics of fundus images and available datasets.
3. Develop an approach to image preprocessing to improve data quality.
4. Conduct an experimental study to evaluate the impact of different data preparation strategies on classification results.
5. Develop a deep learning model for automatic classification of DR stages based on convolutional neural networks.
6. Propose an integrated metric for the comprehensive assessment of classification quality and predictive reliability.
7. Analyse the experimental results, compare the proposed model with existing methods, and assess the practical applicability of the approach for automated medical diagnostics.

---

## Methodology

![Methodology](<img width="1143" height="522" alt="methodology" src="https://github.com/user-attachments/assets/27c973ab-9b56-46bc-9f5b-1d2a739b8e8d" />)

---

### Data
- Dataset: APTOS 2019 Blindness Detection (Kaggle).
- 5 classes (DR stages: 0–4).

---

### Experiments
Four configurations:

| Experiment | Preprocessing | Balancing |
|----------|-------------|----------|
| A0 | Basic | Class weights |
| A1 | Basic | Oversampling |
| B0 | Advanced | Class weights |
| B1 | Advanced | Oversampling |

---

## Reliability Score

A novel metric combining:
- classification quality (QWK);
- prediction confidence;
- predictive uncertainty.

---

## Key Results

- Best model: **B1 configuration**  
  (Focal Loss + Adaptive CBAM + Monte Carlo Dropout)  
- Metrics:
  - QWK: **0.92**  
  - Accuracy: **0.85**  
  - F1-score: **0.85**  
  - AUC: **0.97**
- Key improvements:
  - better minority class detection  
  - higher prediction stability  
  - reduced uncertainty  

![Confusion Matrix](![conf_matrix_B1_full](https://github.com/user-attachments/assets/014292f6-e342-4f87-a5eb-3117b57db3b4))

---

## Additional Results

In addition to figures presented in the paper, this repository includes extended experimental outputs for each configuration:

- Confusion matrixes. 
- ROC-AUC curves.
- Saliency maps.
- Distributions of:
  - epistemic uncertainty;
  - predictive entropy;
  - confidence–entropy ratio; 
- Examples of correct and incorrect predictions.

### Aggregated metrics:
- Mean performance metrics across experiments.  
- Reliability Score comparison.

### Files:
- `training_results.csv` — classification metrics.
- `uncertainty_results.csv` — uncertainty-related metrics. 

---

## Limitations

- Only APTOS 2019 dataset used.
- Oversampling applied before split.  
- No external validation (e.g., EyePACS, Messidor).

---

## Future Work

- Evaluate on additional datasets. 
- Explore alternative uncertainty estimation methods. 
- Improve generalization and robustness.

---

## License

This project is shared for research and educational purposes.
