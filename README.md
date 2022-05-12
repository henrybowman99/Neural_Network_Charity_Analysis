# Neural Network Charity Analysis

## Overview

In this analyis I started with a dataset containing over 34,000 charitable organizations that received funding from Alphabet Soup. My goal was to create a neural network algorithm that predicts whether or not an organization will be succesful if they were to receive funding from Alphabet Soup. T Before running the model, I went through a thorough preprocessing of the data, which included dropping certain columns, binning certain columns, and encoding columns with the "object" datatype to dummy variables. I ran my jupyter notebook many times, tinkering with how I preprocessed the data as well as the model itself (number of neurons, hidden layers, epochs) in order to produce as high a predictive accuracy score as possible. 

## Results

### Data Preprocessing
![X_y_split](https://user-images.githubusercontent.com/95651156/168145113-0966393e-162b-44cc-9ad9-fee073559412.png)

#### Target
* I established the "IS_SUCCESSFUL column as the target variable for the model
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

Additionally, in some versions of the model I decided to drop the "special considerations" column because
Despite tinkering with the model for several hours (I would estimate I changed the model 20 times) I wasn't able to surpass my goal of producing a predictive 
