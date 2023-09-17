# Solving the Waiting Time Prediction Problem with Neural Networks

## Introduction
In our quest to predict waiting times accurately, we encountered challenges with traditional regression models like Linear and Polynomial Regression, as well as tree-based algorithms like Random Forest and Decision Trees. The primary issue stemmed from the data's heavy bias toward one station, making it difficult for these models to provide satisfactory results. Moreover, predicting a numerical value in such a biased dataset is inherently challenging. To overcome these obstacles, we decided to leverage the power of neural networks.

## Data Preprocessing
Before delving into the neural network architecture, we first addressed outliers that were negatively impacting our model's performance. Outliers can skew predictions and hinder the network's ability to learn meaningful patterns. By removing these outliers, we prepared a cleaner dataset for training.

## Classifying Waiting Times
To make the problem more amenable to neural network modeling, we opted to transform the continuous waiting time values into discrete classes. This classification approach simplifies the problem and allows us to use a neural network for multiclass classification.

We divided waiting times into six classes, as follows:
- Class 0: Waiting time between 0 to 10 minutes.
- Class 1: Waiting time between 10 to 20 minutes.
- (And so on, up to Class 5, which represents waiting times greater than or equal to 50 minutes.)

## Neural Network Architecture
Our neural network architecture consists of several dense layers. These layers are responsible for learning and capturing the intricate patterns in the data. Here's a summary of our neural network:

Layer (type) Output Shape Param #
dense (Dense) (None, 256) 6144
dense_1 (Dense) (None, 128) 32896
dense_2 (Dense) (None, 64) 8256
dense_3 (Dense) (None, 32) 2080
dense_4 (Dense) (None, 16) 528
dense_5 (Dense) (None, 8) 136
dense_6 (Dense) (None, 6) 54
Total params: 50,094
Trainable params: 50,094
Non-trainable params: 0


## Conclusion
Our transition from traditional regression models to a neural network approach, along with preprocessing steps such as outlier removal and classifying waiting times, has shown promising results. Neural networks are well-suited for handling complex, non-linear relationships and biased data. With this architecture, we aim to improve the accuracy of waiting time predictions, providing valuable insights for optimizing resource allocation and enhancing customer satisfaction in the transportation domain.
