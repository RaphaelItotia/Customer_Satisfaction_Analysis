# Hypothesis Testing for Customer Satisfaction after Service Improvement
Tool: Python

## Introduction:
In the fast-paced world of retail and service industries, customer satisfaction is key to maintaining loyalty and ensuring long-term success. Murima Superstores, a major retail chain in Kenya, recently implemented service improvements aimed at addressing customer concerns regarding long checkout lines, insufficient product variety, and poor customer service.
The service improvements involved:
  1.	Introducing new staff training programs to improve employee interactions with customers.
  2.	Deploying upgraded IT systems to reduce checkout times.
     
After these changes, the company decided to measure the impact on customer satisfaction. To ensure they were making data-driven decisions, they collected customer satisfaction data both before and after these improvements. The goal was to determine whether the service upgrades significantly improved customer satisfaction levels.

## Objective:
This project aimed to use hypothesis testing(paired t-test) to determine if there is a statistically significant improvement in customer satisfaction after the service improvements at Murima Superstores.

## Dataset Overview:
The dataset consists of feedback from 200 customers, each surveyed both before and after the service improvements. The key attributes include:
-	`Customer_ID`: Unique identifier for each customer.
-	`Customer_Age`, `Gender`, `Income Level`: Customer demographics.
-	`Frequency_of_Purchase`: How often each customer shops at Murima Superstores.
-	`Product/Service Purchased`: The product or service the customer interacted with.
-	`Satisfaction_Before`: Customer satisfaction rating before the improvements (on a scale of 1 to 10).
-	`Satisfaction_After`: Customer satisfaction rating after the improvements (on a scale of 1 to 10).
-	`Customer Feedback (Before/After)`: Written feedback from customers.
-	`Employee Interaction Rating`: How customers rated their interactions with staff (on a scale of 1 to 10).
-	`Region`: The location of the store where the customer shopped (Nairobi, Rift Valley, Western, Eastern, or Central).
-	`Customer Loyalty`: Whether the customer is part of the loyalty program.
  
## Step-by-Step Approach:
--------------

### 1. Data Collection:
The first step in the process was collecting customer satisfaction data at two points:
  -	Before the service improvements: Customers were surveyed about their satisfaction levels (on a scale of 1 to 10) regarding overall service quality.
  -	After the service improvements: The same customers were surveyed again to capture any changes in satisfaction levels post-improvement.
    
The dataset includes additional attributes like age, gender, income level, frequency of purchase, and whether the customer is part of a loyalty program.
N/B: For my case, I generated the [data]() using [Python]() for practice. I ensured it has no inconsistencies hence skipping the data cleaning step.

### 2. Descriptive Statistics:
Next, we calculated some descriptive statistics to better understand the data:
  -	Mean satisfaction ratings before the improvements. This gives us a baseline to compare with the after-data.
  -	Mean satisfaction ratings after the improvements.
  -	Standard deviation to understand the variability of the satisfaction scores.
    
![descriptive]()

By looking at these numbers, we can get an initial idea of whether the improvements had an impact. However, this alone isn't enough to draw a conclusion.

### 3. Visualization of Satisfaction Scores:
To visualize the distribution of satisfaction ratings before and after the improvements, we used boxplots to compare the two sets of data.(before and after)

![boxplot]()

This helps us visually assess whether the overall distribution of satisfaction ratings shifted in a positive direction after the improvements.

### 4. Hypothesis Testing:
Defining the Hypotheses:
  -	Null Hypothesis (H0): There is no significant difference in customer satisfaction before and after the service improvements.
    
\[H_0:\mu_{\text{before}} = \mu_{\text{after}} \]

  -	Alternative Hypothesis (H1): There is a significant increase in customer satisfaction after the service improvements.
    
\[H_1:\mu_{\text{before}} < \mu_{\text{after}} \]

We conducted a paired t-test because the same customers are surveyed both before and after the improvements, making the data dependent.
### 5. Conducting the Paired T-Test:
We calculated the difference between the satisfaction ratings before and after for each customer. Then, computed the mean of the differences and applied the paired t-test formula.

![paired]()

### 6. Interpretation:
   - t-statistic: - 0.08758231902891955
   - p-value: 0.9302967239958176
     
Since the t-statistic is close to zero it indicates that there is very little difference between the means of the two groups (satisfaction ratings before and after the service improvements). In this case, the negative value which is very close to 0, indicates that there is little to no difference between the two means.

Since the p-value is greater than 0.05, we fail to reject the null hypothesis and conclude that the observed differences in customer satisfaction(before and after improvements) at Murima Superstores are likely due to chance. 

----------
### 7. Conclusion:
The analysis indicates that the service improvements made by Murima Superstores did not lead to a statistically significant change in customer satisfaction. Since the p-value is high, we cannot conclude that the improvements had a meaningful impact on customer experiences.
Actionable Recommendations:
-	Monitor Key Performance Indicators (KPIs): Continuously monitor key metrics related to customer satisfaction. Establish regular check-ins to gauge the effectiveness of any ongoing improvements.
-	Enhance Customer Engagement: Foster better communication with customers. Regularly seek feedback through surveys or social media, and ensure that customers know their input is valued and will lead to improvements. Consider implementing a loyalty program to stimulate regular feedback.
-	Test Additional Improvements: Experiment with different types of service improvements, such as faster checkout systems, increased product availability, or better store layout. Conduct small-scale pilot programs before implementing widespread changes and measure their impact on customer satisfaction.
  
By using data-driven insights, Murima Superstores can optimize their services and have high customer satisfaction levels, helping them stay competitive in Kenya’s retail market.
