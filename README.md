# Vietnamese Sentiment Analysis on Crawled Restaurant Reviews with fine-tuning PhoBERT model

## Abstract

This project focuses on binary sentiment analysis of Vietnamese restaurant reviews – a challenging task due to the language’s restricted availability of datasets. I investigate the effectiveness of fine-tuning a pre-trained language model named PhoBERT to solve this problem. Adapting this PhoBERT to Vietnamese crawled reviews from Google Maps is to classify the restaurant reviews as positive or negative. Moreover, the baseline systems for comparsion are the robust fine-tuned BERT models from another previous research and two machine learning model. The experimental results demonstrate that this approach significantly enhances performance through the metrics of classification. In addition, a deep analysis of crawled dataset and model’s predictions will clarify the reliability of this project. Ultimately, this work provides a practical solution for a framework of text classification within the restaurant domain, thus offering valuable insights for Vietnamese businesses.

## Getting Started

This project include three folders:
* data-collection: The cod files of collecting URLs and reviews.
* data-preprocessing: The code files of cleaning, word segmentation, and splitting.
* model-implementation: The code files of fine-tuning PhoBERT model, machine learning models, and fine-tuned BERT models. Specifically, two machine learning models (Linear SVM and Multinomial Naïve Bayes) and 4 fine-tuning BERT-based models was implemented to compared with my fine-tuning PhoBERT model.

## Dataset

* Description:

| Train | Test | Totally |
| --- | --- | --- |
| 30256 records (15268 Pos & 14988 Neg) | 7576 records (3828 Pos & 3748 Neg) | 37832 records |

* Statistical attributes:

| Attribute | Values |
| --- | --- |
| No. of samples | 55.45 |
| No. of labels | 63.75 |
| Level | 1 |
| Minimum length (word) | 1 |
| Maximum length (word) | 134 |
| Average length (word) | 18.6 |
| Vocabulary size | 12940 |

## Comparison

### Baseline systems
The goals of baseline systems is to evaluate the effectiveness of my fine-tuned model; and verify that my dataset and the process of preprocessing are working correctly. Therefore, I established baseline systems against my fine-tuned model:
* Traditional ML Approach: Linear SVM and Multinomial Naïve Bayes are popular and effective algorithms for text classification. I trained these models on my dataset by using the available library scikit-learn of Python.s
* Fine-tuning Approach: there are 4 fine-tuned models (BERT-base, BERT-LSTM, BERT-TextCNN, and BERT-RCNN). They combined BERT model with many types of deep learning models in order to enhance the efficiency of BERT on Sentiment Analysis.

### Results

| Model | Accuracy | Precision(%) | Recall(%) | F1(%) |
| --- | --- | --- | --- | --- |
| Linear SVM | 91.30 | 91.35 | 91.43 | 91.39 |
| Multinomial NB | 89.80 | 89.50 | 90.43 | 89.96 |
| BERT-base | 90.68 | 88.94 | 93.12 | 90.99 |
| BERT-LSTM | 91.45 | 91.38 | 91.74 | 91.56 |
| BERT-TextCNN | 90.72 | 91.28 | 90.25 | 90.76 |
| BERT-RCNN | 91.01 | 90.92 | 91.32 | 91.12 |
| PhoBERT-base-v2 | 93.59 | 93.24 | 94.14 | 93.69 |

## Team

```
Student: Phan Lam Thanh Du
Mentor: Ph.D Duong Viet Hang
```

University of Information Technology, Vietnam National University - HCM City

Ho Chi Minh City, Viet Nam