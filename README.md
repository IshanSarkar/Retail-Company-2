# Data Analysis of Multinational Retail Corporation
- Language: Python
- Libraries: NumPy, Pandas, Matplotlib, Seaborn, Math, Norm

## Business Problem:
The Management team of the company wants to analyze the customer purchase behavior (specifically, purchase amount) against the customer’s gender and the various other factors to help the business make better decisions. They want to understand if the spending habits differ between male and female customers and so on.

## Dataset Characteristics
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/9065fa7b-d78c-42fe-9c99-626f454f9457)<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/a2c77a5a-60a7-40a6-8719-3fee5cc40471)![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/179520d0-75b5-4087-8cfa-181132a6ab0b)
<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/f2db8693-1c69-4519-8d8b-3a2b5c294dd6) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/fd0672c9-56f3-46a6-9cbe-121f25c3d70f) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/53ed1beb-6cc9-4227-adc0-abc0a6d5bb6f) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/a341de8c-a468-4933-823b-c1ce656baaad) <br>
**Given the description and data frame, we can conclude the below details:**
- **Continuous Variables:**
  - Purchase (Purchase Amount)
- **Categorical Variables:**
  - Age (Age in bins, although age itself is a continuous variable but here it is represented in bins)
  - User_ID (User ID)
  - Product_ID (Product ID)
  - Gender (Sex of User: M & F)
  - City_Category (Category of the City - A, B, C)
  - Marital_Status (Marital Status: 0 & 1)
  - Occupation (Occupation, assuming it represents numerical form)
  - Stay_In_Current_City_Years (Number of years stay in the current city, Now there is '4+' mentioned along with (0, 1, 2, 3) but not 4 which means customers living for either 4 years or more than 4 years or both are put in '4+', so we will convert it to 4 for better analysis with keeping in mind the condition)
  - Product_Category (Product Category, assuming it's represented as numerical form)
## Null Values and Outliners
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/5f7b3d14-ccc0-4de6-a4e4-bea58212296b)<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/69494118-ce9d-426a-b896-74732be15a59)![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/8802cb99-0aee-41dc-b4c3-61a4c43da212)

#### Insights:
- The highest peak is around a purchase price of 5000-7500, indicating that this is the most common purchase price range.
- There is another noticeable peak around 15000, suggesting another common price point for purchases.
- It seems that this could be a multimodal distribution, which indicates that there are different groups within the data. Each mode could potentially represent a different group. The prominent peaks could be due to popular products priced at those specific amounts or it could indicate preferred spending amounts by customers.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/9c236769-8a95-4d09-83f3-2841acd83282)<br>
#### Insights:
- **Gender:** The purchase amounts are relatively similar between genders F and M, with M having a slightly wider range.
- **City Category:** City category B has the highest median purchase amount, followed by C and A. The interquartile range is similar across all city categories.
- **Stay in Current City Years:** There is no significant difference in purchase amounts based on the number of years stayed in the current city. All categories have a similar median and interquartile range.
- **Marital Status:** Both categories (0 and 1) have almost identical medians and interquartile ranges, indicating marital status does not significantly impact purchase amounts.

#### Analysis:
- The purchase amounts are not significantly influenced by the gender, city category, stay in current city years, or marital status of the customers. The distributions are quite similar across all these categories. This could suggest that these factors do not play a major role in determining the purchase amounts.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/75d41964-60a2-41f0-ab0b-c436f86e9f7b) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/dbe905c7-4e40-4c50-9577-86ba5224548b)<br>

#### Insights:
- **Age Group:** The majority of individuals are in the “26-35” age group, followed by the “18-25” and “36-45” groups. This suggests a younger demographic is being represented or targeted.
- **Occupation:** Occupation “4” has the highest count, followed by “0” and “7”. It indicates that these occupations are more common or have higher data entries in this particular dataset.
- **Product Category:** Categories “5”, “1”, and “8” have higher counts, indicating these products are popular or commonly purchased.

