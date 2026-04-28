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

<img width="1600" height="1000" alt="Untitled design" src="https://github.com/user-attachments/assets/c20f74f8-a1bc-4b74-9123-0c6ea447d0b2" />



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

### 1. Data Cleaning & Preprocessing
- Renamed columns for clarity
- Checked and handled null values
- Converted `Start Date` to `datetime` format and extracted `Year`

### 2. Performance Trends
- Average runs scored per year (line plot)
- Average strike rate per year (line plot)
- **Finding:** Overall upward trend in runs with a dip around 2015, followed by a strong recovery. Strike rate shows fluctuations over the career.

### 3. Positional Analysis
- Average runs and strike rate by batting position (bar plots)
- **Finding:** Positions 3 and 4 yield the highest average runs (~49). Position 6 shows an exceptionally high strike rate (~210), indicating aggressive finishing.

### 4. Innings Analysis
- Performance comparison between 1st and 2nd innings (runs, strike rate)
- **Finding:** Slightly higher runs and strike rate in the 2nd innings, suggesting strong chase ability.

### 5. Opponent Analysis
- Average runs and strike rate against each opposition (bar plots)
- **Finding:** Most successful against **Bangladesh** (highest average runs and strike rate). Least successful against **Pakistan**.

### 6. Venue Analysis
- Average runs and total innings at each ground (filtered to ≥5 innings)
- **Finding:** Best performances at **Dhaka** and **Chennai**. Weakest at **Dambulla**.

### 7. Dismissal Analysis
- Frequency and percentage of each dismissal type (pie chart)
- **Finding:** **Caught** is the most common dismissal (~63.6%), reflecting an aggressive playing style. Bowled and LBW are much less frequent.

### 8. Boundary Analysis
- Total 4s and 6s per year (line plot)
- Average boundaries per match against each opponent (bar plot)
- **Finding:** Highest fours in **2011**, highest sixes in **2013–2014**.

### 9. Advanced Insights
- Multi-factor analysis: venue, batting position, and opponent vs. average runs (horizontal bar plots)
- Peak year identification and before/after peak comparison (runs, SR, 4s, 6s)
- **Finding:** **Batting position** is the strongest predictor of high scores. Peak year was **2016**; post-peak play became more aggressive with higher strike rates and increased power hitting.

---

## Key Findings

| Area | Finding |
|---|---|
| Best Batting Position | Position 3 — Highest average runs (~49) |
| Most Aggressive Position | Position 6 — Strike rate ~210 |
| Best Opponent | Bangladesh — highest runs & SR |
| Toughest Opponent | Pakistan — lowest average metrics |
| Best Venue | Dhaka / Chennai — avg. runs above 55 |
| Most Common Dismissal | Caught — ~63.6% of all dismissals |
| Peak Year | 2016 — highest average runs in career |
| Post-Peak Trend | More aggressive — higher SR and boundaries |
| Innings Preference | 2nd Innings — slightly higher runs and SR |
| Boundary Peak | 4s peaked in 2011; 6s in 2013–2014 |

---
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

