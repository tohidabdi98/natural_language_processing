## Overview
This project performs sentiment analysis on financial news headlines using natural language processing (NLP) techniques and machine learning models. It utilizes the Financial Phrase Bank dataset to classify sentences as positive, neutral, or negative sentiments.

---

## Features
- **Data Preprocessing**: 
  - Converts text to lowercase.
  - Removes punctuation.
  - Tokenizes sentences into words.
  - Removes stopwords.
  - Applies stemming for dimensionality reduction.

- **Word Embeddings**:
  - Uses GloVe pre-trained embeddings (100-dimensional vectors) to represent words.
  - Creates an embedding matrix for each sentence.

- **Machine Learning Models**:
  - Logistic Regression for classification.
  - Multinomial Naive Bayes for probabilistic modeling.

- **Performance Metrics**:
  - Computes precision, recall, F1-score.
  - Constructs confusion matrices for detailed evaluation.

---

## Workflow
1. **Dataset Preparation**:
   - Downloads the Financial Phrase Bank dataset using the Kaggle API.
   - Loads data into a Pandas DataFrame for processing.

2. **Text Preprocessing**:
   - Applies various NLP techniques to clean and prepare text data.

3. **Feature Extraction**:
   - Uses GloVe embeddings to convert words into numeric vectors.
   - Flattens embeddings for machine learning compatibility.

4. **Model Training and Evaluation**:
   - Splits data into training and testing sets.
   - Trains Logistic Regression and Naive Bayes models.
   - Evaluates performance using metrics and confusion matrices.

---

## Results
- **Logistic Regression**:
  - Precision: 0.71
  - Recall: 0.71
  - F1-Score: 0.71

- **Naive Bayes**:
  - Precision: 0.71
  - Recall: 0.71
  - F1-Score: 0.71

---

## How to Run
1. Upload the Kaggle API key (`kaggle.json`) to authenticate.
2. Download the dataset:
   ```bash
   !kaggle datasets download -d ankurzing/sentiment-analysis-for-financial-news
   !unzip /content/sentiment-analysis-for-financial-news.zip
   ```
3. Run the script step by step in a Jupyter or Colab environment.

---

## Dependencies
- `pandas`
- `nltk`
- `gensim`
- `sklearn`
- `numpy`

Install dependencies via pip:
```bash
pip install pandas nltk gensim scikit-learn numpy
```

---

## Limitations
- Pre-trained GloVe embeddings may not capture domain-specific nuances in financial text.
- Additional tuning of hyperparameters and preprocessing steps might improve results.

---

## Acknowledgments
- Dataset: [Financial Phrase Bank](https://www.kaggle.com/datasets/ankurzing/sentiment-analysis-for-financial-news)
- Word Embeddings: [GloVe](https://nlp.stanford.edu/projects/glove/)