#### Analysis:
The data represents a younger demographic, with certain occupations being more prevalent. The product categories with higher counts could be the ones that are more popular or commonly purchased among these individuals. This information could be useful for targeted marketing or product development strategies aimed at these specific demographics.<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/5bf42d94-5eab-4e68-ac96-c9779c8a12ae)![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/881aafba-1b06-40f4-96cf-00f2b7c70858)<br>

#### Insights:
- **Gender Distribution:** The majority of customers are male, making up 75% of the total.
- **Age Distribution:** The largest age group among the customers is 26-35 years old, accounting for 40% of the total.
- **City Category:** Most customers belong to city category B, which constitutes 42% of the total.
- **City Tenure:** The largest segment of customers have a city tenure of one year, making up 35% of the total.
- **Marital Status:** The majority of customers are unmarried, accounting for 59% of the total.
- **Income Group:** The customer base is evenly distributed between the low and medium-income groups, each constituting about 40%.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/a42022e3-cba5-4827-a254-d2cd2d99b0fe)<br>

#### Insights:
- The dataset contains information on over 550,000 unique users.
- Users have varying occupations, with an average occupation value of around 8.08 and a standard deviation of approximately 6.52.
- Marital status is mostly unmarried, with an average value of about 0.41 and a standard deviation of around 0.49.
- Purchases span across different product categories, with an average category value of approximately 5.40 and a standard deviation of about 4.0.
- Purchase amounts vary widely, with an average of around 9255.02 and a standard deviation of approximately 5000.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/7e0fdb83-7fd4-47ef-9c58-2ac946846605) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/5cdf9305-eda0-4af0-9d4f-67648d6067f8) <br>

#### Insights:
- **Occupation and Marital_Status:** These two variables have a very weak positive correlation of 0.025. This suggests that there’s almost no linear relationship between a person’s occupation and their marital status.
- **Stay_In_Current_City_Years and Purchase** have a very weak positive correlation of 0.0055, suggesting that the length of stay in the current city has a negligible effect on Purchase.
- **Occupation and Product_Category:** These variables have a negligible negative correlation of -0.0072. This indicates that there’s no significant linear relationship between a person’s occupation and the product category they choose.
- **Occupation and Purchase:** These variables have a very weak positive correlation of 0.021. This suggests that a person’s occupation has very little impact on their purchasing behavior.
- **Marital_Status and Product_Category:** These variables have a very weak positive correlation of 0.019. This suggests that a person’s marital status has very little impact on the product category they choose.
- **Marital_Status and Purchase:** These variables have an almost non-existent negative correlation of -0.0011. This indicates that a person’s marital status has almost no impact on their purchasing behavior.
- **Product_Category and Purchase:** These variables have a moderate negative correlation of -0.37. This suggests that as the product category number increases, the purchase amount tends to decrease.

In **conclusion**, none of the variables have a strong correlation with each other based on the provided data. The strongest relationship is a moderate negative correlation between Product_Category and Purchase.<br>
## Data Exploration
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/c50306ea-df9d-4e02-9d2f-4caedeee3878) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/646625fb-8d33-4efc-aa32-f1e50288777b) <br>
#### Insignts and Analysis:
- **Age Distribution:** The majority of customers fall within the age groups of 26-35 and 18-25, each contributing around 40% and 18% respectively to the total customer base.
- **Product Category Preference by Age Group:**
    - Product Category 1 and 5 seems to be popular across all age groups (25.52% and 27.43%), with the highest proportion of customers from age 26-35 (41.49% and 40.72% respectively).
    - Product Category 8 also sees notable interest which is 20.71% of total customers, with the highest proportion of customers from age 26-35 (38.84% of all the age groups in that product category).
    - Certain product categories, like 9, 14, 17, etc., have very low overall proportions across all age groups which are 00.07%, 00.27%, 00.10% respectively.
