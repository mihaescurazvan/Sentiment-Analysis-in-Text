# Sentiment-Analysis-in-Text

This project is a sentiment analysis task performed on the [Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140) dataset from Kaggle, which contains 1.6 million tweets labeled as positive or negative. The aim of this project is to build a binary classification model that can predict the sentiment of a given text.


## Dataset

The Sentiment140 dataset was used for this project, which contains tweets labeled as either positive or negative. The dataset has 1.6 million tweets, with 800,000 samples for each class, making it a perfectly balanced dataset. For this project, only the tweets column and the target column were used.


## Exploratory Data Analysis

Exploratory data analysis was performed on the dataset to gain insights into the data. The analysis revealed that the dataset was very large, with 1.6 million tweets. Since this project was focused on NLP, only the tweets and the target columns were kept for further analysis. The data was balanced, with 800,000 samples for each class.


## Data Preprocessing

Before feeding the data to the models, some preprocessing was performed on the data to clean it and prepare it for analysis. I have decided decided to use only **10%** of the data for the project, resulting in 160k samples. This decision was made to keep the execution time of the project low.
Next, the following preprocessing steps were performed:

  * **Stopword removal**: Stopwords are words that do not provide useful information, such as "the", "and", "a", etc. These words were removed from the tweets.
  * **Removal of hyperlinks and mentions**: Hyperlinks and mentions were removed from the tweets, as they do not provide useful information about the sentiment.
  * **Removal of punctuations**: Punctuations were removed from the tweets, as they do not contribute to the sentiment of the text.


## Data Splitting

The data was split into training, validation, and testing sets. **80%** of the data was used for training, **9%** was used for validation, and **10%** was used for testing. This resulted in 129,600 tweets for training, 14,400 tweets for validation, and 16,000 tweets for testing.


## Tokenization and Vectorization

Tokenization is the process of breaking down a sentence into words. In this project, the **Tokenizer** provided by Keras was used to tokenize the tweets. The Tokenizer creates tokens for every word in the data corpus and maps them to an index using a dictionary.

After tokenization, the method **texts_to_sequences** was used to convert the whole sentences to a vector representation. The **pad_sequences** method was used to adjust the size of the vectors so that we get a uniformly spaced/sized vector.

For vectorization, pre-trained word vectors from the 100 dimension version of **GloVe (Global Vectors for Word Representation)** by Stanford were used.


## Models

Three deep learning models were trained for this project using **RNNs** and **CNNs** and even combining them. The models were trained on the training data and evaluated on the validation data. The models were then tested on the testing data to evaluate their performance.

After training the RNNs and CNNs, a smaller version of **BERT (Bidirectional Encoder Representations from Transformers)**, the **smallBERT** was used, which gave the best performances. Transformers are the state-of-the-art models now, outperforming RNNs and CNNs, and performing very well in NLP tasks.


## Conclusion

In conclusion, this project demonstrates how sentiment analysis can be performed on textual data using deep learning models. Preprocessing the data and selecting the appropriate model architecture are critical steps in achieving good performance. Transformers are currently the best models for NLP tasks, and it is essential to explore them for similar projects.
