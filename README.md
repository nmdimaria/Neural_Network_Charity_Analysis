# Neural_Network_Charity_Analysis

## Overview

The pupose of this analysis was to create a neural network model to map the trustworthyness of various charities to use funding appropriately when given donations. We modified our model to try to perfect our predictions and

## Results

### Data Preprocessing

Target Variable - IS_SUCCESSFUL Yes or No
Used Features - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
Unused Features - EIN, NAME

### Compiling, Training, and Evaluating the Model

#### How many neurons, layers, and activation functions did you select for your neural network model, and why?

I started with 43 neurons because that is the number of features and I was curious if that would be sufficient. Ultimately, I chose 129, 86 and 43 neurons for 3 hidden layers. While testing input functions, I set the first two layers used the Relu function while the last two used sigmoid.

#### Were you able to achieve the target model performance?

My third model did at one point exceed model performance of 75%, but only for certain itterations (see below).

#### What steps did you take to try and increase model performance?

I tried not to change too much between tests to keep track of the effects each optimization had on performance. My first thought was to increace the number of nodes to the more reccomended level of 2x the number of features for the first test. This did not effect performance very much from the first test (where I set the nodes equal to the number of features)

I then tried to clean the data by removing duplicate rows to see if redundant data hampered model performance with the same number of nodes. It reduced the performance.

Finally, I increaced the node count to 3x the number of features and stair-stepped down to 43 (the number of features) while using the original dataframe. Performance did not improve much. However, I noticed that after 86 epochs the model had an accuracy over 75%. I tried to see if recreating the model at 86 epochs would achieve a higher accuracy. The highest I achieved was 73%

## Summary

While I was able to increase model performance somewhat tinkering with the nodes and functions, it was tough to beat the accuracy of the original model. The biggest difference seemed to come from changing the data itself, but I was only able to hurt the model's performance. Perhaps some variables (like SPECIAL_CONSIDERATIONS) are largely irrelevant and could be eliminated from the dataset and would increace accuracy. Further analysis would be required.

