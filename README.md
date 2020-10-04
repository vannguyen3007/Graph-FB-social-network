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

### Business objectives and constraints:

* No low_latency requirements
* Predicting the probability of a link is useful so as to recommend the highest probability links to a user
* We got to suggest connections which are most likely to be correct and we should try and not miss out any connections

### Performance metric and supervised learning:

1. Both precision and recall are important, hence F1 score is good choice
2. Confusion matrix
3. Accuracy can also be checked