- **Age Group Analysis:**
    - Younger age groups (0-17, 18-25) tend to have a higher proportion (Total of 20.86%) of customers compared to older age groups in most product categories.
    - Middle-aged groups (36-45, 46-50, 51-55) show relatively consistent proportions across various product categories (Ranges from 00.09%-26.70%, 00.07%-26.70% and 00.07%-26.70% respectively).
    - The older age group (55+) tends to have lower proportions which is 3.9% across all product categories compared to other age groups.
- **Overall Trend:** There's a gradual decline in proportions of customers as age increases, indicating that younger demographics are more actively engaged in purchasing across various product categories.
- **Implications:** 
    - Marketing efforts for products in Category 1 could be tailored more towards the 26-35 age group.
    - Products in Category 5 seem to appeal to a wide range of age groups, suggesting potential broad market appeal or the need for varied marketing approaches targeting different age groups.
    - Product categories with consistently low proportions across all age groups may require further analysis to understand customer preferences or may not align with the current customer base.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/16508d01-f795-40e6-adba-bd3db463b375)<br>
#### Insights and Analysis:
- **Higher Median Purchase for Married Individuals Across All Age Groups:** Married individuals consistently exhibit higher median purchase amounts compared to unmarried individuals across all age groups. This indicates that, on average, married individuals tend to spend more than their unmarried counterparts within each age group.
- **Wider Spread of Purchase Amounts for Married Individuals:** The spread of purchase amounts, as depicted by the height of the boxes and whiskers in a box plot, is wider for married individuals. This suggests that there is greater variability in purchase behavior among married individuals, with some spending significantly more and others spending significantly less compared to unmarried individuals.
- **Highest Purchase Values in the Age Group 26–35 Regardless of Marital Status:** The age group 26–35 consistently demonstrates the highest purchase values irrespective of marital status. Additionally, there's not a significant disparity in purchase values between different marital statuses within each age group, indicating that age plays a more prominent role in purchase behavior than marital status within these age brackets.
- **Significantly Lower Purchase Values in the Age Groups 0–17 and 55+:** The age groups 0–17 and 55+ exhibit notably lower purchase values compared to other age groups. This observation highlights certain demographic segments where purchasing activity may be lower, potentially due to factors such as dependence on others for finances in the case of minors or fixed incomes in retirement for older individuals.
- **Overall Implications:** While married individuals tend to have higher median purchases across all age groups, the variability in their purchase behavior suggests a more diverse spending pattern compared to unmarried individuals. Age group 26–35 emerges as a significant demographic segment for high purchase activity, regardless of marital status, indicating a prime target for marketing efforts.
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/880d2607-f172-4fef-952e-7db644856d8f) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/7867f713-9054-4386-9ec3-1cd4508752a5) <br>
#### Insights:
- **Product Category 5** holds the highest overall proportion of purchases, accounting for 27.44% of all purchases. Both male and female customers significantly contribute to this category, with females representing 27.80% and males 72.19% of its distribution. **Product Category 1** closely follows, representing 25.52% of all purchases, with a relatively higher contribution from male customers (82.31%). **Product Category 8** also exhibits notable popularity, contributing 20.71% of all purchases, with a higher proportion of male customers (70.54%).
- Male customers demonstrate a stronger preference for Product Categories 1, 5, and 8, representing 27.89%, 26.30%, and 19.40% respectively of the total male customer distribution. Conversely, female customers exhibit relatively similar preferences, with percentages of 18.28%, 30.89%, and 24.70% for the same categories out of the total female customer base.
- Certain product categories (e.g., Categories 9, 17, 18, 19, and 20) show relatively low proportions of purchases for both genders, suggesting that these categories may not be as popular among either male or female customers (0.07%, 0.10%, 0.56%, 0.29%, and 0.46% respectively out of the total customer distribution).

