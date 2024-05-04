# Task - 1
## Correlation Analysis
The first step is calculating the correlation between the Discount and Total Amount Spent. Use Excel’s CORREL() function to do this.

## Observations
A positive correlation of approximately 0.406 between the Discount and the Total Amount Spent exists. This correlation is moderate, suggesting a relationship between these two variables but is not particularly strong.

The scatter plot visualizes the relationship between the Discount and the Total Amount Spent for each transaction in the dataset. Each point on the plot represents a single transaction, with its position along the x-axis indicating the discount and its status along the y-axis indicating the total amount spent.

Looking at the scatter plot, you can see that as the Discount increases, the Total Amount Spent also tends to increase, which aligns with the positive correlation we calculated. This trend suggests that customers spend more when the discount is higher—perhaps due to customers perceiving higher value in discounted products and willing to spend more.

But the spread of points on the plot shows variability in the data. While the general trend is upward, many transactions do not follow this trend. For example, there are transactions with high discounts but relatively low total amounts spent and transactions with low discounts but high total amounts expended.

These outliers could be due to many factors. For instance, some customers might be more price-sensitive than others and more influenced by discounts. Or certain products might have been discounted heavily but are not popular or do not meet customers' needs, leading to lower total spending. Alternatively, some products might have low discounts but are very popular or in high demand, leading to higher total expenditures. Outliers are not always wrong; they can be essential to the data and provide valuable information.

In conclusion, while there’s a positive relationship between the Discount and the Total Amount Spent, there’s significant variability in the data, and many transactions do not follow the overall trend. This suggests that while discount is a factor that can influence total spending, there are also other aspects at play.

