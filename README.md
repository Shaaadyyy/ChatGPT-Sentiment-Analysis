# ChatGPT-Sentiment-Analysis
Classification model has been trained by two models (CNN, LSTM) to predict the label of the tweets.

Steps to build a classifier using word embedding, CNN and LSTM:-
* process text samples:
  * tokenize samples to words and keep top 20,000 most commonly occuring words in the dataset and neglect the others.
  * form a dictionary of all words in the dataset.. the dictionary maps a word to a word ID
  * replace each word by its ID
  * truncate/pad the sequences to a maximum length of 1000 words
* Each label will be a binary vector of size 20
* splitting dataset to 80 % will be used as training data for the classifier. While the other 20 % will be used as testing data for your model to be able to identify the “accuracy percentage” of your classifier with the data that have not seen before from the classifier.
* Build a dictionary mapping words in the embeddings set to their embedding vector.
* the words in the dataset that don't exist in Glove's dictionary will get a zeroes vector these words already have id 0 so there zeros embedding ector will be at index zero in the new matrix.
* responsible of converting a paded sequence of words IDs to a sequence of words embeddings.
* build, compile and run two models. First model is CNN model and the second one is LSTM model.

**CNN Sentiment Analysis**
![CNN](../master/images/cnn-result-test.png)


**LSTM Sentiment Analysis**
![CNN](../master/images/lstm-result-test.png)
