## Background
This dataset is designed for beginners to practice clustering with a simple quadrant blob pattern.

## Problem Description
The task is to build a model for unsupervised clustering using two input features to predict the target cluster_label.

## About the Dataset

### Data Collection
The data is designed for beginner practice with a simple shape pattern that is easy to learn.

### Column Description
<table>
  <tr>
    <td><b>Column Name</b></td>
    <td><b>Type</b></td>
    <td><b>Description</b></td>
  </tr>
  <tr>
    <td>X1</td>
    <td>Float</td>
    <td>First feature dimension</td>
  </tr>
  <tr>
    <td>X2</td>
    <td>Float</td>
    <td>Second feature dimension</td>
  </tr>
</table>

### Dataset Information
+ Training rows: 160
+ Number of features: 2
+ Target: cluster_label (unsupervised clustering)

## Adjusted Rand Index
Adjusted Rand Index (ARI) measures how similar two data clusterings — the participant's prediction and the ground truth — are, regardless of the differences in cluster label names. The ARI is corrected for the expected value under random conditions, so that random clusterings will result in a score close to 0.

### Formula
$$ARI = \frac{RI - \mathbb{E}[RI]}{\max(RI) - \mathbb{E}[RI]}$$

Where:
+ $RI$ = Rand Index, the proportion of data pairs that are consistently classified between the prediction and the ground truth
+ $\mathbb{E}[RI]$ = the expected Rand Index under random conditions
+ $\max(RI)$ = the maximum Rand Index value that can be achieved

### Rand Index

The Rand Index is calculated based on data pairs:

$$RI = \frac{TP+TN}{TP+TN+FP+FN}$$

Where:

+ $TP$ = pairs of data that are in the same cluster in both the prediction and the ground truth
+ $TN$ = pairs of data that are in different clusters in both the prediction and the ground truth
+ $FP$ = pairs of data that are grouped together in the prediction, but are different in the ground truth
+ $FN$ = pairs of data that are grouped differently in the prediction, but are the same in the ground truth
