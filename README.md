# Employee-Demographics-and-Salary-Analysis-System

This project explores employee trends and compensation insights using SQL for data analysis and Tableau for interactive visualizations. The dashboard answers key questions about workforce distribution, gender parity, salary trends, and managerial dynamics within an organization over time.
![Dashboard Thumbnail](https://github.com/SayantaniSengupta/Employee-Demographics-and-Salary-Analysis-System/blob/169b59bdd22cda1ed28cef28ebb63b74b5382fb5/screenshot.png)
##  Sample SQL Queries
---

##  Project Overview

This project simulates a real-world HR analytics system by integrating structured SQL queries with a rich Tableau dashboard. It provides deep insights into:

- 👨‍👩‍👧‍👦 Gender-wise employee distribution across years
- 💸 Average annual salaries over time
- 🧑‍💼 Managerial trends by department
- 🏢 Salary comparison by department and gender

---

##  Database Schema

The dataset is inspired by a simplified HR system and contains the following tables:

- `employees` – Personal and demographic info of employees
- `departments` – Department names and IDs
- `salaries` – Salary history with effective dates
- `titles` – Employee roles over time
- `dept_manager` – Department managers with tenure information

---

##  Technologies Used

- **SQL** – Data querying, aggregation, joins, and time-based analysis
- **Tableau** – Dashboard design, data storytelling, interactivity
- **MySQL** – For database simulation 

---

##  Key Visualizations in Tableau

| Visualization Title                     | Description |
|----------------------------------------|-------------|
| Gender Distribution Over Time          | Stacked bar chart showing growth of male vs. female employees |
| Average Annual Salary Trend            | Line chart tracking salary growth from 1990 onwards |
| Number of Managers per Department      | Area chart showing managerial presence by year |
| Average Salary by Department & Gender  | Bar chart comparing pay equity across departments |

---


```sql
-- Average salary by gender per year
SELECT YEAR(from_date) AS year, gender, AVG(salary) AS avg_salary
FROM employees e
JOIN salaries s ON e.employee_id = s.employee_id
GROUP BY year, gender;
## 🌐 Interactive Dashboard



