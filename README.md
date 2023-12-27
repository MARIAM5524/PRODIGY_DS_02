# PRODIGY_DS_02
 It is the second task in my internship with prodigy InfoTech





Exploratory Data Analysis (EDA) on Titanic Dataset:

Introduction:

This document outlines the process of performing data cleaning and exploratory data analysis (EDA) on the Titanic dataset. The dataset contains information about passengers aboard the Titanic.

Code and Explanations:

1. Importing necessary libraries:

-- import pandas as pd

-- import matplotlib.pyplot as plt

-- import seaborn as sns

- Explanation: These libraries are imported to facilitate data handling, visualization, and analysis.



2. Loading the dataset:

-- titanic_data = pd.read_csv('titanic.csv')

-- print(titanic_data.head())

- Explanation: The dataset is loaded using Pandas' read_csv() function, and the first few rows are displayed to understand its structure.



3. Data Cleaning:

-- # Handling missing values

-- print(titanic_data.isnull().sum())

-- titanic_data['Age'].fillna(titanic_data['Age'].median(), inplace=True)

-- titanic_data['Embarked'].fillna(titanic_data['Embarked'].mode()[0], inplace=True)

-- titanic_data.drop('Cabin', axis=1, inplace=True)

- Explanation: Missing values in the 'Age' and 'Embarked' columns are filled with median and mode values, respectively. The 'Cabin' column is dropped due to a high number of missing values.



4. Exploring Relationships and Patterns:

** Analyzing survival rate by different variables:

-- # Survival rate by sex

-- sns.countplot(x='Sex', hue='Survived', data=titanic_data)

-- plt.title('Survival Count by Sex')

-- plt.show()

- Explanation: Count plots are generated to analyze survival rates based on sex, passenger class, age, and embarked port.

** Analyzing correlations between numerical variables:

-- # Correlation matrix for numerical variables

-- corr_matrix = titanic_data.corr()

-- sns.heatmap(corr_matrix, annot=True, cmap='coolwarm', fmt='.2f')

-- plt.title('Correlation Matrix')

-- plt.show()

- Explanation: A heatmap is created to visualize the correlation matrix between numerical variables, displaying correlations using colors and annotations.



5. Further Analysis and Insights:

Observations from Visualizations:

- Survival by Sex: The count plot indicates that females had a higher survival rate compared to males.

- Survival by Passenger Class: Higher-class passengers (Pclass) had better survival chances.

- Survival by Age: The histogram shows the distribution of survival based on age.

- Survival by Embarked Port: The count plot displays survival rates based on the port of embarkation.



6. Insights from Correlation Matrix:
- The correlation matrix heatmap illustrates the relationships between numerical variables.

- Positive or negative correlations between features can be observed, aiding in feature selection for further analysis or modeling.



7. Additional Insights and Conclusions:

** Survival Patterns and Demographics:

- Survival by Family Size: Analyzing survival rates concerning family size (combining 'SibSp' and 'Parch' columns) might provide insights into the importance of traveling with family.

- Age Distribution of Survivors: Further investigation into the age distribution among survivors and non-survivors could reveal age-specific survival patterns.

** Feature Engineering Opportunities:

- Name Titles as a Feature: Extracting titles from passenger names (e.g., Mr., Mrs., Dr.) might unveil social or gender-specific survival trends.

- Creating Age Groups: Binning ages into groups (e.g., children, adults, seniors) could reveal age-specific survival rates.



Recommendations and Future Steps:

- Model Building: Utilize machine learning algorithms (e.g., logistic regression, random forests) to predict survival based on the dataset features.

- Cross-Validation and Model Evaluation: Perform cross-validation and model evaluation to ensure robustness and accuracy of predictive models.

- Feature Importance: Evaluate feature importance to understand which variables contribute most significantly to survival predictions.

- Iterative Analysis: EDA is an iterative process; revisiting visualizations and exploring additional variables might reveal deeper insights.



Conclusion:

- The analysis of the Titanic dataset offered valuable insights into the factors influencing survival rates among passengers. Through exploratory data analysis (EDA), several significant trends and patterns emerged, shedding light on the dynamics of survival aboard the Titanic.


** Key Findings:

- Gender Disparity in Survival: The data prominently revealed a higher survival rate among females compared to males, emphasizing the 'women and children first' protocol during the Titanic tragedy.

- Class-Based Disparities: Passengers in higher classes exhibited higher survival rates, indicating potential priority given to individuals in upper-class accommodations.

- Age and Survival: While age alone didn't show a stark correlation with survival, further analysis might uncover nuanced age-specific trends.


** Insights and Implications:

- Social Dynamics: The analysis hinted at the influence of societal norms and protocols during emergency situations, notably the adherence to gender and class-based priorities during evacuation.

- Data Limitations: The dataset's completeness and missing information, particularly in the 'Cabin' column, presented challenges and potentially limited the depth of analysis.

- Future Analysis Opportunities: Further feature engineering and advanced modeling techniques could refine predictions and offer deeper insights into survival probabilities.


** Recommendations:
- Feature Engineering: Explore additional features such as family size or titles extracted from names to enhance the predictive capacity of models.

- Modeling and Validation: Apply machine learning models for predictive analysis, ensuring robust validation and evaluation techniques to validate model performance.

- Iterative Exploration: Continuously revisit and refine analysis techniques to uncover hidden trends or correlations not initially apparent.


** Final Thoughts:

- The exploration of the Titanic dataset underscored the complex interplay of socio-economic factors and survival probabilities during a historical catastrophe. While this analysis provides a foundational understanding, further in-depth analysis and modeling endeavors are vital to unravel more intricate patterns and enhance predictive capabilities.

- The insights gained not only deepen our understanding of historical events but also underscore the importance of comprehensive data analysis in understanding human behavior in critical situations.