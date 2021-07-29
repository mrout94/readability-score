# Readability Score using NLP and RoBERTa
Using RoBERTa and 🤗 library to do assign a readability score to an excerpt of text paragraphs.  
This model achieves a **RMSE score of 0.45**.  
You can try and modify this notebook on Google Colab using [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Urf6RB5QIyq8WvizRllifYjyEsSPTdV3?usp=sharing)  

## Credits
The training Dataset was collected from a [Kaggle competition](https://www.kaggle.com/c/commonlitreadabilityprize)

## Problem Statement
Build algorithms to rate the complexity of reading passages for grade 3-12 classroom use. To accomplish this, we have to pair our machine learning skills with a dataset that includes readers from a wide variety of age groups and a large collection of texts taken from various domains.

## Data Description
We're predicting the reading ease of excerpts from literature. The organisers provided excerpts from several time periods and a wide range of reading ease scores.  
The following features were provided along with the text:-
| Feature Name | Description |
|------------|-----------|
|id | unique ID for excerpt.|
|url_legal | URL of source - this is blank in the test set.|
|license | license of source material - this is blank in the test set.|
|excerpt | text to predict reading ease of|
|target | reading ease|
|standard_error | measure of spread of scores among multiple raters for each excerpt. Not included for test data.|

## Data Cleaning
Basic text cleaning procedures like removing emojis, web links, HTML tags, special characters etc.

## Model
* This approach consists of a vanilla **roberta-base** model finetuned on our dataset using **PyTorch**.
* I have also demonstrated the use for no-decay to improve model performance.
* Other Deep Learning concepts like Optimizer, scheduler, dropout etc have been covered with their implementation in Pytorch.
* Regularization has also been demonstrated and used to reduce overfitting.

## Performance
**RMSE: 0.45**
