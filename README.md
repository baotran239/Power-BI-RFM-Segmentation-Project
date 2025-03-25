# I.Introduction
The project focuses on applying the RFM segmentation scoring method to categorize customers based on their online transaction behavior, aiming to develop tailored strategies for each customer group.

## II. Dataset
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
| **Fact table**  | Sale Order Detail, SalesOrderHeader                                                                           |
| **Dim table**   | Customer, Location, Dim_Date, Product, Segment, SalesReason, SalesOrderHeaderSalesReason              |

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


