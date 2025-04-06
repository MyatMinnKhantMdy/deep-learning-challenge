


# Alphabet Soup Charity Deep Learning Report

## Overview of the Analysis

Alphabet Soup is a nonprofit organization that funds charitable ventures. To improve its funding decisions, Alphabet Soup provided a dataset of previously funded organizations and asked for a machine learning model to predict which applicants are most likely to succeed if funded.

This analysis uses deep learning to build a binary classifier that predicts the success of applicants based on features such as application type, use case, income, and funding amount requested.

---

## Results

### Data Preprocessing

- **Target Variables:**
  - **IS_SUCCESSFUL**: This binary variable (0 = not successful, 1 = successful) is the prediction target.

- **Feature Variable(s):**
  - All other columns except **EIN**, **NAME**, and **IS_SUCCESSFUL**, such as:
    - APPLICATION_TYPE
    - AFFILIATION
    - CLASSIFICATION
    - USE_CASE
    - ORGANIZATION
    - STATUS
    - INCOME_AMT
    - SPECIAL_CONSIDERATIONS
    - ASK_AMT

 **Variables Removed:**
  - **EIN** and **NAME** — these are identification columns that do not contribute to the predictive power of the model and were removed early in the preprocessing step.

---

### Compiling, Training, and Evaluating the Model

**Initial Model Setup:**
   **Neurons and Layers:**
    - 1st hidden layer: 80 neurons, ReLU activation
    - 2nd hidden layer: 30 neurons, ReLU activation
    - Output layer: 1 neuron, Sigmoid activation
  
  **Why these were chosen:**
    - ReLU is commonly used in hidden layers due to performance benefits.
    - Sigmoid is ideal for binary classification in the output layer.
  
   **Performance:**
    - Accuracy of the model was around 72%.

 **Model Optimization Adjustments:**
   
   **Changes made:**
		    - Increased complexity:
		    - 1st hidden layer: 100 neurons (ReLU)
		    - 2nd hidden layer: 30 neurons (Sigmoid)
		    - 3rd hidden layer: 10 neurons (Sigmoid)
			- Added a dropout layer of 20% to reduce overfitting.
			- Increased epochs to 100 and used model checkpoint to store the best model.
   
   **Performance:**
		    - After optimization, model accuracy improved and reached 75% plus.

 **Steps Taken to Increase Model Performance:**
  - Added additional hidden layers and increased the number of neurons.
  - Used dropout() to prevent overfitting.
  - Increased the number of epochs for better training.
  - Applied one-hot encoding and binned rare categorical values into an 'Other' category.
  - Scaled the features using StandardScaler().

---

## Summary of Overall Results

The final deep learning model was able to meet the 75% accuracy goal after optimization. This demonstrates the potential of neural networks in predicting funding success when appropriately tuned and trained. However, there is still room for improvement by exploring other model architectures or data preprocessing techniques.

---

## Alternative Model

To solve this classification problem differently, I used a **Random Forest Classifier**:

 **Why?**
  - This model is highly effective on tabular data.
  - It provides feature importance scores, making interpretation easier.
  - It tends to perform better with less preprocessing and handles categorical data effectively.

Using a tree-based model might offer higher accuracy and a better explanation, which is important for funding decision-making in nonprofit organizations.


