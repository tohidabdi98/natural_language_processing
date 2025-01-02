# Language Modeling and Tokenization in Persian and English Texts

## Overview
This notebook explores the concepts of language modeling and tokenization, focusing on Persian and English texts. It implements various preprocessing, modeling, and tokenization techniques to analyze and manipulate textual data.

### Key Objectives:
1. **Preprocessing Text:** Normalize and tokenize Persian text using the `hazm` library and other NLP tools.
2. **Language Modeling:** Train bigram, trigram, and 5-gram models with Laplace smoothing to analyze word dependencies and generate sentences.
3. **Tokenization:** Compare tokenization methods, including white-space, spaCy, and Byte Pair Encoding (BPE), for Persian and English texts.

---

## Notebook Highlights
### Question 1: Language Modeling
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

### Question 2: Tokenization
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
