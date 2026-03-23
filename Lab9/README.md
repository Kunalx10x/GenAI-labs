# CSET419 -- Introduction to Generative AI

## Lab 9 -- Sequence Generation using LSTM and Transformer

------------------------------------------------------------------------

## 📌 Overview

This lab demonstrates how Generative AI models can be applied to
sequential data such as text sequences.\
The goal is to build models that can learn patterns from sequence data
and generate new meaningful sequences.

Two generative approaches are implemented:

-   Sequence Generation using LSTM (Recurrent Neural Network)
-   Sequence Generation using a Transformer-based Architecture

------------------------------------------------------------------------

## 🎯 Objectives

-   Understand sequential data and sequence prediction\
-   Implement generative neural network models\
-   Train models to learn patterns from text sequences\
-   Generate new sequences using trained models\
-   Compare traditional RNN-based models with Transformer models

------------------------------------------------------------------------

## 📊 Dataset

A small custom text dataset containing sentences related to:

-   Machine Learning\
-   Sequence Models\
-   RNN, LSTM, GRU\
-   Language Modeling\
-   Speech Recognition\
-   Time Series Forecasting\
-   Music Generation\
-   Generative AI

This dataset is used for training both models.

------------------------------------------------------------------------

## ⚙️ Implementation

### 🔹 Data Preprocessing

-   Tokenization of text\
-   Conversion of words into numerical sequences\
-   Creation of input-output sequence pairs\
-   Padding sequences to uniform length

------------------------------------------------------------------------

### 🔹 LSTM Based Sequence Generation

Model Architecture:

-   Embedding Layer\
-   LSTM Layer\
-   Dense Softmax Output Layer

The model learns sequential dependencies and predicts the next word in a
sequence.

------------------------------------------------------------------------

### 🔹 Transformer Based Sequence Generation

Model Components:

-   Word Embedding\
-   Positional Encoding\
-   Multi-Head Self Attention\
-   Feed Forward Network\
-   Global Pooling + Softmax Output

The Transformer captures long-range dependencies and contextual
relationships in sequences.

------------------------------------------------------------------------

## 📈 Results

The trained models generate new sequences such as:

-   deep learning improves sequence modeling performance\
-   sequence models process data step by step\
-   generative models learn probability distributions

Due to the small dataset size, outputs may sometimes be repetitive or
slightly imperfect.

------------------------------------------------------------------------

## 🚀 How to Run

1.  Install dependencies:

pip install tensorflow numpy

2.  Run the notebook cells sequentially:

-   Load dataset\
-   Preprocess data\
-   Train LSTM model\
-   Generate sequences\
-   Train Transformer model\
-   Generate sequences

------------------------------------------------------------------------

## 📌 Applications

-   Language Modeling\
-   Text Generation\
-   Chatbots\
-   Speech Processing\
-   Time-Series Prediction\
-   Music Generation

------------------------------------------------------------------------

## ✅ Conclusion

This lab shows how generative models can learn patterns from sequential
data and generate new sequences.\
LSTM models effectively capture temporal dependencies, while Transformer
models provide improved performance through attention mechanisms and
parallel processing.

------------------------------------------------------------------------

## 👨‍💻 Author

Kunal
