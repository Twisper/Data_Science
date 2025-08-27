# Titanic - Machine Learning from Disaster
This repository contains all the files and Jupyter Notebook for data processing and machine learning  
Link to the contest on Kaggle: [here](https://www.kaggle.com/competitions/titanic)

[train.csv](./train.csv) is training set  
[test.csv](./test.csv) is test set  
[submission.csv](./submission.csv) is final answer  
[Titanic.ipynb](./Titanic.ipynb) is a Jupyter Notebook, which works with data and gives final answer

### How does the program work?

I am using here Logistic Regression model. I'm importing all data from .csv files, then I'm merging training and test sets.  
This is crucial for DataFrame managing. Training and test sets could differ in some data, so, we can solve this problem by just merging two sets into one.  
After that, data preprocessing begins. I'm extracting passengers' titles and replacing rare such as Col, Capt, Dr, etc. with "Rare".  
I'm missing data in Age, Fare, Cabin, Deck. In Age I'm filling missing data with median of certain category. Same with Fare.  
Missing data in Cabin I'm filling with U and Deck with first character from Cabin.  
Every other categorial column I'm transforming into binary columns. And also, I'm dropping all unnecessary columns.  
After that, I'm dividing DataFrame back into training and test sets, training LogisticRegression model and writing answer into submission.csv based on test set