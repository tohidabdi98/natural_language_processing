# Persian Sentiment Analysis with TF-IDF and PPMI Using Naive Bayes Classifiers

## Overview
This script processes Persian text data for sentiment analysis using feature extraction techniques like TF-IDF and Positive Pointwise Mutual Information (PPMI). The data is analyzed using Gaussian and Multinomial Naive Bayes classifiers to evaluate their performance in predicting sentiment labels.

---

## Features
1. **Data Preprocessing**  
   - Normalization and tokenization of Persian text using the `hazm` library.
   - Sampling an equal number of rows for each class for balanced training.
   - Splitting data into training and testing sets.

2. **Feature Extraction**
   - **TF-IDF:** Compute term frequency-inverse document frequency for feature representation.
   - **PPMI:** Build co-occurrence matrices and compute PPMI for capturing word relationships.

3. **Model Training**
   - Train Gaussian and Multinomial Naive Bayes classifiers on TF-IDF and PPMI-transformed features.
   - Evaluate model performance using precision, recall, and F1 scores.

4. **Evaluation**
   - Compare results of TF-IDF vs. PPMI features.
   - Analyze the performance difference between Gaussian and Multinomial Naive Bayes models.

---

## Installation
### Required Libraries
Install the necessary libraries using pip:
```bash
pip install hazm pandas scikit-learn
```

### Kaggle API
1. Upload the Kaggle API token (`kaggle.json`) for accessing the dataset.
2. Download the dataset:
   ```bash
   kaggle datasets download -d soheiltehranipour/snappfood-persian-sentiment-analysis
   ```
3. Unzip the downloaded file.

---

## Usage
1. Clone this repository and place the dataset (`Snappfood - Sentiment Analysis.csv`) in the working directory.
2. Run the script in a Python environment (e.g., Google Colab or Jupyter Notebook).
3. Observe model performance metrics for both TF-IDF and PPMI features.

---

## Results
### Metrics for Gaussian Naive Bayes (TF-IDF):
- Recall: **0.38**
- Precision: **0.67**
- F1 Score: **0.48**

### Metrics for Multinomial Naive Bayes (TF-IDF):
- Recall: **0.89**
- Precision: **0.78**
- F1 Score: **0.83**

### Metrics for Gaussian Naive Bayes (PPMI):
- Recall: **0.28**
- Precision: **0.60**
- F1 Score: **0.38**

### Metrics for Multinomial Naive Bayes (PPMI):
- Recall: **0.73**
- Precision: **0.72**
- F1 Score: **0.72**

---

## Observations
- TF-IDF features outperform PPMI features in both classifiers.
- Multinomial Naive Bayes consistently outperforms Gaussian Naive Bayes.
- PPMI provides insights into word relationships but is less effective than TF-IDF for this task.

---

## Acknowledgments
- Dataset: [Snappfood Persian Sentiment Analysis](https://www.kaggle.com/datasets/soheiltehranipour/snappfood-persian-sentiment-analysis)
- Libraries: `hazm`, `scikit-learn`, `pandas`

---

## License
This project is open-source and available for educational and research purposes.
