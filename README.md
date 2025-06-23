# Titanic_Survival_Rate
In this Task  a predictive model was built  that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).
Loading the data: Reads the Titanic-Dataset.csv file into a pandas DataFrame.
Handling missing values: Fills missing values in numeric columns with the median and in categorical columns with the mode.
Encoding categorical variables: Uses one-hot encoding to convert categorical columns into a numerical format, dropping the first category to avoid multicollinearity.
Standardizing numeric columns: Scales numeric columns to have a mean of 0 and a standard deviation of 1 using StandardScaler.
Boxplots and outlier removal: Generates boxplots for numeric columns to visualize outliers and then removes outliers using the Interquartile Range (IQR) method.
Saving the cleaned data: Saves the processed DataFrame to a new CSV file named "Cleaned_Titanic-Dataset.csv".
Boxplots and Outlier Removal (IQR Method):

Visualization: Boxplots are generated for each numeric column (after standardization) using matplotlib. These plots visually represent the distribution of the data and help in identifying potential outliers.
Outlier Detection and Removal: A function remove_outliers is defined to remove outliers based on the Interquartile Range (IQR) method.
For each specified numeric column, the 1st quartile (Q1) and 3rd quartile (Q3) are calculated.
The IQR is calculated as Q3 - Q1.
The lower bound for outliers is defined as Q1 - 1.5 * IQR.
The upper bound for outliers is defined as Q3 + 1.5 * IQR.
Rows where a value in a numeric column falls outside the [lower, upper] range are considered outliers and are removed from the DataFrame.
