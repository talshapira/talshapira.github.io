---
title: "FlowPic: Encrypted Internet Traffic Classification is as Easy as Image Recognition"
collection: publications
permalink: /publication/flowpic_ni19
excerpt: 'FlowPic: Encrypted Internet Traffic Classification is as Easy as Image Recognition'
date: April 2019
venue: 'IEEE INFOCOM 2019 - IEEE Conference on Computer Communications Workshops (INFOCOM WKSHPS)'
paperurl: 'https://ieeexplore.ieee.org/document/8845315'
citation: 'T. Shapira and Y. Shavitt, "FlowPic: Encrypted Internet Traffic Classification is as Easy as Image Recognition," IEEE INFOCOM 2019 - IEEE Conference on Computer Communications Workshops (INFOCOM WKSHPS), Paris, France, 2019, pp. 680-687.'
---

Identifying the type of a network flow or a specific application has many advantages, but become harder in recent years due to the use of encryption, e.g., by VPN and Tor. Current solutions rely mostly on handcrafted features and then apply supervised learning techniques for the classification. We introduce a novel approach for encrypted Internet traffic classification by transforming basic flow data into a picture, a FlowPic, and then using known image classification deep learning techniques, Convolutional Neural Networks (CNNs), to identify the flow category (browsing, chat, video, etc.) and the application in use. We show using the UNB ISCX datasets that our approach can classify traffic with high accuracy. We can identify a category with very high accuracy even for VPN and Tor traffic. We classified with high success VPN traffic when the training was done for a non-VPN traffic. Our categorization can identify with good success new applications that were not part of the training phase. We can also use the same CNN to classify applications with an accuracy of 99.7%. Overall, our approach achieves significant better performance than previous work, and can handle classification problems that were not studied in the past.

[Download paper here](https://ieeexplore.ieee.org/document/8845315)

Recommended citation: T. Shapira and Y. Shavitt, "FlowPic: Encrypted Internet Traffic Classification is as Easy as Image Recognition," IEEE INFOCOM 2019 - IEEE Conference on Computer Communications Workshops (INFOCOM WKSHPS), Paris, France, 2019, pp. 680-687.
