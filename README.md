# Student Lifestyle and Academic Performance Analysis

An analysis of how lifestyle habits relate to student academic performance (CGPA), using Python for data cleaning and exploration, MySQL for storage, and Power BI for an interactive dashboard.

## Dataset

1,000 engineering students, 12 columns, no missing values or duplicates.

| Column | Description |
| --- | --- |
| Age | Student age |
| Branch | CSE, IT, ECE, Electrical, Mechanical, Civil |
| Study_Hours_per_Day | Average daily study hours |
| Sleep_Hours | Average daily sleep hours |
| Screen_Time_Hours | Average daily screen time |
| Gym_Hours_per_Week | Weekly gym hours |
| Diet_Type | Veg or Non-Veg |
| Attendance_Percentage | Class attendance |
| Stress_Level_1_to_10 | Self-reported stress level |
| Residence | Hosteller or Day Scholar |
| Internal_Marks | Internal assessment marks |
| CGPA | Cumulative grade point average |

## What Was Done

- **Data cleaning:** removed null rows and stripped whitespace from column names.
- **Feature engineering:** created a `Performance` column from CGPA: Excellent (above 8.5), Good (6.5 to 8.5), Poor (below 6.5).
- **Exploratory analysis:** scatter plots of CGPA against study hours, sleep, attendance, screen time and internal marks.
- **Correlation analysis:** correlation matrix visualised as a heatmap.
- **Database:** cleaned data loaded into a MySQL table using SQLAlchemy.
- **Dashboard:** Power BI report with KPI cards (CGPA, attendance, study hours, total students), scatter plots, a branch-wise chart, and slicers for Branch, Performance, Diet Type and Stress Level.

## Key Findings

| Variable | Correlation with CGPA |
| --- | --- |
| Internal Marks | 0.87 |
| Sleep Hours | 0.62 |
| Study Hours per Day | 0.51 |
| Attendance Percentage | 0.42 |
| Stress Level | -0.17 |
| Gym Hours per Week | 0.04 |
| Screen Time Hours | 0.02 |

- Internal marks are the strongest indicator of CGPA.
- Sleep has a stronger relationship with CGPA than study hours.
- Attendance and study time both show moderate positive relationships.
- Higher stress is weakly linked to lower CGPA.
- Screen time and gym hours show almost no relationship.
- Branch, diet and residence make very little difference to average CGPA.

Performance distribution: Good (712), Poor (187), Excellent (101).

## Tools Used

Python (pandas, NumPy, Matplotlib, Seaborn), Jupyter Notebook, MySQL, Power BI

## Files

- `Student_Lifestyle_Data_cleaning.ipynb`: cleaning, analysis and visualisation
- `student_lifestyle_performance_dataset.csv`: dataset
- `student_performance.pbix`: Power BI dashboard
