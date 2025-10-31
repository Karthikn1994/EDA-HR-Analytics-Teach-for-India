Employee Performance - Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Built%20with-Python-blue?logo=python)
![Pandas](https://img.shields.io/badge/Library-Pandas-green?logo=pandas)
![Seaborn](https://img.shields.io/badge/Visuals-Seaborn-orange?logo=seaborn)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

Project Overview
This project is part of the **MentorMind HR Analytics Menternship**.  
The objective is to **perform Exploratory Data Analysis (EDA)** on an employee performance dataset to:

Discover patterns and trends in employee behavior  
Identify anomalies or deviations  
Test hypotheses using data  
Visualize categorical and numerical features  
Clean and prepare the data for predictive modeling  

---

Key Learnings
- Reading and understanding real-world HR datasets  
- Data cleaning and handling missing values  
- Identifying and treating outliers  
- Creating count plots and boxplots for feature insights  
- Building a clean, analysis-ready dataset  
- Summarizing data-driven HR insights for performance prediction  

---

Tools & Technologies Used
| Category | Tools / Libraries |
|-----------|--------------------|
| Programming | Python 3.x |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook (Anaconda) |
| Output Files | PDF, CSV, Notebook (.ipynb) |

---

Exploratory Data Analysis (Steps Followed)

Reading Data into a DataFrame
```python
import pandas as pd
df = pd.read_csv("employee_performance.csv")
df.head()
```

Data Cleaning
- Handled missing values using median/mode.  
- Removed duplicates.  
- Dropped irrelevant columns (`EmployeeID`, unnamed columns).

Count Plots for Categorical Variables
```python
import seaborn as sns
sns.countplot(data=df, x='Department', palette='pastel')
```

Boxplots & Outlier Detection
```python
sns.boxplot(x=df['MonthlyIncome'])
```

Correlation Heatmap
```python
import matplotlib.pyplot as plt
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title("Feature Correlation Heatmap")
plt.show()
```

---

Key Insights & Trends
- **Tenure vs. Performance:** Longer-serving employees show better ratings.  
- **Overtime Impact:** Employees with overtime often perform well but risk burnout.  
- **Departmental Trends:** “R&D” shows higher satisfaction; “Sales” shows higher turnover risk.  
- **Income Distribution:** Skewed toward lower brackets, few high earners dominate.  
- **Work-Life Balance:** Correlates strongly with job satisfaction and retention.

---

 How to Run the Notebook

1. Clone this repository**
   ```bash
   git clone https://github.com/<yourusername>/employee-performance-eda.git
   cd employee-performance-eda
   ```

2. Add your dataset file**
   Place your `employee_performance.csv` file in this folder.

3. Run the Jupyter Notebook**
   ```bash
   jupyter notebook EDA_employee_performance.ipynb
   ```
---

Author
Karthk N 
---

License
This project is licensed under the **MIT License**.  
Feel free to fork, modify, and build upon it for your learning or portfolio.

---

Acknowledgments
This project was developed as part of the **MentorMind HR Analytics Menternship**  
on *Building a Predictive Model to Forecast Employee Performance.*

---
