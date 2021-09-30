# DS3 Human Phone Activity

### This project focuses on testing 7 different machine learning models: K nearest neighbors, decision trees, support vector machine, random forest, logistic regression, XGBoost and an artificial neural network. They were tested on a dataset of 10000 samples taken from UCI's machine learning repository that used accelerometer and gyroscope sensors to collect data on subjects to determine their activity. These activities were walking, standing, walking upstairs, walking downstairs, laying and sitting. 

### We first started with importing and cleaning the data by getting rid of null values and ensuring values were standardized across features. 

### We performed exploratory data analysis by looking at how many samples of each activity we had in order to make sure it was balanced throughout. Data visuals can be seen in the EDA notebook. We looked at differences between the activities across different features to gain a better understanding of the data. 

### Because our data consisted of over 500 features, and because one of different dimensionality reduction methods we would use on our data prior to testing them on models. Ultimately we decided on PCA and determined 40 components would be a good number because we found that it was at 40 when it reached 90% of the explained variance of the data. 

### Because our data consisted of over 500 features, and because one of our goals was to reduce our training times, we began exploring dimensionality reduction methods we would use on our data prior to training our models. Ultimately we decided on PCA and determined 40 components would be a good number since this was when it reached 90% of the explained variance of the data

### After performing PCA and obtaining our new data, we began to train and test our models. We would first collect 5 subsets of 5000 samples of the training dataset which consisted of around 7,000 samples. Then for each sample we would use grid search to find the best performing hyperparameters and test it on the testing dataset to obtain accuracy score, precision scores and f1 scores. This resulted in 15 scores altogether per model, 1 for each subset of the data and 5 for each scoring metric. By doing so we would be able to test for signifigance when finding which models performed better than the rest and find p-values. 

### The three models that performed the best were Logistic Regression with around 92% accuracy score, SVM with around 92% accuracy score, and XGBoost with an accuracy score of 90%. 

### We wanted to see how much more we could increase these scores on these three models if trained on the original data, and found that although training times were significantly longer than when they were trained using the PCA data, it did result in higher accuracies. Logistic regression increased to nearly 96%, SVM to 94% and XGBoost to an average 94% accuracy score. 