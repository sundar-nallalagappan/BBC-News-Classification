# BBC-News-Classification
BBC News Classification using Bidirectional LSTM

Text documents are one of the richest sources of data for businesses.

We’ll use a public dataset from the BBC comprised of 2225 articles, each labeled under one of 5 categories: business, entertainment, politics, sport or tech.

The dataset is broken into 1490 records for training and 735 for testing. The goal will be to build a system that can accurately classify previously unseen news articles into the right category.

The competition is evaluated using Accuracy as a metric.

Following blog has good information on how to look at the problem. https://cloud.google.com/blog/products/gcp/problem-solving-with-ml-automatic-document-classification

kaggle.com/competitions/learn-ai-bbc/overview

Important learning:

1) RNN: Not performing well
Seq length = 550 == Accuracy : 20%
Seq Length = 200 == Accuracy : 25%
Seq length = 150 == Accuracy : 35%

Seq length plays a major role in accuracy and accuracy improved in LSTM models as well as seq length was reduced

2) LSTM: Accuracy was 86% with seq length 150

3) Bidirectional LSTM: Accuracy was 95% with seq length 150

4) Both Sprase categorical cross entropy and categorical cross entropy gave the same results. Both the functionalites of the loss's are same and the change is the way Y is represented. SPCCE - integer (label encoding) but CCCE is one hot encoding
