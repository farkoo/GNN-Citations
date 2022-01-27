# Node Classification with Graph Neural Networks

We want to classify a collection of articles into 7 categories. To do this, we used the **cora** dataset. This database contains article citations as a network and also has a set of node features.
In this notebook, we want to solve this problem with the help of three methods.

## Method one: Use Traditional measures
In this method, using Traditional measures, a set of network structure-dependent properties such as node degree, closseness centrality, betweenness centrality, page rank and etc. is calculated for each node, and using the results of these measures and node properties, and with the help of SVM classifier and Random Forest classifier, classify the nodes of this graph.
 
 ### Results of the first method:
 * Traditional measures + SVM classifier => 31% acc.
 * Traditional measures + Node features + SVM classifier => 37% acc.
 * Traditional measures + Random Forest classifier => 27% acc.
 * Traditional measures + Node features + Random Fores classifier => 59% acc.

## The second method: Use FeedForward Neural Network 
We add eight FFN blocks with skip connections, so that we generate a baseline model with roughly the same number of parameters as the GNN models to be built later.

### Results of the second method:
* Traditional measures + 8-layer FFN model => 30% acc.
* Node features + 8-layer FFN model => 78% acc.
* Traditional measures + Node features + 8-layer FFN model => 69% acc.

## The third method: Use Graph Neural Network
The GNN classification model follows the Design Space for Graph Neural Networks approach, as follows:
1. Apply preprocessing using FFN to the node features to generate initial node representations.
2. Apply one or more graph convolutional layer, with skip connections, to the node representation to produce node embeddings.
3. Apply post-processing using FFN to the node embeddings to generat the final node embeddings.
4. Feed the node embeddings in a Softmax layer to predict the node class.

### Result of the third method:
* Node features + GNN model => 88% acc.

## Support

**Contact me @:**

e-mail:

* farzanehkoohestani2000@gmail.com

Telegram id:

* [@farzaneh_koohestani](https://t.me/farzaneh_koohestani)

## License
[MIT](https://github.com/farkoo/GNN-Citations/blob/master/LICENSE)
&#0169; 
[Farzaneh Koohestani](https://github.com/farkoo)
