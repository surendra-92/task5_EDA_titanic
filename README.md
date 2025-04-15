#task5 
in this import the pandas and seaborn , matplotlib
then 

#1. What is EDA and why is it important?
EDA (Exploratory Data Analysis) is the process of analyzing datasets to summarize their main characteristics, often using visual methods.

✅ Why it’s important:

Understand data structure and quality

Detect missing values, outliers, and skewness

Identify patterns, relationships, or anomalies

Help with feature selection and model choice

#2. Which plots do you use to check correlation?
To visualize correlation between numerical features:

Heatmap (sns.heatmap) — shows the correlation matrix with color gradients.

Pairplot (sns.pairplot) — scatterplots for all numerical features.

Scatter plot (sns.scatterplot) — for specific pairs of variables.

#3. How do you handle skewed data?
Skewed data can affect model performance. To handle it:

Log Transformation: df['column'] = np.log1p(df['column'])

Square Root or Box-Cox Transformation

Remove outliers (if appropriate)

Use robust models (like tree-based models which handle skew better)

#4. How to detect multicollinearity?
Multicollinearity means two or more features are highly correlated.

✅ Methods to detect:

Correlation Matrix (via heatmap)

Variance Inflation Factor (VIF):

python
Copy
Edit
from statsmodels.stats.outliers_influence import variance_inflation_factor
A VIF > 5 or 10 indicates high multicollinearity.

5. What are univariate, bivariate, and multivariate analyses?

Type	Meaning	Example
Univariate	Analyzing one variable	Histogram of age
Bivariate	Two variables	age vs survived
Multivariate	More than two variables	age, fare, and pclass together


#6. Difference between heatmap and pairplot?

Feature	Heatmap	Pairplot
Purpose	Show correlation strength	Visualize relationships
Visual	Matrix with colors	Grid of scatter plots
Type	Summary view	Detailed pairwise view
Example	sns.heatmap(df.corr())	sns.pairplot(df)


#7. How do you summarize your insights?
When summarizing EDA insights:

✅ Focus on:

Key trends (e.g., “Women had higher survival rates”)

Correlations (e.g., “Fare is positively correlated with survival”)

Data issues (missing values, outliers, skewed columns)

Recommendations (feature transformations, dropping features, etc.)

🔍 Example:

"EDA shows survival is strongly influenced by gender and class. Fare has some outliers and is right-skewed, which may need transformation. No high multicollinearity observed among numerical features."
