# Sentiment Analysis with Neural Networks

# Overview
This project demonstrates sentiment analysis on a Twitter dataset using different Recurrent Neural Network (RNN) architectures.
It preprocesses the dataset, tokenizes the text, and applies word embeddings (GloVe) for better feature representation.
Models used include RNN, LSTM, and GRU, trained both with and without GloVe embeddings.
Results are evaluated using accuracy and confusion matrices.

# Dataset
Source: http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip
Training Data: training.1600000.processed.noemoticon.csv
Test Data: testdata.manual.2009.06.14.csv

# Prerequisites
Ensure the following libraries are installed:
pip install numpy pandas nltk torch keras matplotlib tqdm scikit-learn

# Download necessary NLTK data
python -c "
import nltk
nltk.download('punkt')
nltk.download('stopwords')
"

# Steps
## 1. Data Preprocessing
- Convert text to lowercase.
- Expand clitic contractions.
- Remove URLs and punctuation.
- Tokenize text and remove stopwords.
- Apply stemming using PorterStemmer.

## 2. Tokenization and Padding
- Tokenize text using Keras’ Tokenizer.
- Convert tokenized text to numerical sequences and pad them to a fixed length of 33.

## 3. Word Embeddings
- Use GloVe embeddings (300-dimensional) to create feature tensors for the text.

## 4. Neural Network Models
Architectures Implemented:
- RNN: Basic Recurrent Neural Network.
- LSTM: Long Short-Term Memory Network.
- GRU: Gated Recurrent Unit Network.
Models with GloVe:
- RNN, LSTM, GRU trained using GloVe embeddings.

## 5. Training and Evaluation
Loss function: CrossEntropyLoss
Optimizer: Adam with a learning rate of 0.001
Number of epochs: 20

# Metrics:
- Accuracy: Measured on test data.
- Confusion Matrix: Shows the performance for each class.

# Results
Without GloVe:
Model | Accuracy
RNN   | 49.3%
LSTM  | 49.9%
GRU   | 46.2%

With GloVe:
Model | Accuracy
RNN   | 76.3%
LSTM  | 77.4%
GRU   | 77.4%

# Confusion Matrices:
Example (RNN with GloVe):
[[134,  42],
[ 43, 140]]

# Visualizations
- Class Distribution: A bar plot showing the distribution of positive and negative classes in the training data.

# How to Run
1. Clone or download the dataset.
2. Run the script after ensuring all dependencies are installed.
3. Monitor the training progress and evaluate results using the printed accuracy and confusion matrices.

# Conclusion
Using pre-trained word embeddings significantly improves the performance of RNN-based architectures for sentiment analysis.
This demonstrates the importance of feature representation in natural language processing tasks.
