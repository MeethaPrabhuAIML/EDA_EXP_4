# EDA_EXP_4   Titanic Survival Analysis using Univariate Analysis

## Aim

To perform univariate analysis on the Titanic dataset to understand the distribution and characteristics of individual variables (such as Age, Sex, Pclass, Fare, and Survived) and to draw insights about passengers and their survival patterns.


## Algorithm

)Import Libraries:

Load the required Python libraries (pandas, numpy, matplotlib, seaborn).

2)Load the Dataset:**

Read the Titanic dataset from available sources (e.g., seaborn’s built-in Titanic dataset or a CSV file).

3)Data Inspection:**

View the first few rows using head().

Get dataset summary using info() and describe().

4)Handle Missing Data:
Identify missing values using isnull().sum() and handle them appropriately (e.g., fill or drop).

5)Univariate Analysis:
Perform univariate analysis for each variable:

### Categorical Variables: (e.g., Sex, Pclass, Survived, Embarked)
Use frequency tables and count plots.

### Numerical Variables: (e.g., Age, Fare)
Use histograms, box plots, and summary statistics.

### 6)Interpretation:
Analyze distributions, central tendencies, and spread.
Identify patterns (e.g., more passengers in 3rd class, survival differences by gender).


## Program

Name : MEETHA PRABHU

Reg No.: 212222240065

## Write your code here
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = sns.load_dataset("titanic")
df.head()

df.shape

df.isnull().sum()

df["sex"].value_counts()

sns.countplot(x='sex', data=df)
plt.title("Distribution of Gender")
plt.show()

print("percentage of passengers survived")
df["survived"].value_counts(normalize=True) * 100

df["pclass"].value_counts()

sns.countplot(x='pclass', data=df)
plt.title("Passenger class distribution")
plt.show()

df['embarked'].value_counts()

sns.countplot(x='embarked', data=df)
plt.title("passengers embarked from each port")
plt.show()

df["deck"].value_counts()

sns.countplot(x='deck', data=df)
plt.title("Deck distribution")
plt.show()

plt.figure(figsize=(8, 6))
sns.boxplot(y='fare', data=df)
plt.title('Distribution of Passenger Fare')
plt.ylabel('Fare')
plt.grid(axis='y', alpha=0.75)
plt.show()

print(f"Mean Fare: {df['fare'].mean():.2f}")
print(f"Median Fare: {df['fare'].median():.2f}")

plt.figure(figsize=(10, 6))
sns.histplot(df['fare'], bins=50, kde=True)
plt.title('Distribution of Passenger Fare')
plt.xlabel('Fare')
plt.ylabel('Frequency')
plt.grid(axis='y', alpha=0.75)
plt.show()
```

## Output
<img width="245" height="546" alt="image" src="https://github.com/user-attachments/assets/f537f88c-606b-4aa9-977f-0d2e8a6e749f" />

<img width="630" height="449" alt="image" src="https://github.com/user-attachments/assets/25c5837d-2125-4c6d-bd12-65635e25218c" />

<img width="577" height="454" alt="image" src="https://github.com/user-attachments/assets/92a0a944-73f8-491b-a686-f68455ed4574" />

<img width="605" height="458" alt="image" src="https://github.com/user-attachments/assets/96c67914-fb9e-411a-a202-15ff581c0b9a" />

<img width="613" height="460" alt="image" src="https://github.com/user-attachments/assets/6e5fdb93-bb6b-4f96-81f0-decb05e6cee5" />

<img width="797" height="552" alt="image" src="https://github.com/user-attachments/assets/a76c09e8-e7a8-4142-b811-4a28216ac27f" />

<img width="745" height="513" alt="image" src="https://github.com/user-attachments/assets/0091595a-a2f3-48b0-86f0-f5f1e0c96717" />

<img width="812" height="512" alt="image" src="https://github.com/user-attachments/assets/ed163897-1ac4-4ea8-b5a1-b37d6862a8af" />


## Result
From the univariate analysis:

Majority of passengers were male and in 3rd class.

Around 38% survived, majority being females and higher-class passengers.

Age is right-skewed with most passengers aged 20–40 years.

Fare distribution shows a few high outliers for 1st class passengers.

Thus, univariate analysis helps understand the distribution and spread of each individual feature in the Titanic dataset before moving to bivariate or multivariate analysis.

Visualization:
Plot appropriate charts for each variable using Matplotlib/Seaborn.
