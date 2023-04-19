# Loan classification with Python

This dataset is downloaded from Kaggle and belongs to a Hackathon organized by "Univ.AI". An organization wants to predict who possible defaulters are for the consumer loans product. They have data about historic customer behavior based on what they have observed. Hence when they acquire new customers they want to predict who is riskier and who is not. The task is to predict possible defaulters for the consumer loans product based on the customer historic behavior with possible defaulters with Risk_Flag == 1 and 0 for not possible for being a defaulter.

## Data Exploration
The dataset contains categorical data which was converted to numerical using LabelEncoder. The relationships between all the features and the target were plotted using a heatmap 
![image](https://user-images.githubusercontent.com/85885666/233009809-8488ee00-ccf0-48f3-a5b9-dec42ef4f5e3.png)
As all the features does not have a strong correlation to the target, all of the features were used in the machine learning models.

## Model Performance
The models used in this dataset is Decision tree, kNN Classification and Random Forest classifier as there are no strong features correlated to the target.
GridSearchCV was used to search for the best parameters of each models 

|                | Decision Tree | kNN Classification | Random Forest | 
|:--------------:|:-------------------:|:------------------:|:----------:|
|    Accuracy    |         88.7%         |         89.2%        |     93.4%    |

The AUC score is used to see how well the models are able to classify binary cases as shown below.

![image](https://user-images.githubusercontent.com/85885666/233018459-0c68add1-25d8-424c-a3e7-ea33c909e90e.png)

The final model selected is the random forest classifier due to the high accuracy compared to the other models.


## Requirements
To run the notebook, you will need to have Python 3.6 or higher and the following libraries installed:

<ol>
  <li>Pandas</li>
  <li>Numpy</li>
  <li>Matplotlib</li>
  <li>Scikit-learn</li>
  <li>Seaborn</li>
</ol>

You can install these packages by running the following command using pip:
<code>
pip install pandas numpy matplotlib scikit-learn seaborn
</code>

## Usage
To use the notebook, you can simply open it in Jupyter and run each cell sequentially. The notebook is divided into several sections:

Introduction
Data Exploration
Data Cleaning and Preparation
Model Building and Training
Model Evaluation
The notebook contains detailed explanations of each step, as well as code snippets and visualizations to help you understand the process.

## Dataset
The dataset used in this notebook is a collection of data on loan applicants for a bank. The dataset consists of a total of 614 instances, each representing a loan application, and includes 13 predictor variables and 1 binary target variable representing whether or not the loan was approved. The target variable takes on the value of 1 if the loan was approved and 0 if it was not approved. The predictor variables provide various attributes of the loan applicants, such as gender, marital status, education level, loan amount, credit history, and more.

You can find the dataset at the following link: https://www.kaggle.com/datasets/arunavgautam/credit-risk-prediction-by-univai-hackathon

## License
The code in this repository is licensed under the MIT License. See [LICENSE.md](LICENSE.md) for more information.
