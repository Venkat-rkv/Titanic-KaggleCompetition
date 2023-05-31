# Titanic-KaggleCompetition
Using ML, created a model that predicts which passengers survived the Titanic shipwreck. 

# Dataset
https://www.kaggle.com/competitions/titanic/data

The "train.csv" dataset includes information about a subset of passengers (specifically, 891 passengers) onboard the Titanic. Importantly, this dataset reveals whether each passenger survived or not, serving as the "ground truth."

On the other hand, the "test.csv" dataset contains similar information about another set of passengers, but it does not disclose the survival outcomes for these individuals. My task was to predict whether those 418 passengers from the test dataset survived or not based on the patterns and insights I uncover from the train dataset.

# How did I do it ?
After discussing with my classmates, I developed a plan for my project execution. I started by reading the test and train datasets, dropping the "Survived" column from the training data and storing it as the "y_training" data. I then conducted exploratory data analysis by examining the values present in different columns. To gain further insights, I utilized the pandas_profiling library for visualization and analysis. For detailed visualizations, please refer to the attached HTML files containing the visualizations of the training and testing datasets.

During the exploration, I focused on various statistics such as missing values, data distributions, and types. After identifying columns with null values, I proceeded with data preprocessing steps. I grouped common titles together in both the training and testing data. For the training data, I imputed median values for the "Age" column, assigned binary values for "male" and "female," filled the "Embarked" column with "S," and replaced its values with numerical data (1, 2, 3). Additionally, I dropped columns that I believed had minimal contribution to the prediction. Similar steps were applied to the testing data, including imputing median values for "Age" and "Fare."

Next, I trained the data using the random forest classifier and made predictions on the test data. Finally, I generated and saved a submission .csv file.

# Result
Regarding the results, I initially experimented with various models such as SVM, Logistic Regression, Linear Regression, CNN, and ANN. However, these models did not yield satisfactory scores, except for the Random Forest, which provided a decent score (>70%). Furthermore, when I grouped the names under common titles, there was a slight improvement in the score.
