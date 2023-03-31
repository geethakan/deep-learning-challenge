# Prediction of Charity Funding by Organizations - Deep Learning with Neural Network

### Overview
TensorFlow is a Python-friendly open source library for numerical computation that makes machine learning and developing neural networks faster and easier.
This challenge uses Google's machine learning framework, TensorFlow to design a neural network (a deep learning model), to create a binary classification model 
to predict if an Alphabet Soup-funded organization will be successful based on their features.

### Dataset
A csv file with metadata of more than 34K organizations is the dataset being used. Following are the elements of the dataset:
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

### Preprocess
 - EIN and Name columns were dropped from the dataframe
 - Column "IS_SUCCESSFUL" was identified as the target and remaining columns treated as features.
 - 
