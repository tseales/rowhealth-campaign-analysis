# Row Health Campaign Performance Analysis

## About Our Company & Data
Founded in 2016, Row Health is a medical insurance company serving thousands of customers throughout the United States. In 2019, they launched a new set of marketing campaigns spanning topics like Health Awareness, Covid Awareness, and Health Tips. Now that they’re strategizing their marketing budget for the forthcoming year, the company would like to attain a better understanding of the effectiveness of these various types of campaigns, and how they relate to signups and subsequent patient claims. This project conducts a focused analysis on the aforementioned metrics, campaign costs, CTR, MoM & YoY frequency of claims. The garnered insights will allow the Marketing team to make advantageous data-driven decisions for increasing campaign effectiveness.


The ERD can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/f4ac1220566dfc81dff4621e1ab8e0c0d74618e0/artifacts/ERD.md). An Excel workbook can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/f4ac1220566dfc81dff4621e1ab8e0c0d74618e0/artifacts/Row%20Health%20Data.xlsx). A Jupyter Notebook with EDA completed in Python, utilizing Pandas, can be found [here](https://github.com/tseales/rowhealth-campaign-analysis/blob/c99580226f8eecbb4127696215eb2edf0f78d7ea/artifacts/rowhealth-camp-performance-eda.ipynb)

## Summary of Insights
<details>
<summary>Stakeholder Initial Questions</summary>
  1. Which campaigns resulted in the highest number of signups?</br>
  2. How does the type of campaign correlate with the type of plan chosen?</br>
  3. How does the cost of a campaign relate to the number of signups?</br>
  4. What do claims look like for customers acquired through certain campaign groupings?
</details>

Conducting an analysis on 49k+ `customers`, `claims`, `campaigns` records for the years 2019-2023, key insights in the following areas were made:
### 1) Campaign Costs & Signups
**Note:** *24 campaigns did not have any associated customers. Analysis was done on 33/57 campaigns.*
- There is no significant relationship between the cost of a campaign and the number of signups.
- The top 5 highest-signup campaigns *(see section 2)* have an avg. cost-per-signup of $0.59; 199% less than the overall avg. of $203.91.
- Campaigns of type 'Covid Awareness' & 'Offer Announcement' have the largest average cost-per-signup, at $537.25 and $411.94 respectively - surpassing the overall average of $203.91. In relation to costs, 'Covid Awareness' is 2nd highest, at $6.6K; 'Offer Announcement' in 5th, at $4.2K.
  - 7 Campaigns (21.2%) are above the avg. cost/signup.
  - 26 Campaigns (78.8%) are below the avg. cost/signup.
- 'Customer Testimonial' is the highest-costing campaign with a total of $7.2K &ndash; 4th in total number of signups. The following chart depicts types of campaigns with their associated costs & signups, from most-to-least expensive:

![campaign-cost-vs-signup-barchart](https://github.com/user-attachments/assets/bf71ff58-3376-459f-9a20-5c0c2c886f6e)
</br></br>

### 2) Campaign Signups & Plans


### 3) Frequency of Claims