#### Overall Metrics:
- Product Category 5 maintains the highest proportion of purchases, followed closely by Category 1 and then Category 8 for both male and female customers.
- Male customers contribute more to the overall purchases compared to female customers across all product categories, representing a significant majority of 75.31% of the total customer base.
## Effect of Different Genders on Purchase
As we know, the CLT states that, regardless of the shape of the population distribution, the distribution of sample means will approach a normal distribution as the sample size increases, and by applying the CLT, we can assume that the distribution of sample means is approximately normal, which allows us to make inferences about the population parameter (in this case, the average amount spent per gender) using the properties of the normal distribution. <br>
**For the entire population of Males:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/a66b5a88-7c88-4d0f-87ab-b50e589a674d) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/01ffc2b9-3596-442d-b0ea-0c36ea1406d1) <br>
**For the entire population of Females:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/586935d0-1044-4cf5-9f36-49f1b90ea866) ![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/97c445db-5062-43f2-88e2-7f835f734689) <br>
**Taking the sample size of 300 for each gender** <br>
**For male:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/cb686cc6-70d1-458c-ba5f-9ff608fab614) <br>
So, to minimize the variation, we are conducting 10,000 iterations of samples, each with a size of 300. By doing so, we obtain a normal distribution of male purchase samples. <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/0774c67a-0066-4a76-b250-60ee5a3a935c) <br>
**For Female:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/aa011fe6-79ef-4ad8-8e66-cd3f26bf1b3e) <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/fba0f46c-8560-4fd7-aff8-e63b28e29bcb) <br>
**Taking the sample size of 3000 for each gender <br><br>
For male:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/3f1fb990-d627-4514-aad3-3b61ecf0c2c6) <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/33097cc8-5af7-4ee4-bd2c-3732710a2020) <br>
**For Female:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/306b27d4-d3d0-4c3a-a5b0-edcf8f6ff01a) <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/0e644ac5-71c2-4db8-8eda-b16461a0e8db) <br>
**Taking the sample size of 30000 for each gender <br><br>
For male:** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/6954ece2-ad83-49a0-b946-781008ca01c0)<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/86d43f50-988f-459d-8d89-02eb7e601789)<br>
**For Female:**<br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/5e8b879a-68d6-46d3-aed8-ca8422a81c28) <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/3ebd1e7d-68d1-4fff-93db-2c6a0e710ec7) <br>
### Summary:
Average amount spent by Male (total population) at 95% confidence interval is (9413.93, 9442.81)<br>
Average amount spent by Female (total population) at 95% confidence interval is (8701.02, 8751.48)<br>
Average amount spent by Male of sample size 300 at 95% confidence interval is (9400.80, 9466.40)<br>
Average amount spent by Females with a sample size of 300, the 95% confidence interval is (8700.84, 8761.98)<br>
Average amount spent by Males with a sample size of 3000, the 95% confidence interval is (9425.24, 9431.8).<br>
Average amount spent by Females with a sample size of 3000, the 95% confidence interval is (8723.16, 8729.28).<br>
Average amount spent by Males with a sample size of 30000, the 95% confidence interval is (9427.88, 9428.52)<br>
Average amount spent by Females with a sample size of 30000, the 95% confidence interval is (8726.37, 8726.91)<br>

#### Insights:
- The confidence interval computed using the entire dataset is wider for females compared to males. This could be due to several factors including differences in variability of spending habits between genders within the population. A wider interval suggests more uncertainty in estimating the true population mean for females compared to males.
- The width of the confidence interval is inversely proportional to the square root of the sample size. This is because larger sample sizes provide more precise estimates of the population parameter, resulting in narrower intervals.
- The confidence intervals for different sample sizes overlap. This is expected because they are all estimating the population mean with a certain level of confidence (95% in this case), and these estimates are subject to some degree of uncertainty. However, as the sample size increases, the intervals become narrower and may overlap to a lesser extent.
- As the sample size increases, the shape of the distribution of the means becomes more normally distributed, according to the Central Limit Theorem. This means that the distribution of the sample means approaches a normal distribution, regardless of the shape of the original population distribution.

