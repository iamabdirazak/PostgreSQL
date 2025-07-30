# 🧠 PostgreSQL + Python: Data Science Pipeline (Tips Dataset)

This project demonstrates how to set up a complete **Data Mining and Analysis workflow** using **PostgreSQL and Python** — just like a real Data Scientist or Analyst would in production.

It covers:

- Setting up a PostgreSQL database
- Creating a user and database schema
- Loading real-world data (`tips.csv`) into a table
- Running SQL queries from Python
- Pulling results into pandas for analysis

---

## 📦 Project Structure

.
├── tips.csv # The dataset (restaurant tips data)
├── load_tips_to_postgres.py # Python script to load + query the DB
├── README.md # You’re here

---

## 🚀 How to Run This Project

### 1. Prerequisites

- PostgreSQL installed (`brew install postgresql`)
- Python 3.8+
- Install required libraries:

```bash
pip install pandas sqlalchemy psycopg2

2. Start PostgreSQL
brew services start postgresql

3. Create User + Database (run in psql)
CREATE USER ds_user WITH PASSWORD 'ds_pass';
CREATE DATABASE ds_pipeline;
GRANT ALL PRIVILEGES ON DATABASE ds_pipeline TO ds_user;

4. Run the Python Script
python3 load_tips_to_postgres.py

You’ll see a printed summary showing average tips and bills grouped by day.

📊 Sample Output
     day   avg_tip  avg_bill
0    Sun    3.25     21.41
1    Sat    2.99     20.44
2   Thur    2.77     17.68
3    Fri    2.73     17.15
```
