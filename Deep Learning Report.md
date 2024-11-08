# Neural Network Model Optimization Report

## Overview of the analysis:

This analysis's purpose was to create a tool that can help Alphabet Soup select applicants for funding with the best chance of success in their ventures.

In the initial model, we followed the criteria given in the starter code file, and the model's accuracy was not above 75%. In this optimization, various data attributes and model 
attributes were changed to increase the model's accuracy to above 75%.

## Results:

### Data Processing
1. What variable(s) are the target(s) for your model?
  
  The variable for the target is the IS_SUCCESSFUL data column.

2. What variable(s) are the features for your model?

  The remaining data columns contain the variables for the features: NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.

3. What variable(s) should be removed from the input data because they are neither targets nor features?

  In the original module, the name and EIN were removed, but with that set of data, we could not meet our accuracy goal.For the optimization, only the EIN was removed because it is a 
  duplicative identifier to the organization name.

### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?

  For the optimization model, three layers with many neurons were used, and the same activation function was used on all layers. I added the additional layers to increase the learning 
  capacity of the model and, therefore, the accuracy results. In future model testing, we could change the activation(s) to see if the accuracy increases even more.

2. Were you able to achieve the target model performance?

  Yes, by adding the additional layer and including the names, I was able to hit the target model performance.

3. What steps did you take in your attempts to increase model performance?

  To increase model performance, I first changed the number of nodes and layers to see if our assurance score improved. When those changes made little impact, I went back to the
  original data and determined that the EIN or Names needed to be included in the overall data. From there, I added the names and followed bin allocation in a manner similar to the 
  application type and classification.

### Summary

The overall results of the deep learning model suggests that using TensorFlow can give us results that would meet our goal of 75% accuracy, but we would need to 
determine if that level is high enough for us to trust the results.

Upon trying two different models, I was able to meet the 75% accuracy goal, so we could potentially use another model and get similar results, but both of the 
alternatice models yieled lower accuracy scores than the TensorFlow model.

Based on the TensorFlow model, we can detrmine that NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, 
and ASK_AMT have a high impact on outcomes. With the name data having the most impact, since it adding this varialble back into our test data increased our accuracy results.  