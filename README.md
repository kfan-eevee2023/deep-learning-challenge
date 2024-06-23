#21 Alphabet Soup Charity -- Neural Networks and Deep Learning
Completed By: Kefan Liao

1. Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. In this project we will develop a binary classifier that predicts the likelihood of applicants achieving success if they receive funding from Alphabet Soup. The objective is to optimize the model to achieve an accuracy score above 75%.


2. Preprocess the Data
2.1 Feature Selection --Dropped irrelevant columns such as `EIN` and `names`.
2.2 Binning/Bucketing --Applied to rare occurrences in the `APPLICATION_TYPE` and `CLASSIFICATION` columns.
2.3 Encoding --Transformed categorical data into numeric data using one-hot encoding.
2.4 Splitting Data -- Divided data into training and testing sets.
2.5 Scaling -- Ensured uniform data distribution through scaling.

3. Model Training and Evaluation
3.1 Initial Model
--Architecture: Three layers - input layer (80 neurons), hidden layer (30 neurons), output layer (1 neuron).
--Activation Functions: 'relu' for input and hidden layers, 'sigmoid' for output layer.
--raining: 100 epochs, achieving 74.04% accuracy on training data and 72.99% on test data.
3.2 Optimized Model
--Changes: Added 2 dropout layers and used `tanh` activation functions.
--Results: 74.08% accuracy on training data and 73.09% on test data.

4 Files
AlphabetSoupCharity.ipynb       --Python code for Initial Model
results\AlphabetSoupCharity.h5  --HDF5 result file from Initial Model
AlphabetSoupCharity_Optimization.ipynb        --Python code for Optimized Model
results\AlphabetSoupCharity_Optimization.h5   --HDF5 result file from Optimized Model

5. Summary
The target accuracy of 75% was not achieved despite several optimization attempts. So the current models are not recommended for deployment. Further work is needed to explore alternative models like Random Forest Classifier and make adjustments to preprocessing and model optimization.
