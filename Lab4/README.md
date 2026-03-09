# GenAI-Lab-4
# CSET419: Text Generation with RNN/LSTM and Transformers

## Objective
The objective of this lab is to design and implement simple text generation models that can learn patterns from a given text corpus and generate new sequences.

## Dataset
The models were trained on a specialized corpus covering Artificial Intelligence, Machine Learning, and Transformer architectures.

## Architectures Implemented

### Component I: RNN / LSTM
- **Architecture**: Embedding Layer -> LSTM (150 units) -> Dense (Softmax).
- **Key Metric**: Achieved a training accuracy of **99.17%** and a loss of **0.1418**.
- **Technicality**: Uses a hidden state to manage temporal dependencies through gating mechanisms (Input, Forget, Output).

### Component II: Transformer
- **Architecture**: Multi-Head Self-Attention -> Positional Encoding -> Feed-Forward Network.
- **Key Metric**: Achieved a final loss of **0.0949**.
- **Technicality**: Leverages parallel processing and self-attention to capture global context across the corpus.

## Results
Both models successfully generated coherent text based on the training data.The Transformer model showed faster convergence and a lower final loss compared to the LSTM.
