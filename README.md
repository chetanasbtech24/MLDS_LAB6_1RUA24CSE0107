# Sentiment Analysis using RNN, LSTM, GRU and Bidirectional LSTM

## Author

**Name:** Chetana S
**USN:** 1RUA24CSE010

---

## Overview

This project focuses on building and evaluating deep learning models for sentiment analysis using the Twitter US Airline Sentiment dataset. The objective is to classify tweets into three sentiment categories: positive, neutral, and negative. Multiple recurrent neural network architectures are implemented and compared to analyze their performance on textual data.

---

## Objectives

* Perform data preprocessing and text cleaning
* Explore dataset characteristics through visualizations
* Implement and compare RNN, LSTM, GRU, and Bidirectional LSTM models
* Evaluate model performance using appropriate metrics
* Perform hyperparameter tuning for performance optimization

---

## Dataset

The dataset used is the Twitter US Airline Sentiment dataset from Kaggle.
It contains tweets labeled with sentiment and additional metadata.

Key columns used:

* `text`: Raw tweet content
* `airline_sentiment`: Sentiment label (positive, neutral, negative)

---

## Preprocessing

The following preprocessing steps were applied:

* Lowercasing text
* Removing URLs, mentions, hashtags, punctuation, and numbers
* Removing stopwords using NLTK
* Tokenization and sequence padding
* Label encoding of sentiment classes

---

## Model Architectures

The following models were implemented:

### 1. Simple RNN

* Embedding Layer
* SimpleRNN Layer
* Dropout
* Dense Output Layer

### 2. LSTM

* Embedding Layer
* LSTM Layer with dropout and recurrent dropout
* Dropout
* Dense Output Layer

### 3. GRU

* Embedding Layer
* GRU Layer with dropout and recurrent dropout
* Dropout
* Dense Output Layer

### 4. Bidirectional LSTM

* Embedding Layer
* Bidirectional LSTM (stacked)
* Dropout layers
* Dense layers

---

## Training Strategy

* Train/Validation/Test split: 70/15/15
* Loss Function: Sparse Categorical Crossentropy
* Optimizer: Adam
* Metrics: Accuracy
* EarlyStopping and ModelCheckpoint callbacks used

---

## Evaluation Metrics

* Accuracy
* Precision, Recall, F1-score
* Confusion Matrix

---

## Results Summary

* Bidirectional LSTM achieved the highest performance due to its ability to capture context in both directions
* GRU provided a good balance between performance and computational efficiency
* Simple RNN showed comparatively lower performance due to limited memory capabilities

---

## Hyperparameter Tuning

A manual grid search was performed over:

* Embedding dimensions
* Number of units
* Dropout rates

The best-performing configuration was retrained and evaluated on the test set.

---

## Key Observations

* The dataset is imbalanced, with negative tweets dominating
* Neutral class is more difficult to classify accurately
* Pre-trained embeddings could further improve performance
* More complex models tend to overfit without proper regularization

---

## Technologies Used

* Python
* NumPy, Pandas
* Matplotlib, Seaborn
* NLTK
* Scikit-learn
* TensorFlow / Keras

---

## Conclusion

This experiment demonstrates the effectiveness of different recurrent architectures for sentiment analysis. Bidirectional LSTM provides the best performance, while GRU offers a more efficient alternative. Proper preprocessing, model tuning, and evaluation are critical for achieving reliable results.

---

## Repository Structure

```
├── Sentiment_Analysis_RNN_LSTM_GRU_Assignment.ipynb
├── README.md
├── dataset/
│   └── Tweets.csv
```

---

## How to Run

1. Install required libraries
2. Open the Jupyter Notebook
3. Run cells sequentially
4. Ensure dataset is available in the working directory

---

## License

This project is developed for academic purposes.
