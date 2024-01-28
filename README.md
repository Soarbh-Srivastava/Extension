# Dark Pattern Detection using DistilBERT

## Overview

This project implements a dark pattern detection system using the DistilBERT model. The system can evaluate the trustworthiness of text paragraphs and identify potential dark patterns in web content.

## Contents

- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Model Training](#model-training)
- [Web Scraping](#web-scraping)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Install required packages:

   ```bash
   pip install requests beautifulsoup4 torch transformers
   
## Dark Pattern Detection

This repository contains code for two different approaches to detect dark patterns - one using a Naive Bayes classifier and the other using DistilBERT, a pre-trained transformer model.

## Naive Bayes Approach

### 1. Data Preparation

Assuming you have a labeled dataset in TSV format (`dataset.tsv`), where the 'text' column contains the textual data and 'label' contains binary labels (0 or 1).

### 2. Train Naive Bayes Model

```python
# Code for training the Naive Bayes classifier
# Refer to the Naive_Bayes_Modal.ipynb notebook for detailed implementation
