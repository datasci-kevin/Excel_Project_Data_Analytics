# 📊 Project 1: Interactive Excel Dashboard

![Excel](https://img.shields.io/badge/Microsoft%20Excel-217346?logo=microsoftexcel&logoColor=white&style=flat-square)
![Data Cleaning](https://img.shields.io/badge/Data%20Cleaning-4B7E5E?style=flat-square)
![Data Validation](https://img.shields.io/badge/Data%20Validation-6BA43F?style=flat-square)
![Conditional Formatting](https://img.shields.io/badge/Conditional%20Formatting-F9A825?style=flat-square)
![Dynamic Visualizations](https://img.shields.io/badge/Dynamic%20Visualizations-003366?style=flat-square)

### 🎥 Demo
Check out the demo GIF showing the dashboard's interactivity!

![alt text](../assests/dashboard_demo.gif)
---

## 🏗️ Project Overview
This project is an interactive Excel dashboard that dynamically updates data based on user selections. Key features include:

- **Dynamic Dropdowns:** Built with validation sheets ensuring interdependent dropdowns (country, title, type).
- **Conditional Formatting:** Highlights selected items with a darker color for clarity.
- **Advanced Formulas:**
  - Dynamic median calculations based on selections:
    ```excel
    =MEDIAN(
      IF(
        (jobs_info[job_country]=A2) *
        (jobs_info[salary_year_avg]<>0) *
        (jobs_info[job_title_short]=title) *
        (ISNUMBER(SEARCH(type,jobs_info[job_schedule_type]))),
        jobs_info[salary_year_avg]
      )
    )
    ```
  - Data filtering for cleaner dropdowns:
    ```excel
    =FILTER(J2#, NOT(ISNUMBER(SEARCH("and", J2#))) * (J2# <> 0))
    ```
- **Data Validation Logic:** Ensures consistent dropdown options like "Full-time", "Part-time", excluding complex terms like "Full-time and Internship".

![alt text](../assests/formulas.png)

---

## 📊 Example of Chart Creation
The following columns were selected to make the item selected appear darker than the rest:

![alt text](../assests/data_show.png)

---

## 🧠 Key Skills Demonstrated
- **Advanced Excel functions and formulas**
- **Data cleaning and validation**
- **Pivot tables and cross-tab analysis**
- **Conditional formatting and drop-down validations**
- **Dynamic data visualizations (charts, salary comparisons)**

---

## 🚀 How to Use (Optional)
1. Open the Excel workbook (`Project_1.xlsx`).
2. Navigate to the dashboard sheets.
3. Select desired country, title, and type from the dropdowns.
4. Observe how the dashboard updates dynamically.

---

## 🌟 Conclusion & Reflection
This project demonstrates my ability to design **dynamic Excel dashboards** with advanced formulas and conditional formatting. By leveraging data validation, pivot tables, and interactive visuals, I created a user-friendly interface for job and salary analysis.

Future improvements could include:
- Enhancing visuals with custom charts or Power BI.
- Adding more metrics (e.g., average salary by skill or location).
- Expanding to include predictive modeling or trend analysis.

---

## 🛠️ Tools Used
- Microsoft Excel
- Advanced Formulas (MEDIAN, FILTER)
- Data Validation
- Conditional Formatting
- Pivot Tables and Dynamic Charts
