# Big Data Analytics

This repository contains the semester assignment of the M.Sc. course Big Data Analytics. More specific this assignment contains 2 main tasks, a text classification task & a duplicate detection task. Also this assingment was based to a former Quora's competition and all the data are publicly available by Quora.

## Task 1: Text Classification

At this part of the assignment we were called to classify articles based on their content. More specific the datasets contain a large amount of articles that belong to one of the following categories: `Bussiness`, `Entertainment`, `Health` & `Technology`.

The model that achieved the best scores at my expirements was Random Forest with SVD, scoring ~96% accuracy & F1-score.

You can check out this [notebook](https://github.com/VangelisTsiatouras/big-data-analytics/blob/main/notebooks/classification.ipynb) for more info.


## Task 2: Nearest Neighbor Search and Duplicate Detection

This task consists of two parts. The first part is about de-duplication using LSH with Cosine Similarity and Jaccard Similarity variations. The goal of this task is to detect similar small texts and extract approximatelly how many of them are duplicate, using the referred similarity metrics. Initially, a large amount of texts are loaded and then we query with a batch of texts expecting how many of them are duplicate or almost similar. Also by using LSH we estimate efficiently the approximate similar (or approximate nearest) texts. In that way we compare the input query texts to smaller amount of texts in contrast with a brute force technique that requires to check all the texts.

You can check out this [notebook](https://github.com/VangelisTsiatouras/big-data-analytics/blob/main/notebooks/deduplication.ipynb) for more info.

Finally, the last part is about duplicate detection. This was classic task of Quora at 2017 and more precisely it was about detecting similar Quora questions. Given a train dataset that contains pairs of questions along with boolean labels that indicate if they are duplicate, we have to train a model that can estimate efficiently and accurately question pairs about their context similarity. My model that scored almost ~77% accuracy with 75% F1-score consists of XGBoost Classifier with Word2Vec.

You can check out this [notebook](https://github.com/VangelisTsiatouras/big-data-analytics/blob/main/notebooks/duplicate_detection.ipynb) for more info.
