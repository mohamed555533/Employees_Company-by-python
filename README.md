🔍 Data Analysis Project: Employee Insights from Company Dataset
I recently completed a comprehensive exploratory data analysis (EDA) and data cleaning project using Python on an employee dataset. Here’s a quick walkthrough of what I did and the insights I uncovered.

📂 Dataset & Goal
The dataset contained employee information including demographics, job details, salaries, leaves, and overtime. The goal was to clean the data, handle missing values and outliers, and visualize key patterns to derive actionable insights.

🧹 Data Cleaning & Preparation
Removed irrelevant columns (No, Office).

Created a Full Name column from first/last names.

Dropped rows with missing Full Name.

Filled missing values:

Department → most frequent (“Manufacturing”)

Monthly Salary, Annual Salary, Job Rate, Years of Experience → mean

Overtime Hours → median

Renamed Ge to Gender and extracted Year from Start Date.

✅ Final clean dataset: 617 employees after outlier removal.

📊 Outlier Detection
Used IQR method to identify outliers in:

Monthly Salary

Years of Experience

Overtime Hours

Interesting outlier: three employees had >23 years of experience (the highest was ~28 years). These were excluded from further analysis.

📈 Key Visualizations & Insights
1. Gender Distribution
👩‍🦰 Female: 185 (30%)
👨‍🦱 Male: 432 (70%)
➡️ Significant male majority.

2. Top Departments by Total Annual Salary
Manufacturing leads by a large margin, followed by Quality Control and Account Management.

Suggests where the company invests most in salaries.

3. Average Overtime Hours by Department
Quality Control and Manufacturing show highest average overtime (~10–20 hours).

Low overtime in Sales, Training, Creative – possible workload balance or different policies.

4. Years of Experience vs. Annual Salary
Positive correlation, but with a wide spread – indicating that experience alone doesn’t guarantee high pay; other factors like role and department matter.

5. Employee Count by Country
Egypt dominates (331 employees), followed by UAE (150), Saudi Arabia (76), Syria (50), Lebanon (10).

Reflects regional presence of the company.

6. Unpaid Leaves by Department
Manufacturing and Quality Control also top in total unpaid leaves – could be linked to overtime or different leave policies.

🛠 Tools Used
Python (pandas, matplotlib, plotly)

Jupyter Notebook for interactive analysis

Visual storytelling with Plotly Express

💡 Takeaways
This project reinforced my skills in data cleaning, outlier treatment, and creating meaningful visualizations. The insights can help HR and management understand workforce distribution, salary trends, and departmental workloads.

Would love to hear your thoughts! If you're interested in the full code or have questions, drop a comment below. 😊

#DataAnalysis #Python #DataScience #EDA #HRanalytics #DataVisualization #LinkedInLearning

عاوز ملف README
We need to create a README file summarizing the project. The user wants a README to accompany the project, possibly for LinkedIn or GitHub. The context is a data analysis project on employee data.

We should write a README that explains the project purpose, steps taken (data exploration, cleaning, outlier detection, visualizations), and key insights. Use a professional but accessible tone, maybe include an overview, tools used, results, and perhaps a sample of findings.

Given the notebook content, we can summarize:

Data loading and initial exploration.

Data cleaning: removing unnecessary columns, handling missing values (fill with mean/median/mode), renaming, creating new columns (Full Name, Year).

Outlier detection using IQR for monthly salary, years of experience, overtime hours.

Visualizations: scatter plots, histograms, bar charts, pie charts to show distributions, relationships, and comparisons.

Key insights: gender distribution, department salary totals, overtime by department, experience vs salary, employee count by country, unpaid leaves by department.

We can structure the README with sections: Project Overview, Data Source, Steps Performed, Key Findings, Technologies Used, How to Run, etc.

We'll produce a clean, markdown-formatted README.md file.

📊 Employee Data Analysis Project
This project performs an exploratory data analysis (EDA) and data cleaning on a company employee dataset. The goal is to uncover insights about employee demographics, salary trends, departmental workloads, and leave patterns.

📁 Dataset
The dataset (Employees_Company.xlsx) contains 693 employee records with 16 columns, including:

Personal info: First Name2, Last Name, Ge (gender)

Job info: Department, Job Rate, Start Date

Compensation: Monthly Salary, Annual Salary

Attendance: Sick Leaves, Unpaid Leaves, Overtime Hours

Other: Country, Center, Office (mostly empty)

🔍 Steps Performed
1. Data Exploration
Used df.info(), df.describe(), df.isna().sum() to understand data types, missing values, and basic statistics.

Checked unique values in categorical columns.

2. Data Cleaning
Removed irrelevant columns: No and Office (all null).

Created Full Name by combining and capitalizing first and last names.

Dropped rows with missing Full Name.

Filled remaining missing values:

Department: mode (most frequent = "Manufacturing")

Monthly Salary, Annual Salary, Job Rate, Years of Experience: mean

Overtime Hours: median

Renamed Ge → Gender.

Converted Job Rate and Overtime Hours to integers.

Extracted Year from Start Date.

3. Outlier Detection
Used the IQR method on Monthly Salary, Years of Experience, and Overtime Hours.

Visualized outliers with boxplots.

Removed outliers to retain 617 clean records for analysis.

4. Visualizations & Insights
Gender Distribution: Pie chart showing male/female ratio.

Total Annual Salary by Department: Bar chart highlighting top departments.

Average Overtime by Department: Bar chart comparing workload across teams.

Years of Experience vs. Annual Salary: Scatter plot revealing correlation.

Employee Count by Country: Bar chart of regional presence.

Total Unpaid Leaves by Department: Bar chart identifying departments with highest unpaid leave totals.

📈 Key Findings
Gender imbalance: 70% male, 30% female.

Highest total salary spend: Manufacturing, followed by Quality Control and Account Management.

Overtime hotspots: Quality Control and Manufacturing have the highest average overtime (~10–20 hours).

Experience–salary correlation: Positive but not deterministic – other factors play a role.

Regional concentration: Most employees are in Egypt (331), then UAE (150), Saudi Arabia (76), Syria (50), Lebanon (10).

Unpaid leaves: Manufacturing and Quality Control also lead in total unpaid leaves, possibly linked to higher overtime or different leave policies.

🛠️ Technologies Used
Python 3

pandas – data manipulation

matplotlib / plotly – visualizations

Jupyter Notebook – interactive development

🚀 How to Run
Clone the repository.

Install dependencies: pip install pandas matplotlib plotly

Place the Employees_Company.xlsx file in the same directory as the notebook.

Run the Jupyter notebook final project.ipynb.

📌 Future Work
Build predictive models for salary or leave patterns.

Incorporate more advanced feature engineering.

Create an interactive dashboard using Dash or Streamlit.