#### Conclusion:
- **Male vs. Female Spending:**
    - In all sample sizes (300, 3000, and 30000), the average amount spent by males tends to be higher than that of females.
    - For example, in the smallest sample size of 300, the average amount spent by males ranges from approximately 9400.80 to 9466.40, while for females, it ranges from about 8700.84 to 8761.98.
- **Confidence Interval Overlap:**
    - Although the averages for males are consistently higher than those for females, there is some overlap in the confidence intervals, especially in the larger sample sizes.
    - This overlap suggests that while there may be a trend indicating that males tend to spend more than females on average, it's not an absolute rule. There are instances where females spend amounts that fall within the range of what males spend.

#### Summary
While the data suggest a tendency for males to spend more on average compared to females, it's not a definitive conclusion. <br>

## Effect of different Marital Status on Purchase
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/c0217052-3ee8-4136-8680-e658dbb85bbd) Not Married-Entire Dataset <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/2aad55c5-35bb-499f-96f9-197c60e70999) Married-Entire Dataset <br>

### Summary:
- The average amount spent by Not-Married at 95% confidence interval is (9240.3, 9274.74)
- The average amount spent by Married at 95% confidence interval is (9230.82, 9272.04)
- The average amount spent by Not-Married of sample size 300 at 95% confidence interval is (9219.17, 9284.77)
- The average amount spent by Married of sample size 300 at 95% confidence interval is (9218.45, 9284.27)
- The average amount spent by Not-Married of sample size 3000 at 95% confidence interval is (9254.85, 9261.35)
- The average amount spent by Married of sample size 3000 at 95% confidence interval is (9246.94, 9253.38)
- The average amount spent by Not-Married of sample size 30000 at 95% confidence interval is (9257.22, 9257.84)
- The average amount spent by Married of sample size 30000 at 95% confidence interval is (9251.17, 9251.79)

#### Insights:
- The confidence interval computed using the entire dataset is slightly wider for the “Not-Married” group. This could be due to a greater variability in the amount spent within this group, which would result in a wider confidence interval.
- The width of the confidence interval is inversely proportional to the square root of the sample size. As the sample size increases, the width of the confidence interval decreases. This is because larger samples tend to provide a more accurate estimate of the population parameter, hence the confidence interval becomes narrower.
- The confidence intervals for different sample sizes do overlap. This suggests that the difference in the average amount spent between the “Married” and “Not-Married” groups is not statistically significant at the 95% confidence level.
- As the sample size increases, the distribution of the means becomes more narrowly spread around the population mean. This is due to the Central Limit Theorem, which states that the distribution of sample means approximates a normal distribution as the sample size gets larger, regardless of the shape of the population distribution. This is why the confidence intervals become narrower with increasing sample size.

#### Conclusion:
- **For Not-Married individuals:**
    - Across all sample sizes (300, 3000, and 30000), the confidence intervals for the average amount spent are fairly wide but consistently overlap.
    - This indicates that there is no significant difference in the average amount spent between not-married individuals across different sample sizes.
- **For Married individuals:**
    - Similar to the not-married group, the confidence intervals for the average amount spent overlap across different sample sizes.
    - Again, this suggests that there is no significant difference in the average amount spent between married individuals across different sample sizes.

#### Summary:
Based on the provided data, there doesn't appear to be a significant difference in the amount spent based on marital status. Both not-married and married individuals seem to spend similar amounts, as indicated by the overlapping confidence intervals across different sample sizes.

