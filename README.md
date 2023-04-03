# Neural_Network_Charity_Analysis

## Overview of the loan prediction risk analysis:

The analysis is used to create a neural network model, a guide to the best investment opportunities. Using a supervised machine learning (neural networks) and Jupyter Notebook, the load data is trained to give the results needed. Then the data is optimized to remove the noisy variables, using more neurons in the hidden layers, adding more hidden layers, and using different activation functions, and lastly using check points to save the progress.

## Results:

### Data Preprocessing

- What variable(s) are considered the target(s) for your model?
    -  Variable `IS_SUCCESSFULL` was used.

- What variable(s) are considered to be the features for your model?
    - `APPLICATION_TYPE` `AFFILIATION` `CLASSIFICATION` `USE_CASE` `ORGANIZATION` `INCOME_AMT` `ASK_AMT` `IS_SUCCESSFUL`

- What variable(s) are neither targets nor features, and should be removed from the input data?
    - Removed in initial model `EIN` `NAME`
    - Removed in optimizations `EIN` `NAME` `STATUS` `SPECIAL_CONSIDERATIONS`

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Initial Model: Neurons 8 and 4, Two hidden layers; Activations used are relu and sigmoid.
    - First attempt at optimizing the model: Neurons 50, 20, and 10, Three hidden layers;  Activations used are `relu` and `sigmoid`.
    - Second attempt at optimizing the model: Neurons 120, 80 and 40, Three hidden layers; Activations used are `relu` and `sigmoid`.
    - Third attempt at optimizing the model: Neurons 10, 3, and 1, Three hidden layers; Activations used are `relu` and `sigmoid`. 

- Were you able to achieve the target model performance? Goal is 75% or greater accuracy.
    - Initial Model: loss is 70.3% and accuracy is 55.3%. Did not achieve desired performance.
    - First attempt at optimizing the model: loss is 67.8% and accuracy is 57.2%. Did not achieve desired performance.
    - Second attempt at optimizing the model: loss is 64.7% and accuracy is 60.2%. Did not achieve desired performance.
    - Third attempt at optimizing the model: loss is 70.1% and accuracy is 53.8%. Did not achieve desired performance.

preview of the Second attempt optimization:
<img src:"https://github.com/mehill37/Neural_Network_Charity_Analysis/blob/edbd7674433ada105c0ef8d430de59281214870c/images/optimization.png">

preview of the Second attempt loss and accuracy scores:
<img src:"https://github.com/mehill37/Neural_Network_Charity_Analysis/blob/edbd7674433ada105c0ef8d430de59281214870c/images/optim_accuracy_2.png">

- What steps did you take to try and increase model performance?
    - increasing the parameters by icreasing the neurons in each hidden layer.
    - Change the output layer activation function

## Summary:

After reviewing all the attempts, I was unable to achieve an Accuracy Score of 75% or higher. I adjusted the neurons each attempt and tried switching the activation function, but the accuracy score only continued to worsen. This model doesn't seem ideal for getting the results we need. The `RandomForestClassifier` could be a better solution. It's more useful when trying to aviod overfitting the model. 
