#  Virat Kohli ODI Performance Analysis (2008–2017)
![Numpy](https://img.shields.io/badge/Numpy-150458?style=for-the-badge&logo=Numpy&logoColor=blue)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-00cc44?style=for-the-badge)


---
# Virat Kohli Cricket Performance Analysis

## Project Overview

This project applies exploratory data analysis techniques to Virat Kohli's match-by-match batting records. The aim is to uncover patterns in performance across different years, batting positions, opponents, venues, and innings using Python libraries for data manipulation and visualization.

<img width="2600" height="2604" alt="dashboard_pro" src="https://github.com/user-attachments/assets/845624b6-faba-4d70-936f-3409b9e9eb64" />


---

## Dataset

- **File:** `Cricket DataSet.csv`
- **Coverage:** 2008 to 2017, one row per innings
- **Key columns:**

| Column | Description |
|---|---|
| Runs | Runs scored in that innings |
| SR | Strike rate |
| Positions | Batting position |
| Inns | Innings number (1st or 2nd) |
| Opposition | Opponent team |
| Ground | Venue of the match |
| Dismissal | Mode of dismissal |
| 4s | Number of fours hit |
| 6s | Number of sixes hit |
| Start Date | Date of the match |
| Year | Extracted from Start Date |
| Boundaries | Engineered column — 4s + 6s combined |

---

## Analysis Sections

**1. Data Cleaning and Pre-processing**
Renamed columns, checked for null values, corrected data types, and extracted year from match dates for time-based analysis.

**2. Performance Trends**
Yearly average runs and strike rate plotted using line charts to track overall progression and identify dips and peaks across the decade.

**3. Positional Analysis**
Grouped average runs and strike rate by batting position using bar charts to identify the most and least productive positions.

**4. Innings Analysis**
Compared 1st and 2nd innings performance on both runs and strike rate using grouped bar plots.

**5. Opponent Analysis**
Average runs and strike rate calculated for each opposition team to identify strongest and weakest matchups.

**6. Venue Analysis**
Total runs and average strike rate aggregated by ground to find best and worst performing venues.

**7. Dismissal Analysis**
Frequency and percentage of each dismissal type visualized using a pie chart to identify the most common mode of getting out.

**8. Boundary Analysis**
Year-wise trend of fours and sixes plotted as a line chart, and average boundaries per match calculated for each opponent.

---

## Key Findings

- Average runs show an overall upward trend across the decade with a sharp dip around 2015 followed by a strong recovery
- Strike rate fluctuates across years with no sustained period of dominance
- Batting positions 3 and 4 yield the highest average runs, making them Kohli's most productive slots
- Position 6 records an exceptionally high strike rate of around 210, reflecting an aggressive finishing role
- 2nd innings performance is marginally stronger than 1st innings in both runs and strike rate
- Most successful opponent is Bangladesh — highest average runs and strike rate
- Least successful opponent is Pakistan — lowest average runs and strike rate
- Wellington was the best performing venue; Adelaide was the weakest
- Caught dismissals account for approximately 63.6% of all dismissals, showing a tendency to get out while playing attacking shots
- 2011 recorded the highest number of fours; 2013 and 2014 had the highest sixes

---
**requirements.txt**

```
numpy
pandas
matplotlib
seaborn
jupyter
```

**Libraries used:**

```
├── numpy           — numerical computations and array operations
├── pandas          — data manipulation and cleaning
├── matplotlib      — base plotting library
├── seaborn         — statistical visualizations
└── jupyter         — interactive notebook environment

```

## ⚙️ How to Run This Project

### 1. Clone the repository

```
https://github.com/Akksshhatt/Cricket_analysis.git

```

### 2. (Optional) Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate           # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook cricket_analysis.ipynb
```

### 5. Run all cells

In the Jupyter interface, go to **Kernel → Restart & Run All** to execute the full analysis from top to bottom.

> **Note:** Make sure `Cricket DataSet.csv` is placed in the same directory as the notebook before running.

---

