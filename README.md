<h1 align="center">Peter Garay-Robles </h1>

<h3 align="center">A Data Engineer in Snowflake and Excel. </h3>

----

## 📌 Star Schema 

## Denormalized Data Modeling 

This project demonstrades the Tradeoffs of data modeling techniques such as Star Schema and Snowflake Schema.

---

![star schema data model](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/Flowchart%20from%20Provided%20Content.png)

---

## 🎯 High-Level Overview

- Connect a One-To-Many Relationship to the Foreign Keys

1. Identify Fact from Business Activity KPI
2. Determine Dimensions such as Attributes and Decriptions
3. Create Marts for End Users

### The "Fact Table" 
Customer ID's are Key points of data and Dimensions, such as Location, provide entry points for grouping Customer Sentiment Analysis by Region. 


### Result: 
To join the Location data, a "Star Schema" provides efficiency to one "Fact Table" by identifying which part of the Data Tables are Keys, and which part of the Data Tables are complementary to to tell a story.

---

![star schema overview spreadsheet](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/spreadsheet_star_schema.png)

---

## 📌 Identify Facts

- Granularity & Keys 

Fact Tables are the foundation of the Data Warehouse, therefore, we want to highlight the components of a Fact Table, listed below.

- Sales, Profit, Quanitity, Cost

### Granularity

In this case the Customer ID, Product ID, and City ID are the lowest points of Granularity that will provide business insights for Customer Sentiment Analysis. 

---

![Fact Table](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/field_dictionary_fact_table.png)


## Dimensions Tables

- Attributes or Descriptions

Below is an Example of a Dimension table that are the outer components of the Star Schema, as shown below the Excel Model.

A Star Schema stores Related Attributes in One Dimension Table

- Month, Quarter, Year, Category, Brand, City, State, Name

---


![excel data model customer dim](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/excel_data_model_customer_dim.png)

---

![star schema data model](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/Flowchart%20from%20Provided%20Content.png)

---

## 📌 Data Mart

- Join Facts & Dimensions to Create Custom Views

A Data Mart can be a custom view of Total Orders by Product. A Star Schema produces a source of all the keys in a "Fact Table", allowing for Dimensions to be joined in to Create a Custom View known as a Data Mart. 

---

### The Entity Relationship Diagram (ERD)
- Data Model below is used to support Business Intelligence tools such as Power BI. 


---

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ ORDER_ITEM : contains
    PRODUCT ||--o{ ORDER_ITEM : included_in

    CUSTOMER {
        int customer_id PK
        string name
        string email
    }

    ORDER {
        int order_id PK
        date order_date
        int customer_id FK
    }

    PRODUCT {
        int product_id PK
        string product_name
        decimal price
    }

    ORDER_ITEM {
        int order_id FK
        int product_id FK
        int quantity
    }
```


