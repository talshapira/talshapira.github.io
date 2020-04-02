---
title: "FlowPic's Project Page"
excerpt: "We introduce a novel approach for encrypted Internet traffic classification and application identification by transforming basic flow data into a picture, a FlowPic, and then using known image classification deep learning techniques, Convolutional Neural Networks (CNNs), to identify the flow category (browsing, chat, video, etc.) and the application in use.  <br/><br/><img src='http://talshapira.github.io/files/FlowPic_sys.png'>"
collection: portfolio
---

# FlowPic

Identifying the type of a network flow or a specific application has many advantages, but become harder in recent years due to the use of encryption, e.g., by VPN and Tor. 
Current solutions rely mostly on handcrafted features and then apply supervised learning techniques for the classification. 
	
We introduce a novel approach for encrypted Internet traffic classification and application identification by transforming basic flow data into a picture, em a FlowPic, and then using known image classification deep learning techniques, Convolutional Neural Networks (CNNs), to identify the flow category (browsing, chat, video, etc.) and the application in use. 

# Approach

1. Extract records from each flow, which comprised of a list of pairs, {IP packet size, time of arrival} for each packet in the flow.
2. Split each unidirectional flow to equal blocks (15/60 seconds).
3. Generate 2D-histogram. For simplicity, we set the 2D-histogram to be a square image.
4. Feed a Convolution Neural Network.

<img src='http://talshapira.github.io/files/FlowPic_sys.png'>


# FlowPics Exploration

<img src='http://talshapira.github.io/files/flowpic_categories.png'>

<img src='http://talshapira.github.io/files/flowpic_apps.png' width="400">

