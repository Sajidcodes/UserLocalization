### User Localization with Self-Supervised Learning
User localization is a critical feature in wireless communication systems, facilitating applications such as navigation, smart factories, surveillance, and IoT. This project explores the potential of self-supervised learning for user localization based on Channel State Information (CSI). The goal is to design a model that can determine user positions using estimated channel frequency responses.

# Overview
Problem Statement
Traditional machine learning methods for user localization require large amounts of labeled data, making them impractical for scenarios with changing radio environments. Self-supervised learning aims to overcome this limitation by reducing the need for labeled data.

![image](https://github.com/Sajidcodes/UserLocalization/assets/101083684/d4124613-12ec-4e9f-86c3-cd4c5403c69d)

# Dataset
The dataset was obtained using a massive MIMO channel sounder [1]. It includes labeled and unlabeled samples:

# Labelled Data (4096 samples):

H_Re: Real part of estimated channel matrices
H_Im: Imaginary part of estimated channel matrices
SNR: Signal-to-noise ratio measured at each antenna
Pos: Ground truth positions of the transmitter

# Unlabelled Data (36192 samples):

Same variables as labelled data, excluding "Pos"
Test Data (883 samples):

Same variables as unlabelled data
## Approach
# Self-Supervised Learning

Design a model to learn from the large unlabelled dataset.
Create a custom task/objective function/target for training.
# Supervised Learning

Use learned information from unlabelled data to build a supervised learning model.
Train on the small labelled dataset with ground truth positions.

# Prediction
Run the trained model on the test data to predict user positions.


# Requirements
Python
Jupyter Notebook
Required libraries (specified in the notebook)

# Evaluation
The final score is based on Mean Absolute Error (MAE) averaged over all three axes and all samples in the test dataset.

# References
[1] Maximilian Arnold, Jakob Hoydis, and Stephan ten Brink, “Novel Massive MIMO Channel Sounding Data applied to Deep Learning-based Indoor Positioning”, Proc. SCC, 2019.





