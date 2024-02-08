# project4-group4
This is our U of T Bootcamp Project 4 - Group 4

# Required Modules
* In order to run the script, please ensure below tools are installed in your local machine:
* AWS CLI (download link: https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
* AWS CLI needs to be configured with Access key ID and Access Keys

* `sqlalchemy_utils` and `psycopg2`

# Summary of EDA
* In this project, we used a clothes price dataset from Kaggle (Resource: https://www.kaggle.com/datasets/mrsimple07/clothes-price-prediction/data
), and we also use hundreds of online images for model training.

# How the Project Works
Step1. user give us a picture. </br>
Step2. we use CNN model to predict what it is (e.g. what category/what colour...) </br>
Step3. we use the prediction result, as a test data and use NN model to predict how much price this item should be. </br>
Step4. show the predict price to user.</br>

![Project%20Scope.png](Project%20Scope.png)

# Who and Why
This project is design for data analyst, business owner who what to predict the price of their new products or cusumer want to have a budget before they make a purchase.

# Actionable items to improve the model
* Feeding more training data (e.g. loading more raw images to training database, rotating the current images as new training data etc.) can definatly improve the model.
* Cropping key identical images. (For example, cropping the logo as training data instead of the whole shoe with background could reduce the noise. )