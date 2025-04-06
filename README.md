# Sales Insights Analysis using Tableau & SQL
As part of my data analyst & data science journey, I performed an end-to-end sales insights project for an India-based hardware company, utilizing SQL-based databases
### Project Overview
This project focused on analyzing sales performance using structured data across multiple dimensions like revenue, profit, cost, and region. 
- Performed India based hardware company sales insights - A Data Analysis project.
- SQL (MySQL): Wrote complex queries to perform data extraction, transformation, and cleaning from multiple tables across two SQL database versions.
- ETL Process: Simulated an ETL pipeline by transforming unstructured records into a clean, analysis-ready star schema.
- Tableau: Created two interactive dashboards with filters, KPIs, and custom-calculated fields for business decision-making.
* Revenue Analysis Dashboard
* Profit Analysis Dashboard
- Tools used - MySql, Tableau, PowerBI, Github
  
### 🔗 [Sales Insights Tableau Public](https://public.tableau.com/views/SalesInsights-DataAnalysisProjectusingTableau_17438516539650/Dashboard-RevenueAnalysis?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link) :Tableau:

### Problem Statements
Sales director wants to know the performance of the company in various Indian states & accordingly provide some discount.
- Revenue breakdown by cities.
- Revenue brekdown by years & months.
- Top 5 customers by revenue & sales quantity.
- Top 5 Products by revenue.
- Net Profit & Profit Margin by Market

### Project Planning & Objectives
1. Purpose – What & Why? <br/>
To uncover actionable sales insights that were previously hidden, enabling the sales team to make data-driven decisions. The goal is to automate reporting, minimize manual data collection, and accelerate strategic decision-making.

2. Key Stakeholders – Who is Involved? <br/>
- Sales Director – Driving revenue strategy and execution 
- I.T. Team – Supporting infrastructure and data access
- Customer Service Team – Aligning customer feedback with sales insights
- Data & Analytics Team – Designing, building, and maintaining the dashboard

3. Expected Outcome – What Do We Aim to Achieve? <br/>
An interactive, real-time sales insights dashboard that replaces manual reporting processes and empowers the business with accurate, up-to-date visual analytics.

4. Success Criteria – How Will We Measure Success? <br/>
- Dashboard delivers live, automated sales order insights.
- Sales team improves decision-making and achieves at least 10% cost reduction in total spend.
- Sales analysts eliminate manual data gathering, saving up to 20% of business hours, enabling focus on higher-value tasks.

### Setup Process

Step 1: Download file: db_dump.sql and import it in MySql 

Step 2: Download Tableau Public (Free) or Tableau Desktop (14 days trial) to perform Data Analysis

Step 3: Do ETL(Extract, Transform, Load) if required

Step 4: Connect Tableau with MySql database or Excel database

Step 5: Save the file as (.twb or .twbx)

### Data Analysis Using SQL

Show all customer records

```SELECT * FROM customers;```

Show total number of customers

```SELECT count(*) FROM customers;```

Show transactions for Chennai market (e.g.market code for chennai is Mark001)

```SELECT * FROM transactions where market_code='Mark001';```

Show distrinct product codes that were sold in chennai. 

```SELECT distinct product_code FROM transactions where market_code='Mark001';```

Show transactions where currency is US dollars.

```SELECT * from transactions where currency="USD"```

Show transactions in 2020 join by date table.

```SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;```

Show total revenue in year 2020.

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";```

Show total revenue in year 2020, January Month.

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");```

Show total revenue in year 2020 in Chennai.

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020and transactions.market_code="Mark001";```

### Tableau Dashboards 
- Revenue Analysis

  ![Test Image 6](https://github.com/Nishita76/Sales-Insights-Analysis/blob/main/Tableau%20Dashboard/Dashboard%20-%20Revenue%20Analysis.png)

- Profit Analysis

  ![Test Image 6](https://github.com/Nishita76/Sales-Insights-Analysis/blob/main/Tableau%20Dashboard/Dashboard%20-%20Profit%20Analysis.png)
  
  
