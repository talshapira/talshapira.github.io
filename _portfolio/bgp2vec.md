---
title: "BGP2VEC Project Page"
excerpt: "We introduce a novel approach for Autonomous System (AS) embedding using deep learning based on only BGP announcments. Using these vectors we able to solve multiple important classification problem such as AS business types, AS Types of Relationship (ToR) and even IP hijack detection. <br/><br/><img src='http://talshapira.github.io/files/BGP2VEC_sys.png'>"
collection: portfolio
---


We introduce a novel approach for Autonomous System (AS) embedding using deep learning based on only BGP announcments. Using these vectors we able to solve multiple important classification problem such as AS business types, AS Types of Relationship (ToR) and even IP hijack detection.  Similar to natural language processing (NLP) models, the embedding represents latent characteristics of the ASN and its interactions on the Internet.  The embedding coordinates of each AS are represented by a vector; thus, we call our method BGP2VEC.

<p align="center">
<img src='http://talshapira.github.io/files/ToR_Gao.png' width="400">
</p>

# Method

Our method works as follows: first, using a shallow neural network, we map each AS number (ASN) to an embedded vector. 

The training procedure is done by feeding the network with the ASN pairs; the input is a one-hot vector representing the input ASN and the training outputs, which are also one-hot vectors representing the output ASNs (the context ASNs). Then applying gradient descent learning to adjust the weights of the network in order to maximize the log probability of any context word given the input word.

<img src='http://talshapira.github.io/files/as_route_ngram_example_fixed.png'>

Then, for each task; AS classification or ToR classification task, we activate Artificial Neural Network (ANN) that receives the vectors from the previous stage.

<img src='http://talshapira.github.io/files/BGP2VEC_sys_0.png'>