# Task-2
## Simple Linear Regression
In this case,  we are trying to predict the Total Amount Spent based on the Discount given:
1. The dependent variable is the Total Amount Spent. This is the variable that you’re interested in predicting.
2. The independent variable is the Discount. This is the variable used to make the prediction.
In general, the dependent variable is what you're interested in understanding or predicting, and the independent variable(s) are the factors you hypothesize will impact the dependent variable.
![image](https://github.com/anubhav1535/Regression-Analysis-in-Excel/assets/64795358/74a28e7a-870e-408d-91df-2d9203f121f0)

## Results
Interpreting the results of the linear regression analysis:

1. Slope (0.751). The slope of the regression line is approximately 0.751. This means that for each unit increase in Discount, the Total Amount Spent increases by about 0.751 units, assuming all other variables are held constant. This indicates that the Discount positively impacts the Total Amount Spent.
2. Intercept (127.293). The intercept of the regression line is approximately 127.293. This is the estimated value of the Total Amount Spent when the Discount is zero—assuming all other variables are held constant. It acts as a baseline value for the Total Amount Spent.
3. Prob (F-statistic) (also P-value). This is the p-value associated with the F-statistic. It tells us the probability of obtaining an F-statistic (3955.126) as extreme as ours if the null hypothesis is true—i.e., if the true slope is zero. A small p-value indicates strong evidence to reject the null hypothesis. Our p-value is 0.00, less than the commonly used significance level of 0.05, so we would reject the null hypothesis and conclude that our model provides a significant fit to the data. In other words, the Discount significantly explains the Total Amount Spent.
4. Correlation Coefficient (R, 0.406). The correlation coefficient (R-value) is approximately 0.406. This indicates a moderate positive linear relationship between the Discount and the Total Amount Spent. A positive R-value signifies that the Discount increases as the Total Amount Spent increases.
5. Coefficient of Determination (R-squared, 0.165). The coefficient of determination (R-squared) is approximately 0.165. This means that the Discount can explain about 16.5% of the variability in the Total Amount Spent. In other words, the Discount explains about 16.5% of the variation in the Total Amount Spent. The remaining 83.5% could be explained by other factors not included in the model.
   
So, while there’s a positive relationship between the Discount and the Total Amount Spent—and the Discount explains some of the variability in the Total Amount Spent—other factors are likely influencing the Total Amount Spent not captured in this simple linear regression model.

# Task-3
## Multiple Linear Regressions
Distributions:
1. Discount: This distribution appears right-skewed, with most of the values clustered on the left and a long tail on the right.
2. Product Price: This distribution also appears to be slightly right-skewed, though not as pronounced as the Discount.
3. Total Amount Spent: The distribution is noticeably right-skewed, similar to Discount.
   
Skewness Values:
1.Discount: 1.87
2.Product Price: 0.63
3.Total Amount Spent: 1.58

Recall the general guidelines for skewness:
1. If skewness is between -0.5 and 0.5, the distribution is approximately symmetric.
2. If skewness is between -1 and -0.5 or between 0.5 and 1, the distribution is moderately skewed.
3. If skewness is less than -1 or greater than 1, the distribution is highly skewed.
Based on the skewness values and visual inspection:

Both Discount and Total Amount Spent are highly skewed to the right, and log transformation could help in making their distributions more symmetric.
Product Price is moderately skewed to the right, and a log transformation might also be beneficial for this variable.
 

Regression Analysis
Given this analysis, it seems that log-transforming the variables could be beneficial in achieving more symmetrical distributions, especially for Discount and Total Amount Spent.
![image](https://github.com/anubhav1535/Regression-Analysis-in-Excel/assets/64795358/1e8598a6-e82f-49f2-bb9e-0cb53918b482)


# Task - 4
## Advance Multiple linear Regression
![image](https://github.com/anubhav1535/Regression-Analysis-in-Excel/assets/64795358/27378a31-cd25-4162-b187-481120c1e1e3)
1. R-squared. The R-squared value is 0.619, which means our model explains about 61.9% of the variation in the Log_Total Amount Spent. In other words, about 61.9% of changes in the Log_Total Amount Spent can be explained by differences in our independent variables.
2. F-statistic and Prob (F-statistic). The F-statistic is 2933, and the p-value is 0.00, less than 0.05. This indicates that our independent variables are statistically significant and contribute to predicting the Log_Total Amount Spent.
3. Coefficients and significance of coefficients (P>|t|).
   a. The coefficient for the constant term is 0.390.
   b. The coefficient of Log_Product Price is 0.946. This means that, on average, a 1% increase in the product price is associated with an approximately 0.946% increase in the Log_Total Amount Spent, holding all other variables constant.
   c. The coefficient of Log_Discount is 0.065. This suggests that, on average, a 1% increase in the discount is associated with an approximately 0.065% increase in the Log_Total Amount Spent, holding all other variables constant.
   d. Other variables are not significant predictors because their p-values are more than 0.05, including Age, Gender, User Region_North, User Region_South, User Region_West, Product Category_Clothing, Product Category_Electronics, Product Category_Home & Kitchen, and Product Category_Sports & Outdoors.
4. Regression Equation. Based on these results, the multiple linear regression equation is as follows:
log(Total Amount Spent)=0.3905+0.9468 × log(Product Price) + 0.0712 × log(Discount)+Other variables

The Trendy Shopper should then consider the following strategies:

Pricing Strategy. The company could continue to offer products at a higher price if the quality and brand justify the cost. This is supported by the positive coefficient for the Product Price, suggesting that customers are willing to pay more for the company's products.

Discount Strategy. The positive coefficient for Discount indicates customers will likely spend more when discounts are offered. The company could consider offering strategic discounts to drive sales and increase customers’ spending.

Customer Segmentation. The lack of significant results for Age, Gender, User Region, and Product Category suggests that these factors may not significantly influence the total amount spent. But the company should not disregard these factors entirely since they could be significant in other aspects of customer behavior, and further analysis could provide insights for better customer segmentation and targeted marketing strategies.

It's essential to note that these strategies are based on the regression analysis results. Other factors, such as market trends, competitive landscape, company objectives, and resources, should also be considered when making strategic decisions. Additionally, the relationships identified in the regression analysis are associative, not causal. It’s also vital to validate the model with new data and assess its predictive performance.

# Task-5
## Predictive Modelling
![image](https://github.com/anubhav1535/Regression-Analysis-in-Excel/assets/64795358/06b94e79-2b4e-4af7-8295-ef6578e827c9)
The scatter plot compares the actual and predicted values of the log-transformed Total Amount Spent. The x-axis displays the actual log values, while the y-axis shows the model's predicted log values. Each point on the plot corresponds to a transaction from the test dataset.

A perfectly accurate model would result in all points lying on a 45-degree line, indicating that the actual value matches the predicted value for each point. Deviations from this line suggest discrepancies between the model's predictions and the actual data.

The plot shows that the model's predictions are not perfectly aligned with the actual values. The scatter plot reveals some potential outliers, which could be unduly influencing the model's predictions. These could be transactions with exceptionally high or low values of Total Amount Spent that do not follow the same pattern as the rest of the data.

While the model does capture some of the relationships between the Discount, Product Price, and Total Amount Spent, the scatter plot and MSE (observed in output in Task 4) suggest that the model's predictive performance could be improved. This could be achieved by including additional predictors in the model, handling outliers, or using a more complex model that can capture non-linear relationships or interactions between variables.



