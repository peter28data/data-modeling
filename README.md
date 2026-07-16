<h1 align="center">Peter Garay-Robles </h1>

<h3 align="center">A Data Engineer in Snowflake and Excel. </h3>

----

## 📌 Star Schema 

## Denormalized Data Modeling 

This project demonstrades Data Modeling and how tables are structured to Fact Tables and Dimension Tables. 


---

![star schema data model](https://github.com/peter28data/data-modeling/blob/3f632d4caebceafa14d82395f3935025a49cbca0/images/flowchart_star_schema_v2.png)

---

## 🎯 High-Level Overview

- Connect a One-To-Many Relationship to the Foreign Keys

1. Identify Facts from Business Activity Key Performance Indicators
2. Determine Dimensions from Attributes and Descriptions

### The "Fact Table" Holds the Keys
Customer ID's are Key points of data and Dimensions, such as Location, provide entry points for grouping Customer Sentiment Analysis by Region. 


### Result: 
Identifying parts of the Data Tables as Keys and complementary data as Dimensions result in operational efficiency when searching for Business Insights.

---

![star schema overview spreadsheet](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/spreadsheet_star_schema.png)

---

## 📌 Identify Facts

- Keys & KPI's

Fact Tables are the foundation of the Data Warehouse, listed below are components of a Fact Table.

- Sales, Profit, Quanitity, Cost

### Granularity

The Customer ID, Product ID, and City ID are the lowest points of Granularity that serve as Identifiers for Business Insights such as Customer Sentiment Analysis. 

---

![Fact Table](https://github.com/peter28data/data-modeling/blob/6063786bfcd3f56fa56643b9a883b055f33e7e4b/images/field_dictionary_fact_table.png)


## Dimensions Tables

- Attributes or Descriptions

Below is an Example of a Dimension Table; The outer component of the Star Schema, as shown below the Excel Model.


### Dimension Table stores Related Attributes in One Table

- Customer ID, Contact Name, City, Email Address

---


![excel data model customer dim](https://github.com/peter28data/data-modeling/blob/3f632d4caebceafa14d82395f3935025a49cbca0/images/excel_customer_dimension_table_v2.png)

---

![star schema data model](https://github.com/peter28data/data-modeling/blob/3f632d4caebceafa14d82395f3935025a49cbca0/images/flowchart_star_schema_v2.png)

---

## 📌 Data Modeling 

- Join Facts & Dimensions to Create Custom Views

A Star Schema produces a source of all the keys in a "Fact Table", allowing for Dimensions to be joined in to Create a Custom View known as a Data Mart. 

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


----

## 🤝 Done!  Thank you for Reading
For Project in SQL, click below:


1. SQL Portfolio Link: https://github.com/peter28data/SQL

2) Tableau Portfolio Link: https://github.com/peter28data/Tableau

3) Python Portfolio Link: https://github.com/peter28data/Python




---

<p><img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=peter28data&" alt="peter28data" /></p>


<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40"/> </a> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.postgresql.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original-wordmark.svg" alt="postgresql" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <a href="https://seaborn.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" alt="seaborn" width="40" height="40"/> </a> </p>


---

## 📫 How to Connect With Me:

🔗 Email: peter.garayrobles@gmail.com 

