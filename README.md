# Social Graph Link Prediction
### Problem statement:

Given a directed social graph, we have to predict missing links to recommend frienns/connections/followers(Link Prediction on graph).

### Data Overview

Dataset from facebook's recruiting challenge on kaggle:
https://www.kaggle.com/c/FacebookRecruiting
Data contains two columns: source and destination edge pairs in the directed graph.

* Data columns(total 2 columns):
* source_node int64
* destination_node int64

### Mapping the problem to supervised learning problem:

* Map this to a binary classification task with 0 implying an absence of an edge and 1 implying the presence as y_i's
* Now, we need to featurize a pair of vertices (ui, uj), such that these features can help us predict the presence/absence of an edge. A simple feature could be number of common-friends to u_i and u_j which is highly indicative of an edge between u_i and u_j.
* Reference papers and link:
  * https://www.cs.cornell.edu/home/kleinber/link-pred.pdf
  * https://www3.nd.edu/~dial/publications/lichtenwalter2010new.pdf
  * https://www.statisticshowto.com/jaccard-index/

* Assignments:
    Add another feature called Preferential Attachment with followers and     followees data of vertex. You can check about Preferential Attachment     in below pdf: http://be.amazd.com/link-prediction/
    
  

### Business objectives and constraints:

* No low_latency requirements
* Predicting the probability of a link is useful so as to recommend the highest probability links to a user
* We got to suggest connections which are most likely to be correct and we should try and not miss out any connections

### Performance metric and supervised learning:

1. Both precision and recall are important, hence F1 score is good choice
2. Confusion matrix
3. Accuracy can also be checked

