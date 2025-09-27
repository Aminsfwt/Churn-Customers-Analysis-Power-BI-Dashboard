# Churn Analytics Dashboard using Power BI

 [<img width="1344" height="750" alt="image" src="https://github.com/user-attachments/assets/c44dd8c0-5fde-4266-8777-f0f8a6d1c218" />](https://github.com/Aminsfwt/Churn-Customers-Analysis-Power-BI-Dashboard/blob/main/1.PNG?raw=true)


## Overview

This project analyzes customer churn rates for a telecom company using Power BI. Churn refers to the rate at which customers discontinue or cancel their services during a specific period. It represents the percentage of customers who have stopped using the company’s services, either by switching to a competitor or completely ending their subscription. High churn rates can indicate customer dissatisfaction, poor service quality, pricing issues, or increased competition. Understanding churn and its influencing factors is essential for improving customer retention, enhancing service offerings, and maintaining a strong customer base.

The dataset includes customer details such as demographics, services used, contract types, and billing information to identify patterns in churn behavior.

## Metadata

- **Customer ID**: Unique identifier for each customer.
- **Gender**: Whether the customer is male or female.
- **Senior Citizen**: Whether the customer is a senior citizen (1) or not (0).
- **Partner**: Whether the customer has a partner (Yes/No).
- **Dependents**: Whether the customer has dependents (Yes/No).
- **Start Date**: The date when the customer started using the service.
- **Tenure**: Number of months the customer has stayed with the company.
- **Phone Service**: Whether the customer has phone service (Yes/No).
- **Multiple Lines**: Whether the customer has multiple lines (Yes/No/No phone service).
- **Internet Service**: Customer’s internet service provider (DSL/Fiber optic/No).
- **Online Security**: Whether the customer has online security (Yes/No/No internet service).
- **Contract**: Type of contract (e.g., Month-to-month, One year, Two year).
- **Payment Method**: Type of payment method (e.g., Electronic check, Credit card).
- **Monthly Charges**: Single month’s cost.
- **Total Charges**: Total billing amount for the entire subscription duration.
- **Churn**: Whether the customer churned (Yes/No).

## Objectives

The project aims to:
- Perform data cleaning and transformations.
- Build a data model (if needed).
- Create a Power BI dashboard to visualize churn analytics.
- Answer key questions about churn patterns.
- Provide recommendations to reduce churn and increase customer retention.

### Key Questions Addressed
- What is the overall churn rate?
- Which contract type (e.g., month-to-month, one year) has the highest churn rate?
- What is the average tenure of churned customers versus retained customers?
- What is the average tenure across customers with different contract types?
- Do customers with certain service types churn more frequently?
- What is the average tenure for customers by gender and status?
- Is there a noticeable difference in churn between customers with dependents versus those without?
- Are there any trends for churned and active customers over time?
- What are the average MonthlyCharges and TotalCharges for churned vs. retained customers?
- Do certain PaymentMethod types (e.g., Credit Card, Electronic Check) have higher churn rates?
- Do customers with multiple service subscriptions churn less than those with fewer subscriptions?
- What are the key predictors of churn in the dataset?

## Methodology

### 1. Data Upload and Cleaning
- Upload the dataset (`churn analysis dataset.csv`) into Power BI.
- Use Power Query to remove duplicates, blank rows, and handle missing values.
 

### 2. Data Modeling
- Designed a star schema model:
  - **Dimensions**:
    - Payment Method (ID & Name).
    - Services (ID & services like Phone Service, Internet Service, etc.).
    - Customer (ID, Gender, Partner, Dependents, Contract, Senior Citizen, Tenure).
    - Date (Date, ID, Year, Quarter, Month, Day) – Created using DAX.
  - **Fact Table**: Churn Rate (Payment Method ID, Service ID, Customer ID, Date Key, Start Date, Monthly Charges, Total Charges, Churn).

![Star Schema Model](https://github.com/Aminsfwt/Churn-Customers-Analysis-Power-BI-Dashboard/blob/main/Churn%20Data%20Model.PNG?raw=true)  

### 3. Dashboard Building
- Built visuals in Power BI to answer questions (e.g., bar charts for churn by contract, line charts for trends over time).
- Used DAX measures for calculations like Churn Rate, Average Tenure, etc.

![Power BI Dashboard](https://github.com/Aminsfwt/Churn-Customers-Analysis-Power-BI-Dashboard/blob/main/2.PNG?raw=true)  

![Power BI Dashboard](https://github.com/Aminsfwt/Churn-Customers-Analysis-Power-BI-Dashboard/blob/main/3.PNG?raw=true)
## Findings

- **Overall Churn Rate**: Approximately 26-27% (based on typical telecom data; exact value from dataset).
- **Highest Churn by Contract**: Month-to-month contracts have the highest churn.
- **Average Tenure**: Churned customers have lower average tenure than retained ones.
- **Churn by Service Types**: Customers with DSL & Phone services churn more frequently.
- **Multiple Subscriptions**: Yes, customers with multiple services churn less.
- **Key Predictors**: Internet Service (DSL higher churn), Monthly Charges (higher increases churn), Total Charges (lower predicts churn).
- Other trends: Higher churn in short-tenure customers, certain payment methods like Electronic Check.

For detailed findings, refer to `Churn Analytics Project Documentation.docx`.

## Recommendations

- **Reduce Monthly Charges**: Offer discounts for DSL and phone service users to lower churn.
- **Promote Longer Contracts**: Incentives for one- or two-year plans.
- **Bundle Services**: Encourage multiple subscriptions to increase retention.
- **Target High-Risk Groups**: Focus on short-tenure customers and those with high charges via personalized offers.
- **Improve Service Quality**: Address issues in DSL services.

## Files in This Repository

- `churn analysis dataset.csv`: The raw dataset.
- `Churn Analytics Dashboard.pbix`: Power BI file with the dashboard.
- `final project.docx`: Project overview and assignment details.
- `Churn Analytics Project Documentation.docx`: Step-by-step documentation and findings.
- `images/`: Folder for screenshots (e.g., dashboard.png, power-query-cleaning.png).

## How to Use

1. Download the repository.
2. Open `Churn Analytics Dashboard.pbix` in Power BI Desktop.
3. Refresh the data source if needed.
4. Explore the dashboard for interactive visuals.

## Technologies Used

- Power BI (Data Visualization, DAX, Power Query)
- Star Schema Data Modeling

## Contributing

Feel free to fork and submit pull requests for improvements!

## License

This project is licensed under the MIT License.

---




