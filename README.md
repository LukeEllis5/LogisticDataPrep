## Project Overview

The goal of this project is to build a logistic regression model that predicts the probability of an account closing.

## Data
The data used in this project consists of:
-	Original account data
-	Original application data


### Data Loading
-	The data is loaded from an Excel file in a folder location

### Data Preprocessing 
-	Null values were identified
-	Null values for one column were filled using the original application data
-	The remaining values are handled by being filled in with a SimpleImputer

### Data Merging
  - The original application files are combined, and a prefix is added to user IDs.
  - The combined data is merged with the main account data.

### Feature Engineering
  - A new binary target variable (`closed`) is created, indicating whether the loan account has been closed based on a timestamp in the `closed_date` column.

### Feature Selection*
  - Irrelevant columns are dropped before training the model.

## Model Training

- The cleaned and processed data is split into training and test sets.
- A logistic regression model is initialized and trained using the training data.

## Model Evaluation

- The model's performance is evaluated using accuracy, confusion matrix, and classification report metrics.
- The overall probability of account closure is calculated for the test set.

## Results

- **Accuracy**: The accuracy of the model is printed.
- **Confusion Matrix**: The confusion matrix of the model's predictions is displayed.
- **Classification Report**: A detailed classification report including precision, recall, and F1-score is provided.
- **Overall Probability of Closure**: The mean probability of closure for the test set is calculated and printed.
