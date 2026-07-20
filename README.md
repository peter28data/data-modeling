<h1 align="center">Peter Garay-Robles </h1>

<h3 align="center">A Data Engineer in Snowflake and Excel. </h3>

----

## 📌 How Tables Are Organized

## Data Modeling 

This project demonstrades Data Modeling to Organize common tables such as Customer Information Table, Product Information Table, Sales and Marketing Campaign Table, Geographic Table. 


---

![star schema data model](https://github.com/peter28data/data-modeling/blob/86c0859175938ff49f8801383bf1f6acd2becc22/images/star_schema_v6.png)

---

## 🎯 High-Level Overview

- Connect One-To-Many Relationship to the Foreign Keys

1. Identify Facts from Business Activity Key Performance Indicators
2. Determine Dimensions from Attributes

### The "Fact Table" Holds the Keys
Customer ID's are Key points of data and Dimensions, such as Location, provide entry points for grouping Customer Sentiment Analysis by Region. 


### Action Item: 
Identifying parts of the Data Tables as Keys and Complementary Data as Dimensions, produce operational efficiency for reporting and analyzing.

---

![excel star schema](https://github.com/peter28data/data-modeling/blob/5a9e3f987bcda82cf6775245b561ff5416a15932/images/v5/excel_star_schema_v5.png)

---

## 📌 Identify Facts

### Granularity

The Customer ID, Product ID, and City ID are the lowest points of Granularity that serve as Identifiers for Business Insights such as Customer Sentiment Analysis. 

- Keys & KPI's

### Fact Tables

The foundation of the Data Warehouse, listed below are components of a Fact Table.

- Customer Key, Gross Amount, Quanitity


---

![Fact Table](https://github.com/peter28data/data-modeling/blob/5a9e3f987bcda82cf6775245b561ff5416a15932/images/v5/excel_fact_field_dictionary_v5.png)


## Dimensions Tables

- Attributes of Customer Records

Below is an Example of a Customer Dimension Table; The outer component of the Star Schema, as shown below the Excel Model.


### Dimension Table stores Related Attributes in One Table

- Customer ID, Contact Name, Email Address

---


![excel data model customer dim](https://github.com/peter28data/data-modeling/blob/5a9e3f987bcda82cf6775245b561ff5416a15932/images/v5/dim_customer_v5.png)

---

![star schema data model](https://github.com/peter28data/data-modeling/blob/5a9e3f987bcda82cf6775245b561ff5416a15932/images/v5/star_schema_v5.png)

---

## 📌 Data Modeling 

- Join Facts & Dimensions to Create Custom Views

A Star Schema produces a source of all the keys in a "Fact Table", allowing for Dimensions to be joined in to Create a Custom View for Ad Hoc Analysis.

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

