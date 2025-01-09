# BERT-Based Multi-Class Text Classification with ParsBERT

This repository implements a multi-class text classification model using ParsBERT, a pre-trained BERT model fine-tuned for the Persian language. The project involves data preprocessing, model building, and evaluation for natural language processing (NLP) tasks.

---

## Features
- Preprocessing Persian text data.
- Leveraging `ParsBERT` for feature extraction.
- Custom transformer-based classifier head.
- Training, validation, and testing pipelines.
- Evaluation using accuracy, F1-score, and confusion matrix.
- Visualizing training and validation metrics.

---

## Requirements

Install the necessary Python libraries.

---

## Dataset

The project uses the **FarsTail** dataset for training, validation, and testing. Clone the dataset repository.

Ensure that the dataset is placed correctly in the project directory.

---

## Usage

1. **Preprocess the Dataset**:
   - Load the training, validation, and test datasets.
   - Clean text using regex patterns to retain Persian text only.
   - Encode labels into numerical format.

2. **Tokenization**:
   Tokenize the premise and hypothesis using the ParsBERT tokenizer.

3. **Model Architecture**:
   - Two models are explored:
     - **Custom Classification Head**: ParsBERT with a dense classification head.
     - **ParsBERT Sequence Classifier**: Fine-tuned for direct classification.

4. **Training**:
   Train the models with the following parameters:
   - Batch size: `32`
   - Epochs: `15` to `30`
   - Learning rate: `PolynomialDecay` scheduler.

5. **Evaluation**:
   Evaluate the models using:
   - Accuracy
   - F1-Score (micro)
   - Confusion Matrix

6. **Visualization**:
   - Plot training and validation loss.
   - Plot training and validation accuracy.

---

## Example Results

### Task 1 (Custom Classification Head):
- **Accuracy**: `43.47%`

### Task 2 (ParsBERT Fine-Tuned):
- **Accuracy**: `45.52%`
- **F1-Score**: `45.52%`
- **Confusion Matrix**:

[[219 157 123] 
[159 239 158] 
[132 123 254]]


---

## Visualizations

### Loss Plot
![Training and Validation Loss](images/loss_plot.png)

### Accuracy Plot
![Training and Validation Accuracy](images/accuracy_plot.png)

---

## How to Run
Run the provided script.

Make sure to adjust paths to the dataset if necessary.

---

## Acknowledgments

- [ParsBERT](https://github.com/hooshvare/parsbert) for providing pre-trained models for the Persian language.
- [FarsTail Dataset](https://github.com/dml-qom/FarsTail) for enabling this NLP task.
- Libraries: `TensorFlow`, `Transformers`, `Keras-NLP`, and `HuggingFace Datasets`.

---

## License
This project is open-sourced under the MIT license.
