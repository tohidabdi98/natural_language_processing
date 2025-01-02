# Word Embeddings using Skip-Gram and PCA Visualization

## Overview
This project demonstrates the implementation of the Skip-Gram model to generate word embeddings from a text corpus. The embeddings are visualized using PCA to reduce their dimensions and plot relationships between selected words.

## Features
1. **Text Preprocessing**: Removes special characters, tokenizes sentences and words, removes stopwords, and lemmatizes words.
2. **Vocabulary Building**: Creates a vocabulary from the corpus and maps words to unique IDs.
3. **Skip-Gram Model**: Implements a simple neural network for learning word embeddings.
4. **Training**: Optimizes word embeddings by minimizing a custom loss function.
5. **Visualization**: Uses PCA to reduce embeddings to two dimensions for easy plotting.

## Requirements
- Python 3.x
- Libraries: 
  - `nltk`
  - `requests`
  - `numpy`
  - `matplotlib`
  - `scikit-learn`

## Usage
1. Install the required libraries:
   ```bash
   pip install nltk numpy matplotlib scikit-learn requests
   ```
2. Run the script:
   run the notebook
3. View the visualization of word embeddings.

## Output
- Word embeddings are trained on a sample text (Shakespeare's works).
- A 2D plot showing relationships between selected words (`king`, `queen`, `man`, `woman`, etc.).

## Key Functions
1. **preprocess_text(text)**: Prepares the text for embedding training by cleaning and tokenizing.
2. **Skipgram**:
   - `build_vocab`: Constructs the word-to-ID mapping.
   - `generate_training_data`: Prepares the training data with context windows.
   - `train`: Optimizes embeddings using gradient descent.
   - `get_word_vector`: Retrieves the learned vector for a specific word.
3. **Visualization**:
   - PCA is used to project high-dimensional embeddings into 2D space.

## Example Plot
The output plot will show clusters and relationships, e.g., `king` and `queen` will have a similar vector direction as `man` and `woman`.

## Improvements
- Add negative sampling for efficient training.
- Explore different loss functions for better embeddings.
- Incorporate a larger corpus for training.

## References
- Original Skip-Gram model: Mikolov et al., "Efficient Estimation of Word Representations in Vector Space" (2013).
- PCA for dimensionality reduction: Jolliffe, I.T., "Principal Component Analysis" (2002).
