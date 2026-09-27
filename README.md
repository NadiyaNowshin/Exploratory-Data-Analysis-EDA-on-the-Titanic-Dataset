# Titanic Dataset: Exploratory Data Analysis

## Project Overview

This project performs an **Exploratory Data Analysis (EDA)** of the Titanic passenger dataset to investigate the factors associated with passenger survival.

The analysis covers data loading and inspection, missing-value handling, univariate analysis, and bivariate/multivariate analysis. The objective is to understand how characteristics such as **gender, passenger class, age, and port of embarkation** relate to survival outcomes.

## Dataset

The dataset contains information about passengers aboard the Titanic, including demographic, ticket, and survival information.

### Features

| Feature       | Description                                                               |
| ------------- | ------------------------------------------------------------------------- |
| `PassengerId` | Unique identifier for each passenger                                      |
| `Survived`    | Survival status: `0` = No, `1` = Yes                                      |
| `Pclass`      | Passenger ticket class: 1st, 2nd, or 3rd                                  |
| `Name`        | Passenger name                                                            |
| `Sex`         | Passenger gender                                                          |
| `Age`         | Passenger age in years                                                    |
| `SibSp`       | Number of siblings/spouses aboard                                         |
| `Parch`       | Number of parents/children aboard                                         |
| `Ticket`      | Passenger ticket number                                                   |
| `Fare`        | Passenger fare                                                            |
| `Cabin`       | Passenger cabin number                                                    |
| `Embarked`    | Port of embarkation: `C` = Cherbourg, `Q` = Queenstown, `S` = Southampton |

### Dataset Source

The dataset is available from the [Data Science Dojo Titanic Dataset](https://github.com/datasciencedojo/datasets/blob/master/titanic.csv).

The raw dataset can also be downloaded using:

```bash
wget https://raw.githubusercontent.com/datasciencedojo/datasets/refs/heads/master/titanic.csv
```

## Objectives

The main objectives of this project are to:

* Inspect and understand the structure of the dataset
* Identify and handle missing values
* Analyze individual variables using univariate analysis
* Investigate relationships between passenger characteristics and survival
* Visualize important patterns in the data
* Identify the features that appear to have the strongest relationship with survival

## Analysis

### 1. Data Loading and Initial Inspection

The dataset is loaded using **Pandas** and initially inspected to understand its structure.

The analysis includes:

* Displaying the first five rows
* Examining column data types using `.info()`
* Generating descriptive statistics using `.describe()`
* Identifying missing values in each column

### 2. Handling Missing Values

Missing values are examined and addressed for the following columns:

#### Cabin

The percentage of missing values in the `Cabin` column is calculated. Because a large proportion of cabin information is missing, the usefulness of this feature is evaluated before deciding whether to retain or remove it from the analysis.

#### Embarked

The most frequently occurring embarkation port is identified using the mode. Missing values in `Embarked` are then replaced with the most frequent value.

#### Age

Missing values in `Age` are replaced with the **median age** of the passengers.

## 3. Univariate Analysis

Univariate analysis examines individual variables independently.

### Survival Rate

The overall percentage of passengers who survived is calculated and visualized using a count plot/bar chart.

### Passenger Class

The distribution of passengers across the three ticket classes is visualized to determine which class contained the largest number of passengers.

### Age Distribution

A histogram is used to examine the distribution of passenger ages and identify the general age patterns within the dataset.

## 4. Bivariate and Multivariate Analysis

This section investigates relationships between passenger characteristics and the target variable, `Survived`.

### Survival by Sex

The number and proportion of survivors and non-survivors are compared across passenger genders using crosstabulation and visualizations.

This analysis helps examine whether survival outcomes differed substantially between male and female passengers.

### Survival by Passenger Class

Survival rates are calculated for each passenger class and visualized to examine the relationship between ticket class and survival.

This provides insight into whether passenger class was associated with different survival outcomes.

### Survival by Age

The age distributions of survivors and non-survivors are compared using visualizations.

Particular attention is given to the survival patterns among **children, adults, and elderly passengers**.

### Survival by Port of Embarkation

Survival rates are calculated and visualized for each embarkation port:

* Cherbourg (`C`)
* Queenstown (`Q`)
* Southampton (`S`)

This analysis explores whether survival outcomes varied depending on the passenger's port of embarkation.

## 5. Key Insights

The analysis examines several factors that may be associated with Titanic passenger survival, particularly:

* **Sex**
* **Passenger class (`Pclass`)**
* **Age**
* **Port of embarkation (`Embarked`)**

The visualizations and statistical summaries are used to identify patterns and differences in survival outcomes across these groups.

> **Note:** Observed relationships in this exploratory analysis indicate associations within the dataset and should not be interpreted as evidence that a particular feature directly caused survival.

## Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**

## Project Structure

```text
Titanic-EDA/
│
├── Titanic_EDA.ipynb
├── titanic.csv
└── README.md
```

## How to Run

### Option 1: Google Colab

Open the `.ipynb` file in Google Colab and run the notebook cells sequentially.

### Option 2: Local Environment

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Navigate to the project directory:

```bash
cd YOUR_REPOSITORY
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

Then open the notebook using Jupyter Notebook or JupyterLab.

## Author

**Nadiya Nowshin**

