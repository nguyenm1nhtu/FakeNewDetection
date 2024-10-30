# FakeNewDetection

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Manual Testing](#manual-testing)
- [Models Used](#models-used)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Project Structure](#project-structure)

## Introduction

In the era of information overload, distinguishing between fake and real news has become increasingly challenging yet crucial. This project leverages machine learning techniques to build a Fake News Detection System. By utilizing TF-IDF vectorization and various classification algorithms, the system effectively classifies news articles as fake or genuine.

## Features

- **Data Preprocessing:** Cleans and normalizes text data by removing URLs, special characters, stopwords, and applying lemmatization.
- **Visualization:** Generates word clouds to visualize the most frequent words in fake and real news.
- **Multiple Classifiers:** Implements and evaluates multiple machine learning models, including Multinomial Naive Bayes, Random Forest, Logistic Regression, and SGD Classifier.
- **Manual Testing:** Allows users to input custom news articles and see predictions from all models.
- **Performance Evaluation:** Provides accuracy, precision, recall, F1 score, and confusion matrices for each model.

## Dataset

The dataset comprises two CSV files:

- **Fake.csv:** Contains fake news articles.
- **True.csv:** Contains genuine news articles.

Each file includes the following columns:

- `title`: The title of the news article.
- `text`: The main content of the news article.
- `subject`: The subject category of the news.
- `date`: The publication date of the news article.

## Manual Testing

After running the script, you will be prompted to enter a news article for classification. The system will display predictions from all implemented models.

**Example:**

```diff
===== Fake News Detection System =====

Text: Your news article here...
Output:
```

```sql
Predictions from models:
    Model                Result
0   Naive Bayes          Fake New
1   Random Forest        Fake New
2   Logistic Regression  Fake New
3   SGD                  Fake New
```

## Models Used

1. Multinomial Naive Bayes
2. Random Forest Classifier
3. Logistic Regression
4. SGD Classifier

Each model is trained on the TF-IDF vectorized data and evaluated using standard classification metrics.

## Evaluation Metrics

The following metrics are used to evaluate the performance of each model:

- Accuracy: The proportion of correctly classified instances.
- Precision: The proportion of positive identifications that were actually correct.
- Recall: The proportion of actual positives that were identified correctly.
- F1 Score: The harmonic mean of precision and recall.
- Confusion Matrix: A table used to describe the performance of the classification model.

## Results

**Multinomial Naive Bayes**
```yaml
Evaluted the model Multinomial Naive Bayes
Accuracy: 0.9398663697104677
Precision: 0.924948358962589
Recall: 0.9497996700447796
F1 Score: 0.9372093023255814
Confusion Matrix:
 [[4410  327]
 [ 213 4030]]
 ```

**Random Forest**
```yaml
Evaluted the model Random Forest
Accuracy: 0.9914253897550112
Precision: 0.9903483992467044
Recall: 0.9915154371906669
F1 Score: 0.9909315746084089
Confusion Matrix:
 [[4696   41]
 [  36 4207]]
 ```

**Logistic Regression**
```yaml
Evaluted the model Logistic Regression
Accuracy: 0.9875278396436525
Precision: 0.9833840393166393
Recall: 0.9903370256893708
F1 Score: 0.9868482855800845
Confusion Matrix:
 [[4666   71]
 [  41 4202]]
 ```

**SGD Classifier**
```yaml
Evaluted the model SGD Classifier
Accuracy: 0.9913140311804008
Precision: 0.9875907281667057
Recall: 0.9941079424935187
F1 Score: 0.9908386187455955
Confusion Matrix:
 [[4684   53]
 [  25 4218]]
```

**Observation:**

- Random Forest and SGD Classifier exhibit the highest accuracy, precision, recall, and F1 scores, indicating superior performance in classifying fake and real news.
- Multinomial Naive Bayes also performs well but slightly lags behind the other models.
- Logistic Regression demonstrates robust performance with high recall and F1 scores.

## Project Structure

```python
fake-news-detection/
├── Data/
│   ├── Fake.csv.zip
│   └── True.csv.zip
├── fake_news_detection.py
├── README.md
```

- Data/: Contains the zipped dataset files.
- fake_news_detection.py: The main Python script for data preprocessing, model training, evaluation, and manual testing.
- README.md: This documentation file.