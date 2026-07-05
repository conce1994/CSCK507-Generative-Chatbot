# Generative Chatbot using Sequence-to-Sequence Models

## Overview

This repository contains the implementation of a generative chatbot developed as part of the Natural Language Processing (NLP) module at the University of Liverpool.

The project investigates the use of Sequence-to-Sequence (Seq2Seq) neural networks for dialogue generation using the **Ubuntu Dialogue Corpus**, a large-scale customer support dataset consisting of approximately 930,000 two-person conversations extracted from Ubuntu IRC chat logs.

Two chatbot architectures are developed and compared:

- Seq2Seq model without an attention mechanism
- Seq2Seq model with an attention mechanism (Bahdanau or Luong)

The objective is to evaluate whether incorporating an attention mechanism improves the quality of generated responses.

---

## Project Objectives

The project addresses the following tasks:

- Explore and analyse the Ubuntu Dialogue Corpus.
- Perform data cleaning and preprocessing.
- Construct input-response dialogue pairs.
- Develop a Seq2Seq chatbot without attention.
- Develop a Seq2Seq chatbot with an attention mechanism.
- Split the dataset into training, validation and testing sets.
- Train both models using the training and validation datasets.
- Evaluate chatbot performance using BLEU score and qualitative response analysis.
- Compare both architectures and discuss their strengths and limitations.

---

## Dataset

This project uses the **Ubuntu Dialogue Corpus**, one of the largest publicly available conversational datasets for chatbot research.

Dataset characteristics:

- Approximately 930,000 conversations
- More than 100 million words
- Multi-turn technical support conversations
- Suitable for generative dialogue systems

---

## Repository Structure

```text
├── notebooks/
│   ├── 01_dataset_eda.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_seq2seq_baseline.ipynb
│   ├── 04_seq2seq_attention.ipynb
│   └── 05_evaluation.ipynb
│
├── data/
│   ├── dialogueText.csv
│   ├── dialogueText_196.csv
│   ├── dialogueText_301.csv
│   └── toc.csv
│
├── report/
│   └── Final_Report.pdf
│
├── presentation/
│   └── Project_Presentation.mp4
│
├── requirements.txt
└── README.md
```

---

## Exploratory Data Analysis

The EDA investigates the overall quality and characteristics of the dataset by examining:

- Dataset structure
- Missing values
- Duplicate records
- Dialogue utterance lengths
- Vocabulary size
- Most frequent words
- Rare words
- Tokenisation
- Recommended preprocessing decisions

Because of the large size of the Ubuntu Dialogue Corpus, a representative random sample of **100,000 dialogue utterances** is used during exploratory analysis to reduce computational requirements while preserving the overall characteristics of the dataset.

---

## Data Preprocessing

The preprocessing pipeline includes:

- Removing missing values
- Removing duplicate records
- Lowercasing all dialogue text
- Removing unnecessary punctuation and whitespace
- Tokenisation
- Vocabulary construction
- Rare word handling using the `<UNK>` token
- Sequence length filtering
- Sequence padding
- Addition of `<START>` and `<END>` tokens for decoder inputs

---

## Models

### Model 1 – Seq2Seq without Attention

A baseline encoder-decoder architecture using recurrent neural networks (LSTM or GRU) is implemented to generate dialogue responses.

### Model 2 – Seq2Seq with Attention

An enhanced encoder-decoder architecture incorporating an attention mechanism (Bahdanau or Luong) is developed to improve the quality of generated responses by allowing the decoder to focus on the most relevant parts of the input sequence.

---

## Evaluation

The chatbot models are evaluated using:

- BLEU Score
- Qualitative comparison of generated responses
- Performance comparison between the baseline and attention-based models

---

## Technologies

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- TensorFlow / Keras
- Scikit-learn

