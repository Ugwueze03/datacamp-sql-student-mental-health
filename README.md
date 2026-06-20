# 🧠 Analyzing Students' Mental Health with SQL

A SQL analysis project completed as part of the **DataCamp SQL Associate Track** and my **100 Days of Data Analysis** journey.

This project investigates how the length of stay affects the mental health of international students by analyzing depression, social connectedness, and acculturative stress scores.

---

## 📌 Project Overview

Using SQL, this project explores whether international students who spend more time studying abroad experience changes in their mental health.

The analysis focuses on three psychological indicators:

- Depression Score (PHQ)
- Social Connectedness Score (SCS)
- Acculturative Stress Score (AS)

---

## 🎯 Objective

Analyze mental health diagnostic scores of international students based on their length of stay and identify meaningful trends using SQL.

---

## 🛠 Tech Stack

### SQL
- SELECT
- WHERE
- GROUP BY
- ORDER BY
- COUNT()
- AVG()
- ROUND()

### Platform
- PostgreSQL
- DataCamp Workspace
- GitHub

---

## 📂 Repository Structure

```text
Mental-Health-SQL-Analysis/
│
├── README.md
├── analysis.ipynb
├── students.csv
└── mentalhealth.jpg
```

---

## 📜 Project Files

### SQL Analysis

➡️ **[analysis.ipynb](./analysis.ipynb)**

### Dataset

➡️ **[students.csv](./students.csv)**

### Visualization

➡️ **[mentalhealth.jpg](./mentalhealth.jpg)**

---

## 💻 SQL Query

```sql
SELECT
    stay,
    COUNT(inter_dom) AS count_int,
    ROUND(AVG(todep), 2) AS average_phq,
    ROUND(AVG(tosc), 2) AS average_scs,
    ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
```

---

## 📊 Key Insights

- Students who stayed between **8–10 years** recorded the highest average depression scores. However, these groups contain relatively few students, so conclusions should be interpreted with caution.

- Most international students in the dataset stayed for **1–3 years**, indicating that the dataset primarily represents newer international students.

- Students with longer stays generally reported **lower social connectedness scores**, suggesting reduced feelings of connectedness over time.

---

## 📚 Skills Demonstrated

- Data Aggregation
- SQL Filtering
- Statistical Analysis
- Grouped Analysis
- Exploratory Data Analysis (EDA)
- Insight Generation

---

## 👤 Author

**Stephen Ugwueze**

Aspiring Data Analyst passionate about SQL, Excel, Power BI, and transforming raw data into meaningful insights.
