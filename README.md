# I.Introduction
The project focuses on applying the RFM segmentation scoring method to categorize customers based on their online transaction behavior, aiming to develop tailored strategies for each customer group.

# II. Dataset
- Dataset access: Connect Power BI to Google BigQuery and get the public dataset - adventureworks2019
- Data dictionary: file attached above

# III. Design thinking approach
## Step 1. Empathize 
### 5W-1H
| **Question**                                                      | **Answer**                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **Who will see the dashboard?**                                    | Sales Team, Marketing Team                                                                                                   |
| **If we have to choose only one stakeholder, who will be?**        | Sales Team                                                                                                                   |
| **What problem will the dashboard help to solve?**                 | Segment customers into different groups, analyze the performance and characteristics of each segment, and develop appropriate strategies to maintain, grow, retain, or attract each customer segment. |
| **Where and when will our stakeholders see the dashboard?**         | In the meeting, in the presentation session, or anywhere that they have to make decisions.                                   |
| **Why do we have to build the dashboard?**                         | Without the dashboard, stakeholders will lack a comprehensive view and detailed analysis, making it difficult to choose the appropriate strategies to target the customers. |
| **How will our stakeholders see the dashboard to solve their business objectives?** | They have to see the overall performance then zoom into the more detailed layers.                                           |

### Empathy map
| **Category**              | **Details**                                                                                                                                        |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Thinking and feeling**   | They feel confused and find it hard to discover insights when looking at raw data. They think they can utilize transactional data to give the right strategies. |
| **Seeing**                 | They see a massive and chaotic pool of raw data.                                                                                                   |
| **Saying and doing**       | "I want to deep dive into the collected data to find insights. I need to give data-driven decisions." <br> They seek data analysis and visualization to support their decision-making process. |
| **Pains**                  | Insufficient data and information may lead to inefficient solutions and decisions.                                                                 |
| **Gains**                  | Key insights, unmet needs, straight-to-the-point strategies, data-driven solutions.                                                                |

### Dataset exploration
| **Table Type** | **Details**                                                                                                   |
|----------------|---------------------------------------------------------------------------------------------------------------|
| **Fact table**  | SaleOrderDetail, SalesOrderHeader, SalesOrderHeaderReason                                                                          |
| **Dim table**   | Customer, Location, Product, SalesReason, RFMTable, RFMAverageValue             |

## Step 2. Ideate
### Northstar metrics
| **Question**                                   | **Answers**                                                                                                                                                                              |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **What VALUE you want to measure?**            | **1. Customers:** To track the number of unique buyers, assess customer base growth, and measure acquisition and retention effectiveness. <br><br> **2. Revenue:** To track the total income generated from customers and assess overall business growth. <br><br> **3. Orders:** To analyze the volume of transactions, providing insights into purchase behavior and operational demand. |
| **WHEN the value DELIVERY SUCCESS?**           | When they reach their maximum value                                                                                                                                                       |
| **WHY do you choose this metric?**             | **1. Customers:** To track the number of unique buyers, assess customer base growth, and measure acquisition and retention effectiveness. <br><br> **2. Revenue:** To track the total income generated from customers and assess overall business growth. <br><br> **3. Orders:** To analyze the volume of transactions, providing insights into purchase behavior and operational demand.|

### Dimension group
| **Dimension Data Group**    | **Define Point of View**               |
|-----------------------------|----------------------------------------|
| **Group 1**                 | segment                                |
| **Group 2**                 | time                               |
| **Group 3**                 | product                                |
| **Group 4**                 | location                          |
| **Group 5**                 | buying reason                                    |

### Point of view
| **View**                   | **Description**                                                                                           |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| **View 1: Customer Segmentation** |**Customer segmentation distribution** <br>  - by time period  <br>  - by location  <br>  - by product  <br>  - by buying reason |
| **View 2: Sales Performance**     |**Revenue/ Order**  <br>  - by segment <br> - by time period  <br>  - by location  <br>  - by product  <br>  - by buying reason |

