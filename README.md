# Dark Pattern Detection using DistilBERT

## Overview

This project implements a dark pattern detection system using the DistilBERT model. The system can evaluate the trustworthiness of text paragraphs and identify potential dark patterns in web content.

## Contents


1. [Installation](#installation)
2. [Dark Pattern Detection](#dark-pattern-detection)
   - [Naive Bayes Approach](#naive-bayes-approach)
     - [Data Preparation](#1-data-preparation)
     - [Train Naive Bayes Model](#2-train-naive-bayes-model)
     - [Evaluate and Test Naive Bayes Model](#3-evaluate-and-test-naive-bayes-model)
   - [DistilBERT Approach](#2-distilbert-approach)
     - [Data Preparation](#1-data-preparation-1)
     - [Train DistilBERT Model](#2-train-distilbert-model)
     - [Evaluate and Test DistilBERT Model](#3-evaluate-and-test-distilbert-model)
   - [Model Comparison](#model-comparison)
3. [Web Scraping Results](#Web-Scraping-Results)
4. [Dependencies](#dependencies)
5. [Authors](#authors)
6. [License](#license)

## Installation

1. Install required packages(Collab):

   ```bash
   !pip install requests beautifulsoup4 torch transformers
   
## Dark Pattern Detection

This repository contains code for two different approaches to detect dark patterns - one using a Naive Bayes classifier and the other using DistilBERT, a pre-trained transformer model.

## Naive Bayes Approach

### 1. Data Preparation

Assuming you have a labeled dataset in TSV format `dataset.tsv`, where the 'text' column contains the textual data and `label` contains binary labels `0 or 1`.

### 2. Train Naive Bayes Model Results :

```python
Accuracy:  0.9449152542372882

```
### 3. Evaluate and Testing the Naive Bayes Model :
```
Text: limited stock available, buy now!
Prediction: Dark Pattern
Trust Score: 0.02%

Text: free trial for 30 days, cancel anytime.
Prediction: Dark Pattern
Trust Score: 0.04%

Text: write a review and get a discount!
Prediction: Not Dark Pattern
Trust Score: 95.99%

Text: click here to win a prize!
Prediction: Not Dark Pattern
Trust Score: 97.90%
```
DistilBERT Approach
## 2. DistilBERT Approach
### 1. Data Preparation
Assuming you have a labeled dataset in TSV format `dataset.tsv`, where the 'text' column contains the textual data and `label` contains binary labels` 0 or 1`.

### 2. Train DistilBERT Model Results 
```
Epoch 1/10
Validation Accuracy: 0.9703
Model saved with the best accuracy.
Epoch 2/10
Validation Accuracy: 0.9597
Epoch 3/10
Validation Accuracy: 0.9619
Epoch 4/10
Validation Accuracy: 0.9703
Early stopping. No improvement in validation accuracy.

```
### 3. Evaluate and Testing the DistilBERT Model :
```
Text: Limited stock available, buy now!
Prediction: Dark Pattern
Trust Score: 15.00%

Text: Free trial for 30 days, cancel anytime.
Prediction: Dark Pattern
Trust Score: 15.00%

Text: Write a review and get a discount!
Prediction: Not Dark Pattern
Trust Score: 99.71%

Text: Click here to win a prize!
Prediction: Not Dark Pattern
Trust Score: 98.12%

Text: Exclusive offer! Subscribe now and save 20% on your first purchase. Limited time only!
Prediction: Dark Pattern
Trust Score: 15.00%

Text: Hi my name is soarbh
Prediction: Not Dark Pattern
Trust Score: 98.66%
```
...

## Model Comparison
```
| Model          | Accuracy |
| -------------- | -------- |
| Naive Bayes    | 0.9449   |
| DistilBERT     | 0.9703   |

Model used : DistilBERT 
Highest accuracy : 0.9703
```
## Web Scraping Results

The web scraping results provide insights into the trustworthiness of the content obtained from a specific webpage. The analysis includes an overall average trust score and the percentage of identified dark patterns.

```plaintext
Overall Average Trust Score: 0.49%
Percentage of Dark Patterns: 100.00%
Percentage of Overall Average Trust Score: 48.50%
```
## Dependencies
```
Python 3.x
pandas
scikit-learn
joblib
torch
transformers
requests
beautifulsoup4
```
## Authors
[Soarbh Srivastava]()
[Varun]()
[Nidhi]()

## License

This project is licensed under the [MIT License](LICENSE).

