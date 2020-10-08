# Sentiment140
A multi-channel convolutional neural network for sentiment detection. As the name suggests, it uses the Sentiment140 dataset, which is the biggest I've found so far.

An LSTM would probably work better for this problem, but I wanted to try a CNN. It mostly works.

It currently can do some interesting things. For example, it learns negative adjectives and will classify sentences comtaining those words as negative. However, putting a "not" before such an adjective will often switch the classification to positive.

Try some of these phrases:
"Apple's new products are not reasonably priced" - 87% confident that this is negative
"Apple's new products are reasonably priced" - 95% confident that this is positive
"Okay, at this point I am unsatisfied that this software mostly works" - 81% confident that this is negative
"Okay, at this point I am satisfied that this software mostly works" - 88% confident that this is positive
"I do regret moving here" - 87% confident that this is negative
"I do not regret moving here" - 87% confident that this is positive

Currently, the network achieves roughly a 79% accuracy on a validation subset of the data.

Future changes:
Use Word2Vec or GLoVe embeddings to potentially improve accuracy and speed up training. 
