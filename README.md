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
![image](https://github.com/IshanSarkar/Retail-Company-2/assets/160044904/9c236769-8a95-4d09-83f3-2841acd83282)<br>\#### Insights:
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
















