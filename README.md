#  Virat Kohli ODI Performance Analysis (2008–2017)

![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)
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

- What is Kohli's average, median and most frequent score?
- Does he perform better while chasing (Inns 2) or setting a target (Inns 1)?
- Which teams does he score the most against?
- How does his strike rate vary across innings?
- What is his most common dismissal type?
- How many boundaries (4s and 6s) did he hit in this period?
- What is the trend of his performance over the years?
- At which batting position does he perform best?

---

## Key Findings & Insights

| Insight | Finding |
|---|---|
|  **Average Runs** | 46.85 per innings |
|  **Average Strike Rate** | 76.99 |
|  **Median Score** | 32.50 |
|  **Total 4s Hit** | 577 |
|  **Total 6s Hit** | 72 |
|  **Best Innings Type** | Inns 2 (Chasing) — highest SR of 192.30 |
|  **Most Common Dismissal** | Caught |
|  **Fixed Batting Position** | No. 3 |
|  **Highest Score in Dataset** | 154 (Inns 2) |
---

## Dataset Description

**File:** `Virat Kohli DataSet.csv`
**Shape:** 132 rows × 11 columns
**Period:** August 2008 — January 2017

| Column | Data Type | Description |
|---|---|---|
| `Runs` | int64 | Runs scored in that innings |
| `BF` | int64 | Balls faced |
| `4s` | int64 | Number of fours hit |
| `6s` | int64 | Number of sixes hit |
| `SR` | float64 | Strike rate |
| `Positions` | float64 | Batting position (1–5) |
| `Dismissal` | object | How he got out (caught, lbw, etc.) |
| `Inns` | int64 | 1st innings or 2nd innings |
| `Opposition` | object | Team played against |
| `Ground` | object | Venue/stadium name |
| `Start Date` | datetime64 | Date of the match |

**Data Quality:** ✅ No missing values · ✅ No duplicates · ✅ Clean dataset

---

## Analysis Sections

### 1. Data Cleaning & Preprocessing
- Renamed `Pos` → `Positions` for clarity
- Converted `Start Date` from `object` → `datetime64`
- Verified zero null values across all 11 columns
- Confirmed no duplicate rows in dataset

### 2. Descriptive Statistics
- Calculated mean, median, and mode for Runs, SR, and BF
- Mean Runs (46.85) > Median (32.50) → confirms right-skewed distribution
- Mode of Runs = 0 → multiple duck innings show high variance

### 3. Run Distribution Analysis
- Histogram reveals majority of scores fall in the 0–50 range
- Right-skewed distribution with long tail towards centuries
- Big scores rare but extremely impactful on overall average

### 4. Strike Rate Analysis
- Strike rate sorted and compared by innings type
- Inns 2 (chasing): SR as high as **192.30**
- Inns 1 (setting): more conservative, lower SR
- Strong evidence of Kohli being an elite **chase specialist**

### 5. Innings Performance Comparison
- Highest scores (154, 139, 136, 128, 123) all in **Inns 2**
- Multiple ducks appear more in Inns 1
- 2nd innings performance statistically superior in every metric

### 6. Dismissal Pattern
- **Caught** is the most common dismissal by far
- LBW second, Bowled third, Run Out very rare
- Bowlers consistently target outside edge and aerial shots

### 7. Boundary Analysis
- **577 fours** vs **72 sixes** → 8:1 ratio
- Kohli relies on timing and placement over power
- Technically correct ground-stroke batsman profile confirmed

### 8. Batting Position Analysis
- Consistently bats at **Position 3** throughout career
- Some early career appearances at Positions 1 and 2
- Locked in at No.3 from mid-career — never moved

---

## Tech Stack

```
Python 3.12
├── pandas          — data manipulation & cleaning
├── matplotlib      — base plotting library
├── seaborn         — statistical visualizations
└── jupyter         — interactive notebook environment
```

## requirements.txt

```
pandas==2.1.0
matplotlib==3.7.2
seaborn==0.12.2
jupyter==1.0.0
```

---

## Screenshots

<!-- Replace paths below with your actual chart screenshots -->
| Chart | Preview |
|---|---|
<img width="1039" height="703" alt="Screenshot (57)" src="https://github.com/user-attachments/assets/fa55a291-72aa-4df4-a5fe-42e8269e9339" />

<img width="791" height="628" alt="Screenshot (59)" src="https://github.com/user-attachments/assets/6bd1e972-ffdf-476b-8859-abee5df065d7" />

<img width="1458" height="614" alt="Screenshot (58)" src="https://github.com/user-attachments/assets/24de7e06-91d9-41ee-add6-c60b3ad565bd"/>

---

## Future Improvements

- [ ] Add Test and T20 data for format comparison
- [ ] Year-wise trend line for peak performance years
- [ ] Correlation heatmap (Runs vs SR vs BF)
- [ ] Compare with other top ODI batsmen (Rohit, Sachin, AB de Villiers)
- [ ] Build an interactive dashboard using Plotly or Streamlit
- [ ] Predict score based on opposition and venue using ML

---

## License

This project is open source and available under the [MIT License](LICENSE).

---
