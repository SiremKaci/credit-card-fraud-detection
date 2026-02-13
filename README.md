# Détection de Fraude sur Cartes de Crédit

[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Dataset: Kaggle](https://img.shields.io/badge/Dataset-Kaggle-orange)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

## Description

Projet end-to-end pour détecter les fraudes sur cartes de crédit avec un dataset très déséquilibré (seulement 0.17% de fraudes). J'ai implémenté un pipeline complet : preprocessing, rééquilibrage (SMOTE, SMOTETomek), modélisation avec Logistic Regression, XGBoost et Autoencodeur (TensorFlow), et interprétabilité via SHAP.

Ce projet met l'accent sur les métriques adaptées aux classes déséquilibrées (PR-AUC, Recall pour fraudes) et montre comment réduire les faux négatifs pour minimiser les pertes financières.

## Résultats clés

- **Meilleur modèle** : XGBoost avec SMOTETomek – PR-AUC : 0.8673, ROC-AUC : 0.9816, Recall fraudes : 0.8673
- Réduction significative des faux négatifs comparé à un modèle basique.
- Interprétabilité : SHAP values montrent que V14 et V17 sont les features les plus impactantes.

![PR Curve](Email_Silk.svg.png)  
*Courbe Precision-Recall du modèle XGBoost (AP score élevé)*

## Technologies

- **Langage** : Python 3.10+
- **Librairies** : Pandas, NumPy, Scikit-learn, imbalanced-learn (SMOTE), XGBoost, TensorFlow/Keras, SHAP, Matplotlib/Seaborn
- **Dataset** : [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) – 284k transactions anonymisées

## Installation

1. Clone le repo :
   ```bash
   git clone https://github.com/SiremKaci/credit-card-fraud-detection.git
   cd credit-card-fraud-detection
