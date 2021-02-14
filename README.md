# Neural_Network_Charity_Analysis
 
 
## Overview of the analysis
In this project we attempted to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup's Business team. Using The Tensorflow Library and the Keras Model we built a Neural network and attempted to train the network with the given metadata. The goal is to have this model be able to accurately predict the success of an application
 
 
## Results
 
### Data Preprocessing
- Target variable
   * In this case our target variable was the IS_SUCCESSFUL column because we would like to predict successful applications
   ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/splitting_data.png?raw=True)
 
- Feature variables
   * All columns after this except for the NAME and EIN columns are considered valid features
 
- neither targets nor features and should be removed
   * EIN
   * NAMES
   * STATUS
       ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/dropping_cols.png?raw=True)
 
 
### Compiling, Training, and Evaluating the model
- How Many neurons, layers, and activation functions did you select for your neural network model and why
   * 4 hidden layers in an attempt to improve accuracy
   * 8 neurons in the first hidden layer, 3 in the second to keep the 1 - 3 ratio recommended for neurons per layer in machine learning
   * activation function for all layers except for output layer set to relu as it was yielding the most accurate results. Last layer was set to sigmoid activation for its ability to classify the binary output
   ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/model_summary.png?raw=True)
 
- Were you able to achieve the target model performance?
   * I was unable to increase the accuracy above 75 percent
   ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/model_perf.png?raw=True)
   * Accuracy visualization
   ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/accuracy_vis.png?raw=True)
   * Loss visualization
   ![alt-text](https://github.com/sebcampos/Neural_Network_Charity_Analysis/blob/master/images/loss_vis.png?raw=True)
- What steps did you take to try and increase model performance
   * attempted to change accuracy using the different activation functions
   * attempted to change accuracy by using the different optimizers available
   * dropped different columns that were arguably unnecessary, these were the NAME, EIN, and STATUS columns
   * binned the ASK_AMT column.
 
## Summary
 
It is my understanding that the data for a neural network is not sufficient. Perhaps with more data we could create more accurate predictions. On the other hand, maybe a different model would be better suited to this dataset. Perhaps the SVM model would be more appropriate if our data is not sufficient

