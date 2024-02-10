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
- Premade MNIST training data - i.e.) 2 shoes in an image or images not in the right configuration</br>
- Not optimized: run-time 2-3 min/epoch - Upsizing 28x28 to 224x224, increasing runtime 100x</br>
- Low epochs = unable to train all data properly</br>
- Fixed labels MNIST training dataset</br>
- In attempting to create a machine learning model to predict prices, it was observed that there was no correlation between the price and other features in the dataset.

# Actionable items to improve the model
* Feeding more training data (e.g. loading more raw images to training database, rotating the current images as new training data etc.) can definatly improve the model.
* Cropping key identical images. (For example, cropping the logo as training data instead of the whole shoe with background could reduce the noise. )

# Convolutional Neural Network
* Colour and Categories </br>
    - Colours used in our fashion dataset (black, blue, green, red, white, yellow) </br>
    - Category (T-shirts, trousers, pullovers, dresses, coats, sandals, shirts, shoes, bag, and ankle boot) </br>


# CNN Colours Analysis
Training the model to learn colours was simpler than categories. The dataset was much smaller with only 168 images with a high accuracy of 80% after 15 epochs.
![colour_accuracy](https://github.com/JackyUT2023/project4-group4/assets/127992819/6956744a-7548-4bb5-955f-069869851271)
The results of the predicted colours are as shown.
![colour_prediction](https://github.com/JackyUT2023/project4-group4/assets/127992819/77839265-1426-4b04-82d4-ebcc7831f1cf)
# CNN Categories Training Model
* We used a precompiled Fashion MNIST image library. This included over 70,000 images with 10 categories.</br>
    - MNIST Dataset</br>
    - 70,000+ black and white images of 28x28 images</br>
    - 3 neurons</br>
    - 10 categories instead of 6</br>
        - Adjustments to labels made</br>

# CNN Categories Analysis
23 minute runtime (2-3 minute/ epoch) </br>
83-84% accuracy</br>
Probabilities change depending on hyperparameters (epochs, neurons)
Small epoch = probabilities more spread

# References
Fashion MNIST dataset: https://www.kaggle.com/datasets/zalando-research/fashionmnist </br>
Clothing dataset: https://www.kaggle.com/datasets/mrsimple07/clothes-price-prediction/data </br>
PyTorch Color Classifier: https://www.kaggle.com/code/kimduhan/cnn-fashion-color-classifier-with-pytorch </br>