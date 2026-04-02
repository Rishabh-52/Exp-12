AIM
To perform categorical data analysis using Python's Pandas library on student and e-commerce order datasets, by applying techniques such as frequency counts, percentage distributions, cross-tabulations, grouping, filtering, and sorting on categorical columns.

THEORY
Categorical Data refers to data that represents distinct groups or categories rather than continuous numerical values. Examples include Gender (Male/Female), Department (CSE, IT, ECE), Grade (A, B, C), and Payment Method (UPI, Card, Cash). Analyzing categorical data helps uncover patterns, distributions, and relationships between groups.
Pandas provides a rich set of tools for categorical data analysis:
value_counts() counts the frequency of each unique category in a column. Using the normalize=True parameter converts the counts to proportions, and multiplying by 100 gives the percentage distribution. This is essential for understanding how data is distributed across categories.
pd.crosstab() creates a cross-tabulation (contingency table) that shows the frequency of combinations between two or more categorical variables — for example, how many Male vs Female students received each Grade. Using normalize='index' gives the row-wise percentage distribution, making it easy to compare groups.
groupby() splits the DataFrame into groups based on one or more categorical columns and applies an aggregation function. For instance, grouping by Department and then counting Grade values reveals the grade distribution within each department.
unique() returns an array of all unique values present in a categorical column, and nunique() returns the count of those unique values — both useful for understanding cardinality.
Filtering involves selecting rows that satisfy a condition (e.g., df[df['Category'] == 'Electronics']), allowing focused analysis on specific categories.
Sorting with sort_values(by='column') arranges rows in ascending or descending order based on a categorical column, which helps in organizing and reading the data more clearly.
These techniques together form the foundation of Exploratory Data Analysis (EDA) for categorical variables, enabling meaningful insights before applying any machine learning or statistical models.

CONCLUSION
In this experiment, categorical data analysis was successfully performed on two datasets using Pandas:
Dataset 1 — Student Dataset (60 records): Columns included Student ID, Gender, Department, and Grade. Key findings:

Grade B was most common (24 students, 40%), followed by Grade A (22 students, 36.67%) and Grade C (14 students, 23.33%).
Gender distribution was perfectly balanced — 30 Male and 30 Female students.
CSE had the most students (20), followed by IT (18), and ECE and Mechanical (11 each).
Cross-tabulation showed that Female students performed better overall, with 14 getting Grade A compared to 8 Males.
CSE had the highest percentage of A grades (65%), while Mechanical had 0% A grades.

Dataset 2 — E-Commerce Orders Dataset (10 records): Columns included Category, Payment Method, Delivery Type, and Customer Type. Key findings:

Electronics was the most ordered category (40%), while Clothing and Grocery were each 30%.
Cross-tabulation revealed a perfect mapping: Electronics orders used only UPI, Clothing used only Card, and Grocery used only Cash.
Grouping confirmed that each category was exclusively associated with one payment method.

Thus, the experiment demonstrated how Pandas functions like value_counts(), crosstab(), groupby(), unique(), filtering, and sorting can be effectively used to extract meaningful insights from categorical data.
