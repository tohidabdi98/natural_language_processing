# Language Modeling and Tokenization in Persian and English Texts

## Overview
This notebook explores the concepts of language modeling and tokenization, focusing on Persian and English texts. It implements various preprocessing, modeling, and tokenization techniques to analyze and manipulate textual data.

### Key Objectives:
1. **Preprocessing Text:** Normalize and tokenize Persian text using the `hazm` library and other NLP tools.
2. **Language Modeling:** Train bigram, trigram, and 5-gram models with Laplace smoothing to analyze word dependencies and generate sentences.
3. **Tokenization:** Compare tokenization methods, including white-space, spaCy, and Byte Pair Encoding (BPE), for Persian and English texts.

---

## Notebook Highlights
### Part 1: Language Modeling
- **Preprocessing Persian Text:**
  - Normalization with `hazm.Normalizer`.
  - Sentence segmentation and tokenization.
  - Padding for n-gram creation.
- **Building Language Models:**
  - Train bigram, trigram, and 5-gram models using Laplace smoothing.
  - Evaluate the importance of smoothing and generate synthetic sentences.
- **Model Comparison:**
  - Analyze the trade-offs between 2-gram, 3-gram, and 5-gram models.
  - Measure perplexity to compare sentence generation probabilities.

### Part 2: Tokenization
- **Tokenization Methods:**
  - White-space tokenization.
  - Tokenization using `spaCy` and BPE.
- **Comparison:**
  - Analyze the number of tokens and accuracy of each method.
  - Evaluate tokenization efficiency for English and Persian texts.
- **Detailed Analysis:**
  - Highlight challenges in tokenizing complex languages like Persian.
  - Demonstrate advantages of sub-word tokenization using BPE.

---

## How to Use
1. Install the required libraries:
pip install hazm nltk spacy tokenizers tabulate python -m spacy download en_core_web_sm

2. Prepare the dataset:
- Include `hp_en.txt` and `hp_fa.txt` in the same directory as this notebook.
3. Execute the notebook cells sequentially.

---

## Results and Observations
- N-gram models reveal word dependencies but show limitations with small vocabulary sizes.
- BPE tokenization efficiently handles out-of-vocabulary words and performs well in Persian.
- The trade-offs between accuracy and computational cost vary across tokenization methods.

---

## Acknowledgments
This notebook uses:
- `hazm` for Persian text processing.
- `nltk` for n-gram modeling and language processing.
- `spaCy` and `ByteLevelBPETokenizer` for tokenization comparisons.

Feel free to modify and expand this notebook for further experimentation!