# IV. Dashboard
### Data modeling
![Image](https://github.com/user-attachments/assets/015c73f0-ac49-43d5-bd86-dd499cdb96b2)

### Dashboard
<img width="1195" alt="Image" src="https://github.com/user-attachments/assets/00617388-0e2c-4dc2-9805-09ddacde0266" />

<img width="1195" alt="Image" src="https://github.com/user-attachments/assets/d7ede4fe-fc90-4308-ad22-50a370abaac4" />

# V. Insights
### Customer Segmentation
- The "Champions" segment generates 70.06% of total revenue with a small customer base, indicating a high-spending loyal group.
- "Can't Lose Them" was the second most revenue contributed group with relatively low customer base, showing their high-value basket.
- "Potential Loyalists" and "At Risk" segments show a considerable number of customers but lower revenue contribution, suggesting potential churn risks.
- "Hibernating" and "Lost" segments show very low engagement, indicating a need for reactivation strategies.

### Sales Performance:
- Peak revenue occurred around 2013, followed by a decline, indicating market changes or external factors affecting performance.
- "Road Bikes" dominate as the top revenue-generating subcategory.
- North America significantly outperforms other regions in revenue contribution, indicating strong market presence.
- "Price" reasons dominate over promotions or marketing, indicating habitual or necessity-based purchases.

# VI. Recommendations
| **Segment**                | **Characteristics**                                                                 | **Insights**                                       | **Recommendations** |
|----------------------------|-------------------------------------------------------------------------------------|---------------------------------------------------|---------------------|
| **Champions**              | - Recent, frequent purchases with high spending. <br> - Highly engaged and loyal.    | - Major revenue contributors (70%). <br> - Relatively small customer base (15%). | - Offer **VIP loyalty programs** with exclusive perks. <br> - Provide **early access to new products**. <br> - Encourage **referrals** with incentives. |
| **Loyal Customers**        | - Frequent buyers with moderate-to-high spending. <br> - Consistently engaged.      | - Important for retention and advocacy.           | - Introduce a **tiered rewards program**. <br> - Encourage **product reviews & social sharing**. <br> - Provide **personalized content & recommendations**. |
| **Potential Loyalists**    | - Recently purchased but with low frequency. <br> - Could develop into loyal customers. | - Largest amount of customers (28%). <br> - Relatively low revenue contributed (0.3%). | - Send **post-purchase follow-up emails**. <br> - Offer **discounts on the next purchase**. <br> - Use **remarketing ads** to maintain engagement. |
| **Customer Needing Attention** | - Purchased a few times but not recently. <br> - Moderate spending, inconsistent purchase behavior. <br> - Could become loyal customers if engaged properly. <br> - At risk of dropping off due to lack of connection. | - Customers with potential to increase spending but require re-engagement. | - Send **personalized product recommendations** based on past purchases. <br> - Offer **limited-time discounts** to encourage repeat purchases. <br> - Engage with **educational content** (e.g., blogs, emails, videos). <br> - Run **win-back email campaigns** with compelling offers. <br> - Use **social media retargeting** to stay top of mind. |
| **Can’t Lose Them**        | - Previously high-value customers who haven’t returned. <br> - Significant revenue loss if they leave. | - Second revenue contributors (16%). <br> - Low customer base (8%). | - Send **personalized re-engagement emails**. <br> - Offer **exclusive limited-time discounts**. <br> - Conduct **customer service follow-ups**. |
| **At Risk**                | - Long inactivity but had meaningful past transactions. <br> - May have shifted to competitors. | - Second largest customer base (24%). <br> - Relatively low revenue contributed (7%). | - Launch a **“We Miss You” campaign** with special deals. <br> - Recommend **products based on past interests**. <br> - Use **targeted remarketing ads**. |
| **Hibernating**            | - No activity for a long time. <br> - Previous transactions but no engagement now. | - Low engagement and spending. | - Run a **“Comeback Sale” campaign**. <br> - Introduce **new product lines** that fit past preferences. <br> - Gather feedback on why they stopped buying. |
| **Lost**                   | - No purchases in a very long time. <br> - Likely switched to competitors or lost interest. | - Little chance of reactivation unless strong incentives are given. | - Send a **“We’ve Changed” campaign** highlighting improvements. <br> - Offer **one-time exclusive incentives**. <br> - If unresponsive, **remove from marketing lists**. |