## Effect of different Age Groups on Purchase
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/6583234e-1759-4f6b-8b1a-e8cc86c2ad92) <br>
The average amount spent at a 95% confidence interval on the entire dataset by:
- 0-17 Age Group: (8844.36, 9006.72)
- 18-25 Age Group: (9133.02, 9195.36)
- 26-35 Age Group: (9224.07, 9265.81)
- 36-45 Age Group: (9291.37, 9350.41)
- 46-50 Age Group: (9153.24, 9243.82)
- 51-55 Age Group: (9469.13, 9570.44)
- 55+ Age Group: (9253.36, 9386.16)
**Taking the sample size of 300 for each Age Group** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/7b3797e7-0dfa-4c2b-8dbb-243323922f15) <br>
The average amount spent by each Age Group of sample size 300 at a 95% confidence interval is:
- 0-17: (8896.81, 8962.29)
- 18-25: (9133.73, 9198.73)
- 26-35: (9208.61, 9274.11)
- 36-45: (9282.22, 9347.56)
- 46-50: (9169.05, 9233.43)
- 51-55: (9493.14, 9558.8)
- 55+: (9285.52, 9349.32)
**Taking the sample size of 3000 for each Age Group** <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/9ce2b065-4f12-4ad4-948f-8bc0bd924e45)<br>
The average amount spent by each Age Group of sample size 3000 at 95% confidence interval is:
- 0-17: (8922.71, 8928.65)
- 18-25: (9160.72, 9167.22)
- 26-35: (9241.77, 9248.29)
- 36-45: (9315.63, 9322.03)
- 46-50: (9196.21, 9202.39)
- 51-55: (9516.64, 9522.98)
- 55+: (9316.52, 9322.52)
We cannot take the sample size of 30000 as the 0-17 Age Group's population size is 15102. So, we are taking a 10000 sample size. <br>
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/101d57f7-3dbc-45cc-9803-127e32c3cd35) <br>
The average amount spent by each Age Group of sample size 10000 at 95% confidence interval is:
- 0-17: (8925.2, 8926.36)
- 18-25: (9163.62, 9165.48)
- 26-35: (9244.57, 9246.49)
- 36-45: (9319.49, 9321.35)
- 46-50: (9197.64, 9199.36)
- 51-55: (9519.0, 9520.68)
- 55+: (9319.55, 9320.95)
#### Insights:
- The confidence interval computed using the entire dataset is wider for the age groups 0-17, 55+, and 51-55 respectively in decreasing order. This is because of the wider Age Groups result in higher uncertainty about the true population parameter, leading to wider confidence intervals. 
- The width of the confidence interval is inversely proportional to the square root of the sample size. As the sample size increases, the width of the confidence interval decreases. This is because larger sample sizes provide more information about the population parameter, reducing the uncertainty and resulting in narrower intervals.
- The confidence intervals for different sample sizes overlap. However, as the sample size increases, the overlap becomes smaller because the confidence intervals become narrower due to decreased uncertainty.
- As the sample size increases, the shape of the distribution of the means approaches a normal distribution, regardless of the shape of the original distribution. This is described by the Central Limit Theorem (CLT). With smaller sample sizes, the distribution of the means may appear more skewed or varied, but as the sample size increases, the distribution becomes more symmetrical and closely resembles a normal distribution.
#### Overall Trends:
- **0-17 Age Group:** The average amount spent remains relatively stable across different sample sizes, with slight fluctuations within a narrow range.
- **18-25 Age Group:** Similar to the 0-17 age group, the average amount spent shows minimal variation across different sample sizes.
- **26-35 Age Group:** The average amount spent slightly increases with age within this group, showing a gradual upward trend.
- **36-45 Age Group:** The trend of increasing the average amount spent continues, with slightly larger confidence intervals compared to the previous groups.
- **46-50 Age Group:** There's a slight decrease in the average amount spent compared to the preceding age group, but the difference is not significant.
- **51-55 Age Group:** The average amount spent shows a notable increase compared to the 46-50 age group, indicating a potential increase in spending as individuals move into this age bracket.
- **55+ Age Group:** The trend of increased spending appears to plateau within this age group, with relatively consistent average amounts spent across different sample sizes.
#### Explanations:
- The observed trends could be attributed to various factors such as income levels, lifestyle changes, financial responsibilities, and priorities associated with different age groups.
- Younger age groups (0-25) might have relatively lower average spending due to limited disposable income, while older age groups (especially 51-55 and 55+) might have higher average spending due to increased financial stability, savings, and potentially higher discretionary income.
- The slight fluctuations within each age group across different sample sizes suggest inherent variability in spending behavior within each demographic, which could be influenced by individual preferences, socioeconomic factors, and other external variables.
#### Summary:
Age appears to have a nuanced effect on the amount spent, with some age groups showing consistent spending patterns across different sample sizes, while others exhibit slight variations or trends of increasing or decreasing spending with age.

