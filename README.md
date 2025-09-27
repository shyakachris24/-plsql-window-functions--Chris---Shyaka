## SHYAKA CHRIS (27889)
## Individual Assignment I: PL/SQL Window Functions Mastery Project
## STEP 1: BUSINESS PROBLEM & SUCESS CRITERIA
Business Problem:
The company lacks insights into which customers and products drive the most revenue across regions and time periods, making it difficult to optimize sales strategies, marketing, and inventory planning.

Success Criteria:
Use SQL analytics (ranking, aggregation, navigation, distribution) to identify top customers and products, track monthly sales trends and growth, and segment customers into revenue-based tiers for targeted decision-making.


##  STEP 2: 5 Key SQL Use Cases & Queries

 1.  `RANK()`: Ranks products by revenue per region and quarter to find best sellers.

 2.  SUM() OVER()`: Calculates cumulative monthly sales to show overall growth trend.

 3.   `LAG()`: Uses `LAG()` to compare current month’s revenue with previous month's for growth analysis.

 4.   `NTILE(4)`: Splits customers into quartiles based on total spending (e.g., VIPs, high spenders, etc.).

 5.   `AVG() OVER()`: Smooths sales trends using rolling 3-month averages.

## STEP 3: Database Schema

### 1. `customers`  
Stores customer details.
- <img width="322" height="106" alt="create table customer" src="https://github.com/user-attachments/assets/f0c09eb0-578a-418d-8863-0a399404dd93" />
---
### 2. `products`  
Stores product information.
- <img width="322" height="106" alt="create table customer" src="https://github.com/user-attachments/assets/64bab6a4-05e8-49d6-addb-a51cd5264c30" />
---
### 3. `transactions`  
Captures each sale made.
- <img width="322" height="106" alt="create table customer" src="https://github.com/user-attachments/assets/b1cf9bb3-98b6-428f-9455-4a834099eb05" />
---
## INSERTING DATA INTO TABLES
<img width="665" height="197" alt="inserting data to customers" src="https://github.com/user-attachments/assets/c01a2920-9c41-4a96-88af-afeeef0cfbe4" />

---
<img width="619" height="146" alt="inserting data to products" src="https://github.com/user-attachments/assets/5772ef62-45f4-43fa-9920-ed27abcd24d0" />

---
<img width="958" height="382" alt="inserting data to transactions" src="https://github.com/user-attachments/assets/569c3845-235f-45bd-8184-3c6f3b23ca53" />

---
## ENTITY RELATION MODEL
<img width="950" height="372" alt="customer relation" src="https://github.com/user-attachments/assets/bfc272c0-aec2-4733-987d-64147c168698" />

---
<img width="950" height="288" alt="product relation" src="https://github.com/user-attachments/assets/3760e1ba-c714-46cd-906c-ca4ff046e66b" />

---
<img width="951" height="374" alt="transaction relation" src="https://github.com/user-attachments/assets/d713c837-6ae1-4a75-8950-93633f187d8b" />

---
##  STEP 4: WINDOWS FUNCTION IMPLEMETATIOIN
1. Ranking Functions:RANK() allowing the business to identify top spenders in each region or quarter
   <img width="538" height="140" alt="rank sql" src="https://github.com/user-attachments/assets/d7c79d3f-bcf3-4bf2-884d-f6931bd02589" />

Here is the output

<img width="952" height="184" alt="output of ranking" src="https://github.com/user-attachments/assets/1bca9289-e286-4f79-b649-b4bd90cb4e15" />

2. Aggregate Functions with Window Frames: SUM(), AVG() They calculate cumulative sales and moving metrics over time. This enables the business to understand long-term sales trends, seasonality, and revenue growth trajectory.

   <img width="414" height="162" alt="aggregate sql" src="https://github.com/user-attachments/assets/a6a33730-ff86-4641-9d80-9e017319ca7c" />

    Here is the output

    <img width="948" height="184" alt="output of agg" src="https://github.com/user-attachments/assets/5ad2e29b-34b8-4414-8631-8c16f17624b5" />
    
4. Navigation Functions:LAG(), LEAD() These functions compare a current period’s value with the previous or next period, allowing the business to track revenue growth or decline over time.
   
   <img width="595" height="189" alt="navigation sql" src="https://github.com/user-attachments/assets/7f9b2c06-86d3-474e-9d2e-24327b8141e4" />

Here is the output

<img width="950" height="186" alt="output of navigation" src="https://github.com/user-attachments/assets/9459c80c-29d3-42e5-ac98-3a7f34f4e2dd" />

6. Distribution Function: NTILE(4), CUME_DIST() measure their cumulative position in the revenue distribution. Rewarding top-tier customers or re-engaging low spenders.

    <img width="546" height="142" alt="distribution sql" src="https://github.com/user-attachments/assets/265d466e-8d0f-42f0-b239-782155a05e12" />

Here is the output

<img width="949" height="186" alt="output of distribution" src="https://github.com/user-attachments/assets/9753adb5-d8fe-4466-aae5-18b36b9f66f9" />

---
 RECOMMENDATIONS
 
This project helped uncover valuable insights from sales and customer data using SQL analytics. By ranking top customers, tracking revenue trends, analyzing growth, and segmenting customers, I gained a clearer picture of where the business is performing well and where it can improve.
---

### “All sources were properly cited. Implementations and analysis represent original work. No AIgenerated content was copied without attribution or adaptation

---

**Author**: *Shyaka Chris*  
**Date**: 23 September 2025


