# Conditional-Similarity-Network-MNIST
This is a toy example of Conditional Similarity Networks on MNIST dataset. It is based on a paper named "Conditional Similarity Networks" written by A. Veit, S. Belongie and T. Karaletsos.

## Overview
In this paper, they proposed a network named "Conditional Similarity Network" to measure the similarity between images having various attributes. The network consists of two partial networks. One is Convolutional Network to extract features from an image, and the other is a set of mask, each of which is corresponding to one attribute(color, shape, category or something), and works as an element-wise gating function selecting relevant features of the attributes from a feature vector. The most important thing is that the set of mask is also trainable. That is, the masks learn by themselves what features are actually need to distinguish images with respect to the corresponding attributes.

## The characteristics of the network
It is based on deep metric learning. Deep metric learning is to train a network that maps similar input data to similar feature vectors. It means that deep metric network embeds input data in high dimensional space into low dimensional space, conserving the metric between the data. The most usual way to implement deep metric leaning is triplet network. First, we pick a input x, calle an anchor. Then We choose a positive sample x+, which is similar to x(for example, x+ is in the same category with x), and a negative sample x-, which is not similar to x. Now, we construct a 3 parallel networks, each of which has the same weights with the others, and feed a pair of inputs (x, x+, x-) into the networks. 
