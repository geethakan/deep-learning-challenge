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
 - EIN and Name columns were dropped from the dataframe as they are neither features nor targets.
 - Column "IS_SUCCESSFUL" was identified as the target and remaining columns treated as features.
 - Classification and Application_Type columns are binned to group less dense values together.
 - Categorical data were converted to numerical values using pandas get_dummies function.
 - Data is then split into training and testing datasets with default limits (75:25 for train:test dataset ratio)
 - Training and testing features datasets are then scaled using Python sklearn StandardScalar function to standardize data.

### Compile, Train and Evaluate the Model
 - A Sequential model is created using keras interface and use Tensorflow deep learning network.
 - Started off with 10 neurons in the first hidden layer and 8 neurons in the second hidden layer.
 - Model was then compiled and fitted to training dataset.
 - Accuracy was evaluated for test data and found to display a 72% accuracy

### Optimization
Couple of measures were undertaken to improve accuracy of the model.
- Column STATUS although a good feature, was found to be Active for 99.9% of the organizations. Just 5 were not Active.
- STATUS was dropped from feature set.
- Train to test ratio adjusted to 60 to 40 percent.
- Recommended 2-3 times nueron for hidden layer was followed and first hidden layer neuron count increased to 84
- Accuracy was still not improved so after a couple variations, count was set to 70 for first layer, 50 for second layer and 30 for a third layer.
- Epoch count and batch size were increased.
- Target accuracy of 75% was not attained even after several tries and finally a 73% accuracy improvement was achieved.
- Model was saved HDF5 file.

### Summary
Although stratify was specified, test accuracy is a little lower than training accuracy indicating some variance in the dataset. Range of numbers for income amount with hyphen might be one of the reason. Will be better to have the lower and upper values as numeric in separate columns. Keras tuner and more trials with other activations and nueron counts would be required to improve accuracy of prediction.

![image](https://user-images.githubusercontent.com/113957254/229262684-e97204ff-fcb5-4de5-bbe1-95746c5b6038.png)

