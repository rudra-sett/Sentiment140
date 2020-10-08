# Sentiment140
A multi-channel convolutional neural network for sentiment detection

An LSTM would probably work better for this problem, but I wanted to try a CNN. It mostly works.

It currently can do some interesting things. For example, it learns negative adjectives and will classify sentences comtaining those words as negative. However, putting a "not" before such an adjective will often switch the classification to positive.

Currently, the network achieves roughly a 79% accuracy on a validation subset of the data.

Future changes:
Use Word2Vec or GLoVe embeddings to potentially improve accuracy and speed up training. 
