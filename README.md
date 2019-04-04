## image_classifier_model

# Image Classification with CIFAR-10 dataset
In this notebook, I am going to classify images from the [CIFAR-10 dataset](https://www.cs.toronto.edu/~kriz/cifar.html).  The dataset consists of airplanes, dogs, cats, and other objects. You'll preprocess the images, then train a convolutional neural network on all the samples. 

# Model Architecture
<img src="./image_classifier_model/image/conv_model.png" alt="Drawing"/>

The entire model consists of 14 layers in total. In addition to layers below lists what techniques are applied to build the model.

1. Convolution with 64 different filters in size of (3x3)
2. Max Pooling by 2
  - ReLU activation function
  - Batch Normalization
3. Convolution with 128 different filters in size of (3x3)
4. Max Pooling by 2
  - ReLU activation function
  - Batch Normalization
5. Convolution with 256 different filters in size of (3x3)
6. Max Pooling by 2
  - ReLU activation function
  - Batch Normalization
7. Convolution with 512 different filters in size of (3x3)
8. Max Pooling by 2
  - ReLU activation function
  - Batch Normalization
9. Flattening the 3-D output of the last convolutional operations.
10. Fully Connected Layer with 128 units
  - Dropout
  - Batch Normalization
11. Fully Connected Layer with 256 units
  - Dropout
  - Batch Normalization
12. Fully Connected Layer with 512 units
  - Dropout
  - Batch Normalization
13. Fully Connected Layer with 1024 units
  - Dropout
  - Batch Normalization
14. Fully Connected Layer with 10 units (number of image classes)

the image below decribes how the conceptual convolving operation differs from the tensorflow implementation when you use [Channel x Width x Height] tensor format.

<img src="./image_classifier_model/image/convolving.png" alt="Drawing"/>

# Training the model
achieving over 75% accuracy in 10 epochs through 5 batches.

<img src="./image_classifier_model/image/training.PNG" alt="Drawing"/>

# Prediction
<img src="./image_classifier_model/image/prediction.PNG" alt="Drawing"/>


## flask_image_classifier_api

## Download link of Inception 
[Model_link](https://drive.google.com/file/d/19SA-jqUo7b34gmzy75Sjp22hjEi2mlM7/view?usp=sharing) 

## Steps to run this project 
Step01: Firstly, Download the model and put into ./web folder.


Step02: Install the docker [docker_install](https://docs.docker.com/install/linux/docker-ce/ubuntu/)


Step03: Install MongoDB [Mongo_install](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/) (on Ubuntu)


Step04: Create the virtual environment by command: virtualenv venv (on Ubuntu)


step05: Activate the virtual environment: source bin/activate (For Ubuntu)


step06: Run sudo docker-compose up
