# Toxic Comment Classification
## Overview
The threat of toxic, insulting, and hateful comments online can prevent quality discourse about topics on the internet. This Kaggle challenge sought to develop algorithms that can detect different types of negative online comments, including: toxic, severe toxic, insult, identity hate, threats, and obscenities. 

Because the dataset consisted of various written-speech samples (with corresponded labels), this project required utilizing Natural Language Processing (NLP) tools. I used two main NLP approaches in order to create an ensemble model with relatively high accuracy as measured by mean area under the curve (AUC) for the six different categories. 

# Methods
The first method involved using Term Frequency-Inverse Document Frequency (TF-IDF) transformation of both words and characters of varying lengths. This transformed sparse vectors were then fed into Naive-Bayes / Logistic Regression algorithms to create simple linear predictions. The second method involved using Gated Recurrent Unit (GRU) neural networks with trainable embedding for the chosen word vectors. I tried out three different word embeddings of varying length and training source. The outputs from all the models were simply averaged together in order to create an ensemble model.

Methods Utilized:
- GRU models with word embeddings
- TF-IDF transformed vectors with NB-Logistic Regression

## Results
In the end, the best leaderboard and cross-validation score was achieved when simply averaging the output from all the different models. At the time of posting, these results would place in the top 20th percentile of the competition (~800 / 4000), though there is still roughly two weeks to go until the end.

There are three different notebooks that make up the total project:
1. TF-IDF Linear Model
2. GRU Models with Embeddings
3. Ensemble Averaging of Results
