# Neural Network Charity Analysis

## Overview

In this analyis I started with a dataset containing over 34,000 charitable organizations that received funding from Alphabet Soup. My goal was to create a deep learning algorithm that predicts whether or not an organization will be succesful if they were to receive funding from Alphabet Soup. Before running the model, I went through a thorough preprocessing of the data, which included dropping certain columns, binning certain columns, and encoding columns with the "object" datatype to dummy variables. I ran my jupyter notebook many times, tinkering with how I preprocessed the data as well as the model itself (number of neurons, hidden layers, epochs) in order to produce as high a predictive accuracy score as possible. 

## Results

### Data Preprocessing
![X_y_split](https://user-images.githubusercontent.com/95651156/168145113-0966393e-162b-44cc-9ad9-fee073559412.png)

#### Target
* I established the "IS_SUCCESSFUL" column as the target variable for the model
 * * This column took values of 1 and 0, with 1 signifying that the funding was succesful and 0 signaling that it was unsuccesful

#### Features Included
  * application type
  * affiliated sector or industry
  * government organization classification
  * use of funding
  * organization type
  * status (active or inactive)
  * income classification
  * special considerations received (yes or no)
  * requested funding amount

#### Features Dropped from DataFrame
The following features were dropped from every version of the model:

* EIN Code
* Organization Name

Additionally, in some versions of the model I decided to drop the "special considerations" column because a vast majority (over 99%) of orgs did not receive special considerations

### Compiling, Training, and Evaluating the Model

#### Increasing Model Performance
To try and increase  model performance, I did all of the following:

* Add/remove neurons from each hidden layer
* Add/remove hidden layers 
* Increase/decrease number of epochs
* Add/remove columns to model features (specifically, I tried the model with and without "special considerations"
* Change how I binned certain columns
* Change hidden and output layer activation functions



#### Model Selection
Despite tinkering with the model for several hours (I would estimate I changed the model 20 times) I wasn't able to surpass my goal of producing a predictive accuracy score of 0.75. The top accuracy score I was able to produce was 0.7399.

This top performance was achieved by removing the "special considerations" column, using 50 epochs, and using the model setup displayed in the following image:

![Screen Shot 2022-05-12 at 12 13 56 PM](https://user-images.githubusercontent.com/95651156/168151233-8b069ec3-9eef-4547-b2ac-d0f3dee0ec1c.png)

* number of hidden layers: 2
* hidden layer 1 activation function: relu
* hidden layer 2 activation function: relu
* output layer activation function: sigmoid 
* hidden layer 1 number of nodes: 20
* hidden layer 2 number of nodes: 10

The loss and accuracy score metrics of this model are displayed in the following image:

![NN_results](https://user-images.githubusercontent.com/95651156/168151757-8546709c-b80d-4b40-b5cb-1d3a15110a99.png)

## Summary

In the end I was unable to reach a predictive accuracy score of 75%. However, by tinkering with how I preprocessed the data as well as adjusting the how I compiled the model, I was able to come somewhat close to this threshold (nearly 74%). 

One possible alternative to this deep learning model would be a supervised machine learning model that uses the random forest algorithm. I would suggest trying the RF classifier because it has a strong chance of producing similar (and possibly better) accuracy scores while having a far lower runtime than the deep learning model. 
