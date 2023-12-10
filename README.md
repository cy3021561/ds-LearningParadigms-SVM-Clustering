# Supervised, Semi-Supervised, and Unsupervised Learning Project

## Overview

This project explores different machine learning paradigms including supervised, semi-supervised, and unsupervised learning using the Breast Cancer Wisconsin (Diagnostic) and Banknote Authentication datasets. It involves implementing SVMs, k-means, spectral clustering, and active learning techniques.

## Part 1: Learning Methods on Breast Cancer Wisconsin (Diagnostic) Data

### (a) Dataset Preparation

- Download the dataset from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29).
- The dataset includes IDs, classes (Benign=B, Malignant=M), and 30 attributes.

### (b) Monte-Carlo Simulation

- Perform supervised, unsupervised, and semi-supervised learning 30 times with a randomly selected train and test data (20% of both positive and negative classes as the test set).
- Compare the average scores (accuracy, precision, recall, F1-score, and AUC) for each algorithm.

#### (i) Supervised Learning with L1-penalized SVM

- Train an L1-penalized SVM using 5-fold cross-validation.
- Report average metrics and plot the ROC. Include a confusion matrix for one of the runs.

#### (ii) Semi-Supervised Learning/Self-training

- Implement a self-training algorithm using L1-penalized SVM.
- Continuously label and add the farthest unlabeled data point to the labeled set.
- Evaluate the final model on test data.

#### (iii) Unsupervised Learning with k-means

- Apply k-means clustering with k=2 on the whole training set.
- Assign labels based on the majority poll within the closest data points to cluster centers.
- Classify test data based on proximity to cluster centers and report performance metrics.

#### (iv) Spectral Clustering

- Implement spectral clustering with an RBF kernel.
- Do not label data based on proximity to cluster centers but use the fit-predict method.

#### (v) Method Comparison

- Compare the results obtained from supervised, semi-supervised, and unsupervised learning methods.

## Part 2: Active Learning Using Support Vector Machines

### (a) Dataset Preparation

- Download the Banknote Authentication dataset from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/banknote+authentication).
- Split the dataset into 472 test data points and 900 training data points.

### (b) Active vs Passive Learning

- Implement both active and passive learning using SVMs.
- Train SVMs progressively by adding 10 data points at a time from the training set.

#### (i) Passive Learning

- Implement passive learning by randomly selecting new data points to add to the training pool.

#### (ii) Active Learning

- Implement active learning by selecting data points closest to the hyperplane of the SVM.

### (c) Monte Carlo Simulation and Learning Curve

- Perform a Monte Carlo simulation by averaging the test errors of 90 incrementally trained SVMs in both active and passive learning.
- Plot the average test error against the number of training instances for both learning methods.

## Objectives

- To explore and compare different learning paradigms using SVMs and clustering methods.
- To understand the impact of active and passive learning in the context of SVMs.
- To evaluate the performance of each learning method using various metrics and learning curves.
