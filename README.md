# SQL-Database-Project
A database project developed using SQL
# Café Management System

A relational database project built with **MySQL** to manage customers, menu items, and orders in a café.
Developed as a Database course project at **Umm Al-Qura University** (May 2026).

## Team
- Ghufran Talal Simbawah - Conceptual design and documentation
- Fatmah Obaid Alruweys - Schema, DDL, constraints, and sample data
- Lujain Mohammed Alabdali - SQL queries, view, and reporting

**Instructor:** Dr. Najwa Samarkandi

## Project Overview
The system stores customer information, menu details, and order records, and lets the café track which customers placed orders and which items were ordered.

## Database Design
**Database:** `CafeManagementDB`

| Table | Description | Key Columns |
|-------|-------------|-------------|
| `CUSTOMER` | Customer data | Customer_ID (PK), Customer_Name, Phone_Number (UNIQUE) |
| `ITEM` | Menu items | Item_ID (PK), Item_Name, Price (CHECK > 0) |
| `ORDERS` | Orders | Order_ID (PK), Order_Date, Customer_ID (FK), Item_ID (FK) |

**Relationships:** one customer can place many orders (1:M); one item can appear in many orders.

## Constraints
- Primary Keys on all tables
- Foreign Keys in `ORDERS`
- `UNIQUE` on phone numbers
- `CHECK (Price > 0)`

## SQL Queries
1. Customers whose phone starts with `0505` (`LIKE`)
2. Items priced above 15 (`WHERE`)
3. Number of orders per customer (`COUNT` + `GROUP BY`)
4. Average menu price (`AVG`)
5. Full order report (multi-table `JOIN`)
6. Customers who ordered items above the average price (nested subquery)
7. `Order_Report` view for automated reporting

## Tools
MySQL Workbench, SQL, ER Diagram, Relational Schema

## How to Run
1. Open MySQL Workbench.
2. Run the script to create `CafeManagementDB` and its tables.
3. Insert the sample data (5 records per table).
4. Run the queries and the `Order_Report` view.

## Report
See the full project report (PDF) in this repository.
