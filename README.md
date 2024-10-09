# Credit Approval Prediction

## Project Description

This project focuses on predicting whether an individual will be approved for a credit line based on key financial indicators such as income, credit limit, and credit rating. The model leverages statistical learning techniques, including Logistic Regression and Ridge Regression, to perform binary classification on the Credit dataset from the ISLR2 package. The primary goal is to accurately assess creditworthiness while managing multicollinearity in the predictors.

## Table of Contents

1. [Project Description](#project-description)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Project Structure](#project-structure)
5. [Technologies Used](#technologies-used)
6. [Modeling Approach](#modeling-approach)
7. [Evaluation and Results](#evaluation-and-results)
8. [Limitations and Improvements](#limitations-and-improvements)
9. [Contact](#contact)

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Chandan-Kondapuram/Credit-Approval-Prediction.git
   ```

2. **Install required dependencies**:
   This project uses R, and the following packages are required:
   ```r
   install.packages(c("ISLR2", "ggplot2", "caret", "glmnet", "corrplot", "pROC"))
   ```

## Usage

1. **Dataset**: The `Credit` dataset from the ISLR2 package is used in this project. The dataset contains personal and financial details that are key to assessing an individual's creditworthiness.
   
2. **Running the model**: 
   - To run the model, execute the R script that includes the Logistic Regression and Ridge Regression implementations.
   - Ensure the dataset is loaded using `data("Credit")` and preprocessed before applying the models.

   Example:
   ```r
   source("Code.Rmd")
   ```

3. **Evaluating predictions**: The script includes code for training the models on the training data and evaluating performance on the test data, along with visualizations for exploratory data analysis (EDA).

## Project Structure

```plaintext
├── data/                         # Contains the dataset used for training and testing
├── Code.Rmd                      # Main R script with model code
├── Final-project.pdf              # Project report explaining methods and results
├── README.md                     # Project documentation
```

## Technologies Used

- **R** for data analysis and model building
- **ggplot2** for visualizations
- **caret** for cross-validation and model tuning
- **glmnet** for Ridge Regression
- **corrplot** for correlation analysis
- **pROC** for ROC curve generation

## Modeling Approach

The project employs two primary models:

1. **Logistic Regression**: Utilizes the best subset of predictors selected through backward stepwise selection based on Bayesian Information Criterion (BIC).
2. **Ridge Regression**: Tackles multicollinearity among predictors by applying regularization. This method shrinks coefficient estimates, reducing variance and improving generalization.

### Feature Selection and Engineering

- **Best Subset Selection**: Applied to choose the most relevant predictors from the dataset using backward selection.
- **Handling Multicollinearity**: Ridge regression was introduced to manage collinearity, particularly between financial variables such as Income, Limit, and Rating.

## Evaluation and Results

1. **Logistic Regression**:
   - Training Accuracy: 86%
   - Test Accuracy: 85%
   - ROC AUC: 0.9519
   - Confusion Matrix: Sensitivity (88.46%), Specificity (78.57%)
   - The model performed well, achieving balanced accuracy and minimal deviation between training and test performance.

2. **Ridge Regression**:
   - Test Accuracy: 88.7%
   - The Ridge Regression model proved advantageous in handling multicollinearity, yielding slightly higher accuracy than logistic regression.

## Limitations and Improvements

### Limitations:
- The CreditApproval binary outcome was created based on median thresholds for financial indicators, which might oversimplify the real-world complexity of credit approval decisions.
- The models assume linear relationships between predictors and the outcome, which may not fully capture non-linear interactions.

### Possible Improvements:
- Adding interaction terms or polynomial features could better capture the complex relationships in the data.
- Trying alternative machine learning algorithms like Random Forests or Support Vector Machines could further enhance prediction accuracy.
- Testing the model on external datasets would improve generalizability.

## Contact

For any questions or contributions, feel free to reach out:
- GitHub: [Chandan-Kondapuram](https://github.com/Chandan-Kondapuram)
- Email: chandan@example.com
