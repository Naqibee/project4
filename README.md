# project4
ADULT INCOME DATA ANALYSIS

In this project, we are analyzing adult income in the USA as a class group project.

Our data source is from Kaggle website :https://www.kaggle.com/datasets/jainaru/adult-income-census-dataset

Introduction to the Project:

We used the US Adult Income Predictor Dataset to understand the relationship between socioeconomic factors and income. Factors like education level (elementary school education, high school graduation, some college education, bachelor, master, and doctorates), occupation (executive managerial, transportation, farming, fishing, etc.), age, sex, marital status, working hours per week, race, native country, and income. In our datasets, there are numerical data like age, education numbers and categorical data like sex, marital status, income, etc. Income is categorized as >=50 000 or <=50 000.

In this project, we are going to use classification tasks and compare which feature had the most effect on Income. Classification enables the prediction of categorical labels for new data points based on learned patterns from historical data. Classification models can handle both binary (two classes) and multi-class (more than two classes) problems, making them versatile for a wide range of applications. In our data work, the target variable is income, and the others are other features.

**Data Cleaning: **

I inspected the data, handled any missing or duplicate values, and dropped all rows with missing information. We reviewed the columns and discarded or simplified some of them.

Data Transformation:

● Encoding Categorical Variables: Converting categorical data into numerical format using techniques like one-hot encoding or label encoding. changing the categorical (income) into the binary

● Feature Engineering: we created new features from existing data to improve model performance.

Data Visualization

● Visualize the data to understand distributions and relationships. ● Balanced the data by comparing over to check for oversampling and undersampling. As we see in the Income plot, the distribution is unbalanced and not distributed evenly. ● For balancing, we used KNeighborsClassifier for the classification algorithm in machine learning. Techniques to Balance Data: ● Oversampling: increasing the number of instances in the minority class. ● Random Oversampling: Duplicating random instances from the minority class. ● Under sampling: decreasing the number of instances in the majority class. ● Random undersampling: randomly removing instances from the majority class.

Outcome after Balancing:

Accuracy on Oversampled Test Set: 0.825 Accuracy on Undersampled Test Set: 0.81 Accuracy on Original Train Set: 0.92 Accuracy on Oversampled Train Set: 0.94 Accuracy on Undersampled Train Set: 0.861

Data Normalization:

Min-Max Scaling: scaling data to a fixed range, typically [0, 1].
Split the Data: Split the dataset into training and test sets. Splitting the data refers to the process of dividing a dataset into multiple subsets. Testing and training data.

● Training Set: Used to train the model. ● Test Set: Used to evaluate the model's performance on unseen data ● from sklearn.model_selection import train_test_split, ● Apply Preprocessing: Fit and transform the training data and transform the test data using the combined preprocessing pipeline.

Model Building: Model Building and Evaluation Split the data, train a machine learning model, and evaluate its performance using classification metrics and a confusion matrix. Data Model Optimization: valuing the Optimized Model: Evaluate the final model using classification metrics and a confusion matrix.

Training the Model:

For the model, we train Logistic Regression, Rondem Forest, Decision Tree, and MPL.

Logistic Regression model:

Rondom Forest Classifier:

Classification Report:

Accuracy: 0.8505308560053085 Classification Report: precision recall f1-score support

   	0   	0.89      0.92  	0.90  	4580
   	1   	0.71      0.64  	0.67  	1448

accuracy    	                   0.85  	6028
macro avg 0.80 0.78 0.79 6028 weighted avg. 0.85 0.85 0.85 6028

MLP Classifiers a Neural Network Algorithm:

A Multi-Layer Perceptron (MLP) classifier is a type of artificial neural network used for supervised learning tasks. It is one of the simplest and most basic forms of neural networks, consisting of multiple layers of nodes, or "neurons," that are interconnected and operate in a feedforward manner. Here’s a breakdown of its key components and how it works:

MLP classifiers are foundational in neural network models and serve as a basis for understanding more complex architectures such as convolutional neural networks (CNNs) and recurrent neural networks (RNNs). Accuracy: 0.805242203052422 Confusion Matrix: [[4411 169] [1005 443]] Classification Report: precision recall f1-score support

   	0   	0.81      0.96  	0.88  	4580
   	1   	0.72      0.31  	0.43  	1448

accuracy                       	0.81  	6028
macro avg 0.77 0.63 0.66 028 weighted avg 0.79 0.81 0.77 6028

In conclusion, between the MLP/Random Forest, the Random Forest is the best performing algorithm with 85% accuracy.

This is due to 2 reasons: 1.) Out of all the states predicted to have a certain average income, 85% are correctly predicted. Subsequently, this proves a 15% error rate, which is very minimal. 2.) 2.) In terms of real life compatibility, this model's predictions can be utilized to make informed decisions regarding resource allocation or policy analysis. To specify, banks and other businesses can use this model when analyzing/referencing future finances of clients.
