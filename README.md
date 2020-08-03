# SIIM-ISIC Melanoma Classification

Early detection of skin cancer makes the treatment procedure much more effective and therefore increases the chance of survival for the patience. The dataset is provided by Kaggle and includes images of tumors in early stage with labels of "benign" or "malignant". The information of the patient for each image (sex, age and the location of the tumor) is also provided as a separate .csv file.  

The repository contains 3 jupyter notebooks as follow:

## 1) SIIM_Img.ipynb
In this notebook only the images without patient information are used for training the model. The labels are extracted from .csv files and attached to the images. Dataset is divided to train and validation sets and then fed to a convolutional neural network defined using TensorFlow and Keras API.   


## 2) SIIM_Tabular.ipynb
This notebook only considers the information of the patience and based on that predicts the likelihood of a tumor being benign or malignant. First the data is pre-processed and then briefly visualized. In the next step the training and validation sets are fed to a RandomForestClassifier and the model is trained. In the next step, using RandomizedSearchCV the hyperparameters are optimized.

## 3) SIIM.ipynb
This notebook combines the two types of information namely, images and tabular data. The pre-defined EfficientNet model is used for the images and a separate branch is defined for the tabular data. The result of the two networks are then combined and used for the final prediction. 



