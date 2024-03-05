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



















