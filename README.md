# Sales-data-analysis
I. PROBLEM STATEMENT
In retail, a large share of revenue often comes from a small portion of products and
customers. Without structured analysis, identifying these key drivers and
understanding factors like discounts, best selling products,etc becomes diﬃcult. This
project aims to analyze retail sales data to uncover trends across categories, regions,
and time, apply the Pareto principle to find top contributors, and build a regression
model to predict sales.

II. INTRODUCTION
The primary goal of our project is to perform EDA and understand the various trends
amongst diﬀerent factors that aﬀect the sales and build a model that can predict the
sales for given features.
Our dataset is the SuperStore dataset which contains 21 features. It contains various
features such as:
Row ID, Order ID, Order Date, Ship Date, Ship Mode, Customer ID, Customer Name,
Segment, Country, City, State, Postal Code, Region, Product ID, Category,
Sub-Category, Product Name, Sales, Quantity, Discount, Profit

III. EXPLORATORY DATA ANALYSIS (EDA)
After loading our data, we have performed Exploratory Data Analysis. We inferred
various trends from this analysis among diﬀerent features of our data.
The EDA showed that our dataset had no initial missing values.
The analysis revealed several notable trends. Oﬃce Supplies and Technology
categories exhibited the highest sales volume, while Furniture demonstrated lower
profit margins. Certain sub-categories like Chairs and Tables showed significant
variability in profit, possibly due to discounting practices. Regional analysis indicated
that the Western and Eastern regions generated the highest overall sales, while the
Southern region contributed the least. The Corporate and Consumer segments
accounted for the bulk of revenue, though the Home Oﬃce segment displayed strong
profitability per transaction.
The Pareto analysis indicates a strong product concentration where only 22.35% of
products generate 80% of sales, but a weak customer concentration, requiring nearly
50% of the customer base to account for 80% of revenue, suggesting a need to focus on
identifying and fostering high-value customer segments.

IV. METHODOLOGY
Data was first loaded and inspected for missing values and inconsistencies.
Preprocessing steps included type conversion, handling of null values, and
normalization of numerical variables. Exploratory Data Analysis was performed as
shown in the above section. Sales and profit distributions were analyzed across
product categories and customer segments. Time-series trends were examined to
identify seasonal variations in sales.
Models for predicting sales were built using Linear Regression, Random Forest
regressor, and XGBoost. Correlation heatmaps and feature importance analyses were
employed to determine which attributes most strongly influenced sales. Various
plots—such as bar charts, line graphs, and scatter plots—were used to interpret the
model performance.

V. RESULTS AND ANALYSIS
In our initial analysis, we included the Profit feature to predict sales. This inclusion
caused a data leakage of our models and making it more biased to Profit since it has a
direct correlation with the Sales.
Another set of models was built and trained to show this data leakage.
Models with Profit
Models without Profit
The performance of our models dropped significantly, which shows that our model
has become more generalised and will work well in the real world since its not
learning directly from Profit.

VI. CONCLUSION
This analysis shows that the model performs well when predicting stable, consistent
sales patterns where variance is low and data is plentiful, allowing it to easily learn
regular trends. However, it struggles with unpredictable, high-variance spikes that
occur in less popular items. Since the model minimizes overall error, it tends to
underpredict rare, extreme sales events to remain accurate most of the time. As a
result, while it eﬀectively captures everyday sales behavior, it fails to adapt to sudden,
irregular surges, leading to significant underprediction errors.

VII. FUTURE WORK
Our tree-based models exhibited signs of overfitting, indicating that they captured
noise along with meaningful patterns. To address this, future work can focus on
implementing regularization techniques, pruning, or ensemble methods to improve
generalization. Additionally, exploring more eﬃcient and lightweight models could
enhance prediction accuracy and reduce computational cost. Hybrid modeling
approaches—combining linear models to capture simple trends and nonlinear models
to learn complex relationships—could also be employed to achieve a more balanced and robust performance
