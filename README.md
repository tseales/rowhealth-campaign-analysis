# Row Health Campaign Performance Analysis

## About Our Company & Data
Founded in 2016, Row Health is a medical insurance company serving thousands of customers throughout the United States. In 2019, they launched a new set of marketing campaigns spanning topics like Health Awareness, Covid Awareness, and Health Tips. Now that they’re strategizing their marketing budget for the forthcoming year, the company would like to attain a better understanding of the effectiveness of these various types of campaigns, and how they relate to signups and subsequent patient claims. This project conducts a focused analysis on the aforementioned metrics, campaign costs, CTR, MoM & YoY frequency of claims. The garnered insights will allow the Marketing team to make advantageous data-driven decisions for increasing campaign effectiveness. 
</br></br>
**Note:** *24 campaigns did not have any associated customers. Analysis was done on 33/57 campaigns.*

The ERD can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/f4ac1220566dfc81dff4621e1ab8e0c0d74618e0/artifacts/ERD.md). An Excel workbook can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/f4ac1220566dfc81dff4621e1ab8e0c0d74618e0/artifacts/Row%20Health%20Data.xlsx). A Jupyter Notebook with EDA completed in Python, utilizing Pandas, can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/c99580226f8eecbb4127696215eb2edf0f78d7ea/artifacts/rowhealth-camp-performance-eda.ipynb)

## Interactive Tableau Dashboard
An interactive *Tableau Public* dashboard can be found [here](https://public.tableau.com/views/RowHealthCampaigns/Dashboard2?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link). This dashboard focuses on Campaign performance metrics such as CTR, Signup Rate, Cost-per-Signup - enabling stakeholders to garner insights on the selected types of campaigns. 

![row-dash](https://github.com/user-attachments/assets/57c13a51-5b57-45e7-be77-2821e52846d6)
</br></br>

## Summary of Insights
<details>
<summary>Stakeholder Initial Questions</summary>
  1. How does the cost of a campaign relate to the number of signups?</br> 
  2. Which campaigns resulted in the highest number of signups?</br>
  3. How does the type of campaign correlate with the type of plan chosen?</br>
  4. What do claims look like for customers acquired through certain campaign groupings?
</details>

Conducting an analysis on 66k+ `customers`, `claims`, `campaigns` records for the years 2019-2023, key insights in the following areas were made:
### 1) Campaign Costs & Signups
- There is no significant relationship between the cost of a campaign and the number of signups.
- The top 5 highest-signup campaigns *(see section 2)* have an avg. cost-per-signup of $0.59; 199% less than the overall avg. of $203.91.
- Campaigns of type 'Covid Awareness' & 'Offer Announcement' have the largest average cost-per-signup, at $537.25 and $411.94 respectively - surpassing the overall average of $203.91. In relation to costs, 'Covid Awareness' is 2nd highest, at $6.6K; 'Offer Announcement' in 5th, at $4.2K.
  - 7 Campaigns (21.2%) are above the avg. cost/signup.
  - 26 Campaigns (78.8%) are below the avg. cost/signup.
- 'Customer Testimonial' is the highest-costing campaign with a total of $7.2K &ndash; 4th in total number of signups. The following chart depicts types of campaigns with their associated costs & signups, from most-to-least expensive:

![campaign-cost-vs-signup-barchart](https://github.com/user-attachments/assets/bf71ff58-3376-459f-9a20-5c0c2c886f6e)
</br></br>

### 2) Campaign Signups & Plans
- 'Product Promotion' encapsulates the highest number of signups (5581), followed by 'Health Awareness' (3395) and 'Policy Information' (2987).
- The 'Silver' plan unequivocally makes up the largest proportion of each campaign-type's distribution, constituting 86% of all plans. In most cases (~71%), this is followed by the order of: 'Gold', 'Bronze', 'Platinum'.
- The following campaigns *(in descending order)* have the highest number of signups:
  - CAM031 : 3534 signups
    - Type: Product Promotion
    - Category: #CoverageMatters
  - CAM018 : 3279 signups
    - Type: Health Awareness
    - Category: Health For All
  - CAM030 : 2743 signups
    - Type: Policy Information
    - Category: #HealthyLiving
  - CAM004 : 1546 signups
    - Type: Customer Testimonial
    - Category: Compare Health Coverage
  - CAM006 : 1273 signups
    - Type: Product Promotion
    - Category: Compare Health Coverage

![plan-proportion](https://github.com/user-attachments/assets/7e8e1c6c-4c5f-4af8-ac75-e75d7b4cceae)
</br></br>

### 3) Frequency of Claims
- 'Customer Testimonial' types of campaigns encapsulate the highest avg. claim amounts, at $457.35. This is followed by 'Policy Information' and 'Product Promotion', at $248.57 & $236.55, respectively.
  - Digging deeper into the association of campaign types & categories, the following *Type:Category* groupings have above average </br> (> $267.43) claim amounts:
    - Customer Testimonial : Compare Health Coverage
    - Covid Awareness : Compare Health Coverage
    - Health Tips : Tailored Health Plans
    - Customer Testimonial : Preventive Care News
    - Covid Awareness : #InsureYourHealth
  - Of the top 10 groupings with the highest *total* claim amounts, 80% fell below the average, while the following 'Customer Testimonial' groupings did not:
    - Customer Testimonial : Compare Health Coverage *(Ranked 1st)*
    - Customer Testimonial : Preventive Care News *(Ranked 9th)*
- There is a general uptick in claims throughout 2019-2021, likely due to the inception of the COVID-19 pandemic.
  - 'Health Awareness' has the highest YoY frequency of claims, while 'Offer Announcement' is consistently the lowest.

![yrly freq](https://github.com/user-attachments/assets/36b00dc6-c51a-4b62-afac-29604387d8ed)
</br></br>

## Recommendations
<details>
<summary>1. Investigate why customers are primarily opting for the 'Silver' plan, over other choices.</summary></br>
Understanding why customers are opting for a specific plan over others, will provide further insights into the actions taken by customers and provide further direction on the constitution of plans, depending on the strategy of the Marketing team. What criterion encourage a customer to select a specific plan - monthly costs, deductibles, etc.?
</details>
<details>
<summary>2. Reduce campaigns related to types 'Customer Testimonial' and 'Covid Awareness'.</summary></br>
As the costs of these campaigns are relatively high, without a large return in number-of-signups received, reallocating funds to more lucrative types will ensure a healthier cost:signup ratio. Further investigation into the context of what guides a customer to signup with an associated type of campaign is also advised. Campaign types of 'Product Promotion' is recommended as an option for receiving reallocated funds, as this currently has the highest number of signups, and is associated with below avg. claim amounts. 
</details>
<details>
<summary>3. For a goal of reducing campaigns that are indicative of, or associated with, subsequent high claims: Consider reducing 'Health Awareness' campaigns.</summary></br>
This type of campaign is associated with the highest frequency of claims made, although it does come 2nd in total number-of-signups. If this recommendation is being considered, more investigation into the categorical associations of this type is strongly advised, as 2/3 of its associations have an above average click through rate.
</details>
<details>
<summary>4. Gather & incorporate any data the Marketing team may have on the duration of campaigns.</summary></br>
This will allow for a more robust historical analysis, providing a renewed vigor in the paths of analysis.
</details>
