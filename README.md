# Education_Analysis
Anticipating student dropout rate through use of a machine learning model

## Content Page
1. Executive Summary
2. Data Preparation and Cleaning
3. Exploratory Data Analysis
4. Dummify Categorical Data
5. Effectiveness of Machine Learning (ML) Models

## 1. Executive Summary
**Objective**

Use machine learning to train a a model that can anticipate student dropout/failure in the program so we can help them in advance.

**Data Source**

Obtained from [Open Universiy Learning Analytics Dataset (OULAD)](https://analyse.kmi.open.ac.uk/open_dataset/download). Two years' worth of online learning data (assessments, courses, student info etc).

**To Do**

Step 1: Perform extensive data cleaning (combining workbooks, removing null entries etc.)

Step 2: Engineer new features and visualize student information

Step 3: Dummify categorical data for use in Machine Learning (ML) models

Step 4: Compare effectiveness of ML models: DummyClassifier, LogisticRegression, DecisionTree, RandomForestClassifier, GradientBoostingClassifier

Step 5: Tune the most effective model using GridSearchCV



## 2. Data Cleaning
Steps
1. Import necessary libraries
2. Read all csv files into Pandas Dataframes
3. Check for null values and fill with appropriate value
4. Merge relevant dataframes for further analysis

## 3. Exploratory Data Analysis
**Fig 1: No. of Students by Module Code**

![image](https://user-images.githubusercontent.com/74403956/121784173-14180580-cbe5-11eb-9b07-f0cacaa028f3.png)

**Fig 2: No. of Students by Gender**

![image](https://user-images.githubusercontent.com/74403956/121784202-3ad63c00-cbe5-11eb-8736-9525e57d233e.png)

**Fig 3: No. of Students by Geographic Region**

![image](https://user-images.githubusercontent.com/74403956/121784207-43c70d80-cbe5-11eb-8ca8-b33e0c3acb7c.png)

**Fig 4: No. of Students Per Education Level**

![image](https://user-images.githubusercontent.com/74403956/121784223-5d685500-cbe5-11eb-9e4d-4b283c0ebb54.png)

**Fig 5:  No. of Students Per IMD Band**

![image](https://user-images.githubusercontent.com/74403956/121784259-956f9800-cbe5-11eb-8d80-f69310f3c9be.png)

**Fig 6: No. of Students Per Age Band**

![image](https://user-images.githubusercontent.com/74403956/121784266-9ef90000-cbe5-11eb-96ba-62453f66c20b.png)

**Fig 7: Frequency of No. of Attempts**

![image](https://user-images.githubusercontent.com/74403956/121784940-82f75d80-cbe9-11eb-9064-d1a68678416a.png)

**Fig 8: Distribution of Studied Credits**

![image](https://user-images.githubusercontent.com/74403956/121784955-91457980-cbe9-11eb-8bbd-4e13b937b6da.png)

**Fig 9: No. of Students with Disability**

![image](https://user-images.githubusercontent.com/74403956/121784963-9c98a500-cbe9-11eb-9281-bbf095a5a757.png)

**Fig 10: No. of Students with Final Results**

![image](https://user-images.githubusercontent.com/74403956/121784973-afab7500-cbe9-11eb-9f7b-e88747bfe91d.png)

**Fig 11: Distribution of Total No. of Clicks**

![image](https://user-images.githubusercontent.com/74403956/121784985-bcc86400-cbe9-11eb-8d14-262c29889ac9.png)

**Fig 12: Distribution of Mean Score**

![image](https://user-images.githubusercontent.com/74403956/121784996-cce04380-cbe9-11eb-8398-52cade9423da.png)

**Fig 13: Distribution of Max Score**

![image](https://user-images.githubusercontent.com/74403956/121785018-ec776c00-cbe9-11eb-8344-f3fb7d597ae1.png)

**Fig 14: Results by Age Band**

![image](https://user-images.githubusercontent.com/74403956/121785060-37917f00-cbea-11eb-9dee-9b27a8aee2af.png)

**Fig 15: Results by IMD Band**

![image](https://user-images.githubusercontent.com/74403956/121785132-9bb44300-cbea-11eb-84cd-c59b92bd8152.png)

**Fig 16: Results by Gender**

![image](https://user-images.githubusercontent.com/74403956/121785142-ab338c00-cbea-11eb-91ef-11763cfc5af6.png)


## 4. Dummify Categorical Data

Dummify categorical data using .get_dummies(), drop_first = True.

<img width="966" alt="Screenshot 2021-06-13 at 2 02 57 AM" src="https://user-images.githubusercontent.com/74403956/121785284-8be92e80-cbeb-11eb-97ab-d0b19c49b0ec.png">


## 5. Effectiveness of Machine Learning (ML) Models
We will be testing the following models and computing their f1_score. The most accurate model will then be further tuned using GridSearchCV.

1. DummyClassifier

2. LogisticRegression

3. DecisionTree

4. RandomForestClassifier

5. GradientBoostingClassifier

Our test shows that the GradientBoostingClassifier model is the most effective (86% accuracy). We will optimise it with GridSearchCV using the following parameters:

<img width="1016" alt="Screenshot 2021-06-13 at 2 08 13 AM" src="https://user-images.githubusercontent.com/74403956/121785412-3bbe9c00-cbec-11eb-9d86-145d78b3108b.png">

The tuned model also has an accuracy of 86%, suggesting our model is already optimal.