## Report:
### Overall Analysis:
- **Purchase Behavior Patterns:**
    - The purchase price distribution indicates multimodality, suggesting distinct customer groups or popular price points.
    - Gender, city category, and city tenure show no significant impact on purchase amounts, while marital status also has minimal influence.
    - Age group and occupation shed light on the demographic representation and common occupations within the dataset.
- **Demographic Trends:**
    - Majority of customers are male, aged 26-35, residing in city category B, with one year city tenure, and unmarried.
    - The dataset predominantly represents younger age groups, with a concentration in certain product categories like 5, 1, and 8.
- **Purchase Behavior Analysis:**
    - Married individuals tend to spend more across all age groups compared to unmarried individuals.
    - Age plays a more significant role than marital status in determining purchase behavior, with the age group 26–35 consistently exhibiting the highest purchase values.
    - Certain demographic segments, such as minors and older individuals, exhibit lower purchasing activity.
- **Product Category Preferences:**
    - Product categories 5, 1, and 8 are the most popular, with gender differences in preference observed.
    - Some categories have low overall proportions, indicating less popularity among customers.
- **Statistical Analysis:**
    - On average, males tend to spend more than females across all sample sizes. However, there is overlap in the confidence intervals, indicating variability within the data. While there's a trend suggesting higher spending by males, it's not an absolute rule, and there are instances where females spend amounts comparable to males.
    - For both not-married and married individuals, there is no significant difference in the average amount spent across different sample sizes. Overlapping confidence intervals suggest similar spending patterns regardless of marital status.
    - Spending behavior varies across age groups. Younger age groups (0-25) typically have lower average spending due to limited disposable income, while older age groups (especially 51-55 and 55+) may have higher spending due to increased financial stability. However, there are fluctuations within each age group across different sample sizes, indicating variability influenced by individual preferences and external factors.
### Over Recommendations:
- **Price Point Optimization:** Considering the multimodal distribution of purchase prices, focus on product offerings within the most common price ranges (5000-7500 and 15000) to cater to different customer segments.
- **Targeted Marketing by Demographics:** While gender and marital status don't significantly impact purchase amounts, tailor marketing strategies based on city category and age groups. City Category B appears to have the highest median purchase amount, and the majority of customers are in the 26-35 age group.
- **Product Category Focus:** Concentrate on popular product categories such as 5, 1, and 8, which have higher counts and purchase proportions. Additionally, consider the differential preferences between genders for certain product categories to optimize marketing efforts.
- **Age Group Insights:** Recognize the dominance of the 26-35 age group and adjust marketing strategies accordingly. Additionally, be aware of the lower purchase values in the age groups 0-17 and 55+, and consider targeted campaigns to address these segments. Consider offering promotions or discounts aimed at younger age groups to attract more budget-conscious consumers.
- **Marital Status Impact:** Married individuals consistently exhibit higher median purchase amounts across all age groups. Consider tailoring marketing efforts to appeal to this demographic, while also acknowledging the wider spread of purchase amounts among married individuals.
- **Gender Impact:** Develop targeted marketing campaigns that appeal to both male and female demographics. While males tend to spend more on average, it's important not to overlook the purchasing power of females.
