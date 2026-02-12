
#FinTrack Pro – CLI Finance Manager

FinTrack Pro is a Command Line Interface (CLI) based Personal Finance Management System built using Python, SQLite, and SQLAlchemy ORM.

This project allows users to manage daily expenses, track subscriptions, maintain monthly budgets, and generate financial analytics using both ORM and raw SQL queries.

---

## Features

- Add Expense  
- Update Expense  
- Delete Expense  
- Search Expenses by Date  
- Category-wise Expense Analytics  
- Monthly Budget Alert System  
- Subscription Tracking  
- Persistent SQLite Database Storage  

---

## Technologies Used

- Python  
- SQLite  
- SQLAlchemy ORM  
- Raw SQL Queries  
- CLI (Command Line Interface)  

---

## Project Structure

FinTrack_Pro_Project/
│
├── main.py
├── fintrack.db
└── README.md

---

##  Database Design

Tables:

1. categories (id, name)
2. expenses (id, title, amount, date, category_id)
3. subscriptions (id, name, amount, next_date)
4. budgets (id, month, limit)

Relationship:

Category (1) ---- (Many) Expenses

---

## Sample SQL Query

SELECT c.name, SUM(e.amount)
FROM categories c
JOIN expenses e
ON c.id = e.category_id
GROUP BY c.name;

---

## Installation & Setup

Step 1: Clone the repository

git clone https://github.com/your-username/FinTrack_Pro_Project.git

Step 2: Navigate to the project folder

cd FinTrack_Pro_Project

Step 3: Install required dependencies

pip install sqlalchemy

Step 4: Run the project

python main.py

---

##  Learning Outcomes

- Understanding ORM concepts  
- Performing CRUD operations  
- Writing raw SQL queries  
- SQL Joins and Aggregation  
- Modular Programming  
- CLI Application Design  

---

##  Future Enhancements

- CSV Export Feature  
- Web Interface using Flask  
- Authentication System  
- Charts and Data Visualization  
- REST API Integration  

---

## Conclusion

FinTrack Pro demonstrates practical implementation of Python with databases using SQLAlchemy ORM and raw SQL. It is designed as an interview-oriented project and suitable for resume showcase.
