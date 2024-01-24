# Animal Image Classification With Transfer Learning and Deployment into TFLite
A project for my submission of my learning in IDCamp 2023 about machine learning to make an animal images classification. This project is about classifying animal images using transfer learning with MobileNetV2 and then convert the trained model into TFLite. The model created by using Python with TensorFlow and Keras. I use Google Colab notebook to run my code, so I recommend to use Google Colab if you want to try my code. The dataset that I used for this project is [this dataset](https://www.kaggle.com/datasets/alessiocorrado99/animals10) from Kaggle.

# Requirements

Library that I used for this project are below.
* Library for data preprocessing
  * os
  * zipfile
  * cv2
  * shutil
  * google.colab and files
  *  PIL and Image

* Library for machine learning modelling
  * tensorflow
  * ImageDataGenerator
  * matplotlib
  * pathlib

# Project Structure

There are several steps in this project as stated below:
* Library Preparation
  
  In this step, we will prepare the necessary libraries and packages.
* Dataset Preparation
  
  In this step, we will download the dataset and read the dataset. We check the resolution of the images and print some examples of the images

  ![Image Examples.](https://github.com/harisyf/image-classification-with-transfer-learning-deployment/blob/main/images/images-example.png)
* Data Preprocessing
  
  After we extract the dataset, next we will do data preprocessing such as resize our images to the same resolution (224x224), image augmentation (rescale, shear range, zoom range, and flipping horizontally), and training and validation data split into 80:20.

* Machine Learning Modelling
  
  After data preprocessing, next up modelling our machine learning model. We are going to use MobileNetV2 as our transfer learning model as the base model then we are going to add another layers later.

* Base Model
  
  The base model is quite long, you can check all the layers in my notebook. You can see the snippet below.
  ![Base Model Summary.](https://github.com/harisyf/image-classification-with-transfer-learning-deployment/blob/main/images/base-model.png)

* Modelling
  
  After we load our base model, we are going to add new layers then we compile the model.

  ![Model Summary.](https://github.com/harisyf/image-classification-with-transfer-learning-deployment/blob/main/images/model.png)

* Train The Model
  
  Let's train our model!

  ![Model Training.](https://github.com/harisyf/image-classification-with-transfer-learning-deployment/blob/main/images/model-training.png)

* Model Evaluation

  Model evaluation from the results of the training process is shown by creating accuracy plots and loss plots for training and validation.
  
  ![Model Evaluation.](https://github.com/harisyf/image-classification-with-transfer-learning-deployment/blob/main/images/evaluation.png)
  
* Saved Model to TFLite Format

  Then after we train our model, let's save it and convert the saved model into TFLite format.
  
You may check my notebook for the detail of every steps.

# Conclusion
We successfully implement transfer learning with MobileNetV2 into animal image classification dataset. We achieved 95% accuracy. We also successfuly convert our saved model into TFLite. Thank you for visiting my page if you have any further discussion or suggestion you may contact me! (A star would be very appreciated!)

