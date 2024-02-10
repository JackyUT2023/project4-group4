# project4-group4
This is our U of T Bootcamp Project 4 - Group 4

# Who and Why
Our tool is designed for general consumers.
When consumers walking on the street and saw someone with good fashion and they want to figure out what it is and how much would be the value.

# How the Project Works
Step1. user give us a picture. </br>
Step2. we use CNN model to predict what it is (e.g. what category/what colour...) </br>
Step3. we use the prediction result, as a test data and use NN model to predict how much price this item should be. </br>
Step4. show the predict price to user.</br>

![Project%20Scope.png](Project%20Scope.png)

# Required Modules
* In order to run the script, please ensure below tools are installed in your local machine:
* AWS CLI (download link: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
* AWS CLI needs to be configured with Access key ID and Access Keys
* `sqlalchemy_utils` and `psycopg2`
* `TensorFlow`,`TorchVision`,`PyTorch`
* `MNIST` database

# Summary of EDA
* In this project, we used a clothes price dataset from Kaggle (Resource: https://www.kaggle.com/datasets/mrsimple07/clothes-price-prediction/data
), and we also use hundreds of online images for model training.

# Limitation
* For CNN model:</br>
- Premade MNIST training data - i.e.) 2 shoes in an image or images not in the right configuration</br>
- Not optimized: run-time 2-3 min/epoch - Upsizing 28x28 to 224x224, increasing runtime 100x</br>
- Low epochs = unable to train all data properly</br>
- Fixed labels MNIST training dataset</br>
* In attempting to create a machine learning model to predict prices, it was observed that there was no correlation between the price and other features in the dataset.

# Actionable items to improve the model
* Feeding more training data (e.g. loading more raw images to training database, rotating the current images as new training data etc.) can definatly improve the model.
* Cropping key identical images. (For example, cropping the logo as training data instead of the whole shoe with background could reduce the noise. )