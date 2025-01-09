# Sentiment Analysis Using LaBSE and Universal Sentence Encoder

This project implements a sentiment analysis model using TensorFlow and LaBSE (Language-agnostic BERT Sentence Embedding). It processes text data, trains a classification model, and evaluates its performance on test datasets.

## Features
- Preprocessing using Google's Universal Sentence Encoder Multilingual Preprocessor
- Fine-tuned classification model based on LaBSE
- Multi-class sentiment analysis with a custom dataset
- Evaluation on an external test dataset (SnapFood dataset)
- Metrics: Accuracy, Precision, Recall, F1-Score, and Confusion Matrix

## Installation

Ensure you have Python installed. Install the required dependencies by running:

pip install -U sentence-transformers datasets tensorflow tensorflow-text tf-transformers tf-models-official

Clone the repository containing the data:

git clone https://github.com/phosseini/SentiPers

## Dataset
- **SentiPers**: Persian sentiment dataset with labeled polarity values.
- **SnapFood**: External test dataset for evaluating the model's performance.

## Usage

1. **Data Preprocessing**:
   - Map sentiment labels to numerical categories.
   - Split the dataset into training, validation, and test sets.
   - Convert text data to tensors for use with TensorFlow.

2. **Model Architecture**:
   - Text preprocessing using Universal Sentence Encoder.
   - Embedding generation with LaBSE.
   - Fully connected layers for classification.

3. **Training**:
   - Train the model using categorical cross-entropy loss and AdamW optimizer.
   - Early stopping to prevent overfitting.

4. **Evaluation**:
   - Compute metrics (Accuracy, Precision, Recall, F1-Score).
   - Generate confusion matrices for detailed analysis.

5. **External Dataset Testing**:
   - Apply the trained model to the SnapFood dataset.
   - Transform labels and compute performance metrics.

## Running the Code

Run the script:

python sentiment_analysis_labse_tensorflow.py

The script performs the following:
- Trains the sentiment analysis model.
- Evaluates the model on the test set.
- Generates metrics and plots for label distribution and performance.

## Results

### Metrics on SentiPers Test Set:
- **Accuracy**: 62.46%
- **Precision**: 62.46%
- **Recall**: 62.46%
- **F1-Score**: 62.46%

### Metrics on SnapFood Test Set:
- **Accuracy**: 69.64%
- **Precision**: 69.64%
- **Recall**: 69.64%
- **F1-Score**: 69.64%


## Visualizations

### SentiPers Label Distribution:
- Bar plot of the distribution of labels in the SentiPers dataset.

### SnapFood Label Distribution:
- Bar plot of the distribution of labels in the SnapFood dataset.

## Acknowledgements
- SentiPers Dataset: [GitHub Repository](https://github.com/phosseini/SentiPers)
- SnapFood Dataset: A Persian dataset for sentiment analysis in restaurant reviews.

## License
This project is licensed under the MIT License.
