# Mushroom Classification

## Table of Contents

-->[Introduction](#introduction)
-->[Installation](#installation)
-->[Data](#data)
-->[Preprocessing](#preprocessing)
-->[Models](#models)
-->[Evaluation](#evaluation)
-->[Usage](#usage)
-->[Deployment](#deployment)

## Introduction

The Mushroom Classification App allows users to classify mushrooms into 
edible or poisonous based on their attributes. It utilizes machine learning
models trained on mushroom data to make accurate predictions. By providing
features such as cap shape, cap color, gill size, stalk surface, and other
relevant parameters, the app aims to classify mushrooms as edible or poisonous.

## Installation
```
conda create -p venv python==3.8
```
```
conda activate venv/
```
```
pip install -r requirements.txt
```
```
python setup.py install
```

## Data

The dataset used for training and evaluation is stored in database. 
Read the data from the database and stored in the `artifacts` 
directory. It consists of a CSV file named `raw.csv` containing 
the mushroom attributes and their corresponding classes. the data stored in 
mangodb.

## Preprocessing

Before training the model, it's essential to preprocess the data to ensure 
the suitability for machine learning. Convert categorical variables into 
numerical representations using encoding techniques such as Ordinal encoding.

To perform these preprocessing steps, refer to the `src/components/data_preprocessing.py` script in the repository. This script contains the necessary functions and code snippets to preprocess the raw data. Modify the script as per your requirements and execute it before training the model.

## Models

The ML model is built using scikit-learn library and stored in the `artifacts` directory. The project utilizes the following machine learning models for mushroom classification:

-->Decision Tree Classifier
-->Logistic Regression Classifier
-->KNeighborsClassifier
-->RandomForestClassifier
-->GradientBoostingClassifier

These models can be found in the `model_trainer.py` script in the repository. The trained best model is saved in `best_model.pkl`.

## Evaluation

To evaluate the model's performance, metrics such as accuracy, precision, 
recall, and F1 score was used in the model trainer. Final results are stored in logger folder

## Usage

1. Make sure you have the required dependencies installed by following the instructions in the [Installation](#installation) section.
2. Run the `application.py` file.
3. Open your web browser and navigate to the following address:
```commandline
http://127.0.0.1:5000/
```
This will launch the Mushroom Classification App interface where you can interact with the system.
To classify mushrooms, enter the attributes in the provided input fields and click on the "Predict" button.

## Deployment

The project can be deployed using various platforms such as AWS Elastic Beanstalk deployment service. Follow the deployment instructions provided by the chosen platform to deploy the Mushroom Classification Application.
