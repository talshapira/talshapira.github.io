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

<img src='http://talshapira.github.io/files/flowpic_apps.png' width="400" align="middle">

# Dataset

We use labeled datasets of packet capture (pcap) files from the Uni. of New Brunswick (UNB): ["ISCX VPN-nonVPN traffic dataset" (ISCX-VPN)](https://www.unb.ca/cic/datasets/vpn.html) and ["ISCX Tor-nonTor dataset" (ISCX-Tor)](https://www.unb.ca/cic/datasets/tor.html), as well as our own small packet capture (TAU), and conduct different types of experiments; (1) multiclass classification experiments over non-VPN/VPN/Tor and merged dataset, (2) class vs. all classification experiments, (3) application identification, and (4) classification of an unknown application.


## License

Our proceesed dataset (CSV files) is publicly available for researchers. If you are using our dataset, you should cite our related research paper, as well as UNB's related research papers which outlining the details of the dataset and its underlying principles:

* T. Shapira and Y. Shavitt, "FlowPic: Encrypted Internet Traffic Classification is as Easy as Image Recognition," IEEE INFOCOM 2019 - IEEE Conference on Computer Communications Workshops (INFOCOM WKSHPS), Paris, France, 2019, pp. 680-687.

* Gerard Drapper Gil, Arash Habibi Lashkari, Mohammad Mamun, Ali A. Ghorbani, "Characterization of Encrypted and VPN Traffic Using Time-Related Features", In Proceedings of the 2nd International Conference on Information Systems Security and Privacy(ICISSP 2016) , pages 407-414, Rome, Italy.

* Arash Habibi Lashkari, Gerard Draper-Gil, Mohammad Saiful Islam Mamun and Ali A. Ghorbani, "Characterization of Tor Traffic Using Time Based Features", In the proceeding of the 3rd International Conference on Information System Security and Privacy, SCITEPRESS, Porto, Portugal, 2017.

