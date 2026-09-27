The dataset includes information such as:

PassengerId: Unique ID for each passenger.

Survived: Survival (0 = No, 1 = Yes) - Target Variable.

Pclass: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd).

Name: Passenger name.

Sex: Passenger sex.

Age: Age in years.

SibSp: # of siblings/spouses aboard the Titanic.

Parch: # of parents/children aboard the Titanic.

Ticket: Ticket number.

Fare: Passenger fare.

Cabin: Cabin number.

Embarked: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

The dataset can be found here:

https://github.com/datasciencedojo/datasets/blob/master/titanic.csv

To download this data using terminal, run the following command:

!wget https://raw.githubusercontent.com/datasciencedojo/datasets/refs/heads/master/titanic.csv  

Task 1: Data Loading and Initial Inspection
Load the dataset (e.g., using pandas in Python).

Display the first 5 rows to get a quick look at the data structure.

Check the data types of all columns (.info()).

Get descriptive statistics of the numerical columns (.describe()).

Identify the total number of missing values for each column.

Task 2: Handling Missing Values
Missing data can skew analysis. For this task, you will address the missing values in three key columns: Age, Cabin, and Embarked.

Cabin:

Calculate the percentage of missing values in the Cabin column.

Decision: Do we need to drop the Cabin column entirely from the analysis? Briefly justify your reason.

Embarked:

Find the most frequent port of embarkation (the mode).Impute the missing values in the Embarked column with the mode.

Age:

Impute the missing values in the Age column with the median age. 

Task 3: Univariate Analysis 
Univariate analysis looks at a single variable at a time.

Survival Rate:

Calculate the overall survival rate (percentage of passengers who survived).

Visualize the distribution of the Survived variable (e.g., a count plot/bar chart).

Passenger Class (Pclass):

Visualize the distribution of Pclass using a count plot.

Identify which class had the most passengers.

Age Distribution:

Plot a histogram of the Age column to visualize its distribution.

Task 4: Bivariate and Multivariate Analysis 
Bivariate analysis explores the relationship between two variables, specifically focusing on how other features relate to the target variable (Survived).

Survival by Sex:

Create a crosstabulation (or a grouped count) to show the count of survivors and non-survivors grouped by Sex.

Visualize this relationship using a stacked bar chart or a grouped count plot.

Question: Which gender had a significantly higher survival rate?

Survival by Class (Pclass):

Calculate and visualize the survival rate for each Pclass.

Question: Is there a clear correlation between ticket class and survival probability?

Survival by Age:

Plot and compare the age distribution of survivors vs. non-survivors.

Observation: What does the plot suggest about the survival chances of children and the elderly?

Survival by Port of Embarkation (Embarked):

Calculate and visualize the survival rate for each Embarked port.

Task 5: Conclusion and Insights 
Based on your EDA, write a brief (3-5 sentences) conclusion summarizing the most significant factors affecting survival on the Titanic. Highlight the top 2-3 features that appear to be the strongest predictors of survival.
