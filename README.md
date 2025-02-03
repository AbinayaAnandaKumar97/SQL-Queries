# **README - SQL Script for Financial Report**

## **Overview**

This SQL script generates a financial report that aggregates data from multiple sources, including **Payments**, **Rates**, and **CRMOpportunity**. The report displays the **Signed Amount (€)**, **Pending Amount (€)**, and **Paid Amount (€)** for each opportunity, broken down by month (January to December). The data is filtered by **Opportunity Status** (`signed`, `pending`, `paid`), and currency conversion is applied using exchange rates from the **Rates** table.

---

## **Business Requirements**

The report fulfills the following:

1. **Opportunity Information**: 
   - Includes **First Name**, **Last Name**, **Opportunity ID**, **Opportunity Status**, and **Opportunity Closed Date**.
   
2. **Monthly Financial Data**:
   - Shows the **Signed Amount (€)**, **Pending Amount (€)**, and **Paid Amount (€)** for each opportunity, broken down by month (January to December).
   
3. **Currency Conversion**:
   - Applies conversion rates from the **Rates** table to ensure consistent currency representation across all financial data.

4. **Opportunity Status Filter**:
   - Filters data by **Opportunity Status** (`signed`, `pending`, `paid`).

---

## **Execution Flow**

1. **Temp Table Cleanup**: Drops existing temporary tables if they exist.
2. **Data Extraction**: Extracts relevant data from the **Payments**, **Rates**, and **CRMOpportunity** tables.
3. **Currency Conversion**: Converts payment amounts based on the currency exchange rates from the **Rates** table.
4. **Data Aggregation and Pivoting**: Aggregates data by month and pivots the data to show monthly values for each opportunity.
5. **Final Report**: Joins and outputs a report showing the financial data for each opportunity, segmented by **Opportunity Status**.

---

This script is designed to provide a comprehensive view of the financial performance of opportunities, with monthly breakdowns of signed, pending, and paid amounts.
