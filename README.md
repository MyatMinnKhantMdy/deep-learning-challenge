# Alphabet Soup Charity: Deep Learning Challenge

##  Overview

Alphabet Soup is a nonprofit foundation that funds various charitable ventures. To improve its decision-making, the organization provided historical data and requested a predictive model to identify applicants most likely to succeed if funded.

This project uses deep learning to build a binary classification model that predicts the success of future applicants based on their application details.

---

##  Technologies Used

- Python
- Pandas
- TensorFlow / Keras
- Scikit-learn
- Google Colab
- Jupyter Notebooks
- Matplotlib (for optional visualizations)

---

##  Project Files

- `AlphabetSoupCharity.ipynb`: Initial notebook for data preprocessing and base model creation.
- `AlphabetSoupCharity_Optimization.ipynb`: Optimization notebook with improved architecture and performance tuning.
- `AlphabetSoupCharity.h5`: Saved model from the base network.
- `AlphabetSoupCharity_Optimization.h5`: Saved model from the optimized network.
- `README.md`: Project summary and setup instructions.
- `report.md`: Full analysis and results summary.
- 'charity_data.csv' : Resource

---

##  Key Steps

### 1. Data Preprocessing
- Dropped ID columns (`EIN`, `NAME`)
- One-hot encoded categorical variables
- Scaled numerical features using `StandardScaler()`
- Split the data into training and test sets

### 2. Model Development
- Created an initial neural network with:
  - 2 hidden layers (80 & 30 neurons, ReLU activation)
  - 1 output layer (Sigmoid activation)
  - Achieved ~72% accuracy

### 3. Optimization
- Increased complexity with 3 hidden layers (100, 30, 10 neurons)
- Added Dropout layer (0.2) to reduce overfitting
- Trained model for 100 epochs
- Final model reached target accuracy of **~75%**

---

##  Results Summary

| Model Version | Accuracy | Notes |
|---------------|----------|-------|
| Initial Model | ~72%     | 2 hidden layers, basic tuning |
| Optimized Model | ~75%+  | More layers, neurons, dropout, and longer training |

---

##  Future Improvements

- Try using a tree-based model like **Random Forest** for comparison
- Perform feature importance analysis
- Tune learning rates and optimizers further
- Integrate cross-validation for better evaluation
