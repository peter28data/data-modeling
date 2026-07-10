<h1 align="center">Peter Garay-Robles </h1>

<h3 align="center">A Data Engineer in Snowflake and Power BI. </h3>

----

## 📌 Star Schema 

## Denormalized Modeling - Kimball Approach

This project demonstrates Data Modeling in a Star Schema, also known as the Kimball Approach.

The Goal ->  Report the Limitations and Tradeoffs of data modeling techniques to fit different business requirements.

1. Sources - API, Database, Excel Files
2. Staging
3. Star Schema
4. Analytics Team

---

## 🎯 High-Level Overview

- Centralize the Data Warehouse
- Connect a One-To-Many Relationship to the Foreign Keys in "Dimension Tables"

1. Identify Fact from Business Activity KPI
2. Determine Dimensions such as Attributes and Decriptions
3. Create Marts for End Users

### The "Fact Table" 
Key points of data that have been chosen to reflect urgent business priorities and are surrounded by dimensions that provide a wealth of entry points for constraining and grouping

For example, Net Promoter Score and Customer ID's would be the fact table and central to providing insight into the customer experience. 

However, without the location of each customer ID, we cannot group the results to produce sentiment analysis in a meaningful way. 

### Result: 
A "Star Schema" Approach is identifying which part of the Data Tables are Key to tell a story and which part of the Data Tables are complementary to that key data. 

---

## 📌 Identify Facts

- Low Granularity, Keys & Numeric Values

Fact Tables are the foundation of the Data Warehouse, therefore, we want to highlight the components of a Fact Table, listed above.

### Granularity

What a single fact table record represents. The description of the measurement event. For example, the grain produced when a grocery store scanner measures the quanitity and the charged price of a product being purchased is the beep of the scanner; the description of the measurement event in the physical world that gives rise to a measurement. 
