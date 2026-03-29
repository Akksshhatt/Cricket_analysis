#  Virat Kohli ODI Performance Analysis (2008–2017)
![Numpy](https://img.shields.io/badge/Numpy-150458?style=for-the-badge&logo=Numpy&logoColor=blue)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-00cc44?style=for-the-badge)

---

##  Project Overview

This project performs a complete **end-to-end Exploratory Data Analysis (EDA)** on Virat Kohli's ODI (One Day International) batting statistics from **2008 to 2017**.

The goal is to uncover patterns, trends, and key insights from Kohli's 132 innings — including his run-scoring habits, strike rate trends, dismissal patterns, boundary analysis, and performance across different oppositions and venues.

---

##  Questions This Project Answers

- Does he perform better while chasing (Inns 2) or setting a target (Inns 1)?
- Which teams does he score the most against?
- How does his strike rate vary across innings?
- What is his most common dismissal type?
- How many boundaries (4s and 6s) did he hit in this period?
- What is the trend of his performance over the years?
- At which batting position does he perform best?

## Tech Stack

```
├── numpy           — numerical computations & array operations
├── pandas          — data manipulation & cleaning
├── matplotlib      — base plotting library
├── seaborn         — statistical visualizations
└── jupyter         — interactive notebook environment
```

## requirements.txt

```
pandas
Numpy
matplotlib
seaborn
jupyter
```
## Analysis Sections

**1. Data Cleaning and Pre-processing**
Renaming columns, checking for null values, correcting data types, and extracting the year from match dates.

**2. Descriptive Analysis**
Distribution of runs scored across all matches visualized using a histogram to understand scoring frequency.

**3. Performance Trends**
Line plots tracking runs scored and strike rate over time to identify periods of high and low performance.

**4. Positional Analysis**
Grouping performance metrics by batting position to identify the most and least productive positions.

**5. Innings Analysis**
Comparing runs and strike rate between the 1st and 2nd innings using grouped averages and box plots.

**6. Opponent Analysis**
Bar plots and average statistics showing performance against each opposition team, identifying strongest and weakest matchups.

**7. Venue Analysis**
Aggregating total runs and average strike rate by ground to determine the best and worst performing venues.

**8. Dismissal Analysis**
Frequency and percentage breakdown of dismissal types, along with a time-series plot of dismissal patterns.

**9. Boundary Analysis**
Year-wise and opponent-wise breakdown of fours and sixes, including a combined boundary count feature.

**10. Advanced Insights**
Statistical comparison of batting positions across innings to detect any structural performance differences.

---

## Key Findings

- The majority of innings result in scores below 40 runs, though several centuries demonstrate the capacity for high-impact performances.
- Strike rate fluctuates significantly across matches, reflecting an aggressive but inconsistent batting approach.
- Performance in the 2nd innings is marginally stronger than in the 1st innings in both runs and strike rate.
- The highest boundary count was recorded against Sri Lanka; the lowest against Pakistan.
- Wellington was the strongest venue by runs scored; Adelaide the weakest.
- Caught dismissals are the most frequent mode of getting out, with no clear time-based pattern.
- 2011 saw the highest number of fours; 2013 and 2014 had the highest number of sixes.
---
## Screenshots

<!-- Replace paths below with your actual chart screenshots -->

<img width="1039" height="703" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/fa55a291-72aa-4df4-a5fe-42e8269e9339" />

<img width="791" height="628" alt="Screenshot (59)" src="https://github.com/user-attachments/assets/6bd1e972-ffdf-476b-8859-abee5df065d7" />

<img width="1458" height="614" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/24de7e06-91d9-41ee-add6-c60b3ad565bd"/>
---

