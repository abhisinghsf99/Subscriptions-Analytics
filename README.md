# Subscriptions-Analytics

## Overview
This project explores subscription trends for a **simulated SaaS company**, using **MySQL** for database management and **Power BI** for visualization. The goal is to analyze **churn rates, conversion trends, and revenue fluctuations** to provide actionable insights for business strategy.

## Data Structure
The project models a real-world **SaaS subscription system** using a relational database with the following tables:
- **Users**: Captures user demographics and registration data.
- **SubscriptionPlans**: Stores plan details, including pricing.
- **UserSubscriptions**: Tracks user sign-ups, cancellations, and plan changes.
- **UserActivity**: Logs customer interactions and engagement.

### **Database Schema Example**
```sql
CREATE TABLE Users (
    UserID INT AUTO_INCREMENT PRIMARY KEY,
    FirstName VARCHAR(100),
    LastName VARCHAR(100),
    Email VARCHAR(100) UNIQUE,
    DateOfBirth DATE,
    Country VARCHAR(50),
    RegistrationDate DATE
);
```

## Key Insights
### Churn Analysis
- Rising churn trend observed from January 2023 onward, causing customer stagnation in early 2024.
- High churn negatively impacts growth, leading to a flattening of the cumulative customer curve.
- Potential solution: Improve retention strategies, such as loyalty programs and engagement campaigns.

### Conversion Trends
- Increase in plan upgrades from Basic to Premium plans in late 2023.
- Conversion rates peaked in specific months, indicating seasonal patterns in customer behavior.
- Actionable strategy: Enhance targeted promotions during months with high conversion potential.

### Revenue Insights
- Revenue showed steady growth until mid-2023, but increased volatility was observed afterward.
- Fluctuations in revenue streams could be due to external economic factors or changes in pricing strategy.
- Suggested action: Introduce flexible pricing models and better predict revenue stability.

### How to Use the Database Dump
1. **Set up MySQL:** Ensure MySQL is installed on your machine.

2. **Create a new database:**

  CREATE DATABASE subscription_db;

3. **Import the SQL dump file:**

  mysql -u your_user -p subscription_db < data/database_dump.sql

4. **Verify import:**

  SHOW TABLES;

5. **Run analytical queries from scripts/queries.sql to extract insights.**
