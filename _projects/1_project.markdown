---
layout: page
title: Decentralized Secure Cloud Storage using Blockchain
description: a major project for my Computer Engineering final year thesis.
img: /assets/img/major_project_thumbnail.png
fullwidth: true
---

A distributed peer-to-peer (P2P) network built over Kademlia Distributed Hash Table (DHT) protocol for secure storage of smaller files and user credentials. The system allows user to securely store the credentials or files in the network with the Service Term Agreement enforced using the Ethereum smart contract. 

The system has 4 parts: 
- **Node Jar Application** - a jar file that can be run at any machine to run as a node.
- **Android Application** - a mobile user interface to easily communicate with the network.
- **Node Web Application** - a desktop interface for node manager to view the details and status of the node.
- **Smart Contract** - to record transaction information such as file hashes stored at each node, payment history etc. 

The system provides 2 different services:
- **Secured File Storage** [PRIMARY] - to store user files using digital tokens as payment.
- **Secured Credentials Storage** - to store smaller piece of information at no cost.


---

Complete project source code is available at [my github repository](https://github.com/bipinkh/DECENTRALIZED-SECURE-CLOUD-STORAGE-USING-BLOCKCHAIN){:target="\blank"}.

View or download the final thesis report from [here](https://github.com/bipinkh/DECENTRALIZED-SECURE-CLOUD-STORAGE-USING-BLOCKCHAIN/blob/master/ThesisReport.pdf){:target="\blank"}.

--- 

#### **Secured Credentials Storage Service:**
This service allows user to store small piece of information such as credentials, passwords etc in the network at no cost. It implements the `Shamir's Secret Sharing Algorithm`.

*System workflow:*
- Using the mobile application, user sets the information as a key-value pair. It allows user to select the number of pieces to split them into and the threshold number limit for recovery.
- User can view the list of keys stored in the network, in the app.
- To see the credentials, user simply selects the key and the app reconstruct the secret value by combining at least the minimum threshold number of pieces.

The advantage of this service is that, the information can be retrieved even if the few nodes are down. If a information is splitted to 5 chunks with 3 recovery threshold value and if each 5 of them are stored at different node, to reconstruct the information, chunks form any of the 3 nodes irrespective of order is sufficient. This solves the issue with node downtime or node crash.

---

#### **Secured File Storage Service:**
This service allows user to store the files into the network.
<img class="col three left" src="{{ site.baseurl }}/assets/img/major_project_enc_algorithm.png" alt="" title="example image"/>

*System workflow:*
- The user logs into the android application using a Ethereum wallet address. User then selects one of the available nodes to act as a Postman node for him.
- The mobile application maintains the communication with the Postman node everytime.
- To store the file in the network, user selects the file from the application and send it to the Postman node after which the node encrypts the file using AES encryption, splits the encrypted file into smaller chunks, and store each of the chunks at several other nodes that are currently available.
- The user can view the list of nodes where the chunks of his files are stored in his application.
- During the file recovery, the Postman node calculates the total cost of service considering the size of file and storage cost for total time with each node. The mobile app then pays the total price in ERC-20 tokens using the wallet address.
- The file pieces are collected from all nodes and is combined, then decrypted to recreate the original file with 0% loss.
- The node manager can view the Web Application at any time to see the current volume consumed at his machines, number of files stored and the total tokens earned.

Since the node only stores a part of a file and only the user knows the list of nodes that are storing the file parts, the system provides a added layer of file security in the network with no central server.

---

#### **Project Screenshots:**

The images has been excluded for brevity.

Please refer to page 45 - 51 of the [thesis report](https://github.com/bipinkh/DECENTRALIZED-SECURE-CLOUD-STORAGE-USING-BLOCKCHAIN/blob/master/ThesisReport.pdf){:target="\blank"} for screenshots.

Alternatively, you can view/download the image files [here](https://github.com/bipinkh/DECENTRALIZED-SECURE-CLOUD-STORAGE-USING-BLOCKCHAIN/tree/master/final%20project%20screenshots){:target="\blank"}.