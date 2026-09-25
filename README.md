# minor_-project_2
 SpendDNA – Personal Spending &amp; Transaction Analysis
 # SpendDNA — Personal Transaction Analysis

## 📌 Project Overview

**SpendDNA** is a Python-based data analysis project that analyzes six months of bank and UPI transaction data.

The project processes raw transaction data, cleans the information, identifies vendors, categorizes spending, detects unusual transactions, and generates useful spending insights.

The project is based on a synthetic transaction dataset representing a Bengaluru-based software engineer from **January to June 2024**.

---

## 🎯 Project Objectives

The main objectives of this project are:

* Clean and process raw transaction data
* Standardize transaction dates and amounts
* Extract and normalize vendor names
* Categorize transactions into spending categories
* Analyze monthly spending patterns
* Study spending based on time of day
* Detect unusual transactions using Z-score
* Identify spending behavior/archetypes
* Generate a final spending summary
* Create additional insights using NumPy and Pandas

---

## 📂 Dataset

The dataset contains bank/UPI transactions with information such as:

* Date
* Time
* Transaction description
* Transaction type
* Amount
* Other transaction details

The dataset contains **1,328 raw transaction rows**.

### Time Period

**January 2024 – June 2024**

### Location

**Bengaluru, India**

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Jupyter Notebook / Google Colab**

### Libraries

```text
Python
Pandas
NumPy
```

No machine-learning libraries are required for this project.

---

## 🔄 Project Workflow

```text
Raw Transaction Data
        ↓
Data Cleaning
        ↓
Date & Amount Parsing
        ↓
Duplicate Removal
        ↓
Vendor Extraction
        ↓
Category Classification
        ↓
Spending Analysis
        ↓
Monthly Trend Analysis
        ↓
Time-of-Day Analysis
        ↓
Anomaly Detection
        ↓
Spending Archetype Detection
        ↓
Final SpendDNA Report
```

---

# 🚀 Features

## 1. Transaction Parser

The project cleans and standardizes the raw transaction data.

It handles:

* Different date formats
* Currency symbols
* Commas in amounts
* Debit/Credit transaction types
* Duplicate transactions
* Missing or invalid values

Example:

```text
₹1,250.00
Rs. 1,250
1,250
```

are converted into a numerical amount that can be analyzed.

---

## 2. Vendor Extraction

Different descriptions can represent the same vendor.

For example:

```text
POS SWIGGY BANGALORE
UPI-SWIGGY5057@OKAXIS
BHIM SWIGGY
SWIGGY*Order
```

are normalized into:

```text
Swiggy
```

Similar normalization is performed for vendors such as:

* Amazon
* Zomato
* Swiggy
* Uber
* Ola
* Blinkit
* Zepto
* Flipkart
* Myntra
* Starbucks
* Rapido
* BMTC
* Groww
* Zerodha

---

## 3. Spending Categories

Transactions are grouped into meaningful categories such as:

| Category          | Examples                   |
| ----------------- | -------------------------- |
| Food Delivery     | Swiggy, Zomato             |
| Quick Commerce    | Blinkit, Zepto, Instamart  |
| E-commerce        | Amazon, Flipkart, Myntra   |
| Transport         | Uber, Ola, Rapido, BMTC    |
| Restaurants       | Restaurants and dining     |
| Cafe              | Starbucks, Third Wave, CCD |
| Groceries         | DMart, BigBasket           |
| Fuel              | HP, BPCL, Indian Oil       |
| Utilities         | Jio, Airtel, BESCOM, BWSSB |
| Investments       | Groww, Zerodha             |
| Subscriptions     | Netflix, Spotify, Hotstar  |
| Rent & Housing    | Rent payments              |
| Entertainment     | BookMyShow                 |
| Cash Withdrawal   | ATM withdrawals            |
| Personal Transfer | UPI transfers              |

---

# 📊 Analysis Performed

## Spending Overview

The project calculates:

* Total credits
* Total debits
* Net change
* Savings rate
* Number of transactions
* Number of unique vendors
* Top spending categories
* Top vendors

---

## 📅 Monthly Trend Analysis

The project compares spending across:

```text
January
February
March
April
May
June
```

It identifies categories with increasing or decreasing spending patterns.

---

## 🕐 Time-of-Day Analysis

Transactions are analyzed according to the hour of the day.

The project creates a:

```text
Category × Hour
```

spending matrix.

It also checks late-night food delivery activity between:

```text
21:00 – 01:59
```

---

## 🚨 Anomaly Detection

The project uses the **Z-score** method to identify unusually large transactions.

Formula:

```text
Z = (X - Mean) / Standard Deviation
```

Transactions with:

```text
Z > 2
```

are flagged as potential anomalies.

---

# 👤 Spending Archetypes

The project identifies possible spending patterns based on predefined rules.

Examples include:

* 🍔 The Foodie
* 🛒 The Quick Commerce Junkie
* 🛍️ The Shopaholic
* 📈 The Investor
* 🌙 The Late-Night Snacker
* 🚕 The Cab Commuter
* 📺 The Subscription Lover
* 💸 The YOLO Spender
* 💰 The Disciplined Saver
* 💻 The Tech-Bro Investor

These are **rule-based classifications**, not machine-learning predictions.

---

# ⭐ Bonus Features

The project also includes additional analysis:

### Day-of-Week Analysis

Compares spending across:

```text
Monday → Sunday
```

### Vendor Cleanup Audit

Checks whether any transaction descriptions remain uncategorized.

### 3-Month Spending Forecast

Uses the average spending of the previous three months to estimate the next month's spending.

```text
Forecast = Mean of Last 3 Months
```

---

# 📁 Project Structure

```text
SpendDNA-Minor-Project-2/
│
├── Data set for DADS June.csv
│
├── SpendDNA_Minor_Project_2.ipynb
│
├── README.md
│
└── DS June_Minor_Project_2 Brief.pdf
```

---

# ▶️ How to Run

## Option 1 — Google Colab

1. Open Google Colab.
2. Upload:

```text
SpendDNA_Minor_Project_2.ipynb
```

3. Upload the dataset:

```text
Data set for DADS June.csv
```

4. Run all cells.

---

## Option 2 — Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy jupyter
```

Start Jupyter:

```bash
jupyter notebook
```

Open:

```text
SpendDNA_Minor_Project_2.ipynb
```

Upload/place the CSV in the same folder and run the notebook.

---

# 📌 Important Dataset Note

The project reports values calculated directly from the supplied CSV after cleaning and processing.

The numerical results may differ from illustrative/example values mentioned in the project brief because the analysis is based on the **actual supplied dataset**.

---

# 📈 Key Learning Outcomes

Through this project, I learned how to:

* Work with real-world style transaction data
* Clean messy datasets using Pandas
* Parse dates and numerical values
* Handle duplicate records
* Normalize inconsistent vendor names
* Create meaningful categories
* Group and summarize data
* Analyze trends
* Use NumPy for numerical calculations
* Detect anomalies using statistical methods
* Build rule-based user profiles
* Present data-analysis results in a clear format

---

# 👨‍💻 Author

**Naga Chaitanya**

**B.Tech — Civil Engineering**

This project was completed as part of a **Data Analytics / Data Science Minor Project**.

---

# 📜 License

This project is intended for **educational and academic purposes**.

