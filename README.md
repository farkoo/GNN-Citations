# Node Classification with Graph Neural Networks

We want to classify a collection of articles into 7 categories. To do this, we used the **cora** dataset. This database contains article citations as a network and also has a set of node features.
In this notebook, we want to solve this problem with the help of three methods.

## Method one: Use Traditional measures
In this method, using Traditional measures, a set of network structure-dependent properties such as node degree, closseness centrality, betweenness centrality, page rank and etc. is calculated for each node, and using the results of these measures and node properties, and with the help of SVM classifier and Random Forest classifier, classify the nodes of this graph.
 
 ### Results of first method:
 * Traditional measures + SVM classifier => 31% Accuracy
 * Traditional measures + Node features + SVM classifier => 37% Accuracy
 * Traditional measures + Random Forest classifier => 27% Accuracy
 * Traditional measures + Node features + Random Fores classifier => 59% Accuracy
