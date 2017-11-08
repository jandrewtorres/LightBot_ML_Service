# LightBot_ML_Service
A machine learning service for the LightBot application.

## Overview
The LightBot machine learning service is a python flask server that takes in LightBot user action histories and returns a predicted user action profile.

## Developer notes

Install anaconda. This includes all python libraries needed (sklearn, python 3.6, numpy, Jupyter Notebook: currently being used. More to be used in future).

Once you have anaconda or the python libraries installed in your environment, run `jupyter notebook` in the LightBot-ML-Service/ folder and you will get a window in your browser that allows you to open the notebook and see the current work.

Currently, there is a shitty Random Forest Regression model, which is totally inappropriate for classification. It was late, I don't know what I was thinking. More appropriate models would be logistic regression and Naive Bayes classification models. This is going to require reconfiguring the data we already have.

## Machine Learning service architecture:
NodeJS server sends user action history in json format to python flask server. Python flask server takes user action history, manipulates data, does machine learning magic, reconfigures data into json and sends the predicted user profile back to the NodeJS server which updates the the new predicted user profile.
