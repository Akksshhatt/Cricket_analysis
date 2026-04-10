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

### 1. Data Cleaning & Pre processing

- Loaded dataset using `pandas`
- Renamed the `Pos` column to `Positions` for clarity
- Checked and handled null values
- Converted `Start Date` to `datetime64` type
- Extracted `Year` as a separate column for time-series analysis
- Inspected data types to ensure correctness before analysis

---

### 2. Performance Trends

**Goal:** Understand how Kohli's batting performance evolved over the years.

- Computed **yearly average runs** and plotted a line chart
- Computed **yearly average strike rate** and plotted a line chart
- Used `seaborn.lineplot` with markers for clarity

**Visuals:**
- 📈 Line plot — Average Runs Over Time
- 📈 Line plot — Average Strike Rate Over Time

**Insight:** Average runs show an overall upward trend with a sharp dip around 2015, followed by a strong recovery and peak performance in later years.

---

### 3. Positional Analysis

**Goal:** Identify which batting positions yield the best results for Kohli.

- Grouped data by `Positions` and computed mean `Runs` and `SR`
- Plotted side-by-side bar charts for both metrics
- Identified the most and least productive positions using `.max()` and `.min()`

**Visuals:**
- 📊 Bar chart — Average Runs by Batting Position
- 📊 Bar chart — Average Strike Rate by Batting Position

**Insight:**
- Positions **3 and 4** yield the highest average runs (~49), confirming Kohli's dominance in the top order
- Position **6** shows an extremely high strike rate (~210), indicating aggressive finishing when needed

---

### 4. Innings Analysis

**Goal:** Compare Kohli's performance in the 1st vs 2nd innings.

- Grouped data by `Inns` and computed mean `Runs` and `SR`
- Visualized comparison using a grouped bar chart

**Visual:**
- 📊 Bar chart — Runs & SR: 1st vs 2nd Innings

**Insight:** Kohli shows slightly better and more aggressive performance in the 2nd innings — higher runs and strike rate — though variability exists across matches.

---

### 5. Opponent Analysis

**Goal:** Determine which opponents Kohli performs best and worst against.

- Grouped data by `Opposition` and computed mean `Runs` and `SR`
- Sorted and plotted bar charts
- Identified the best and worst opponents using `.max()` and `.min()`

**Visual:**
- 📊 Bar chart — Average Runs & Strike Rate vs Each Opponent

**Insight:**
- **Most successful against:** Bangladesh — highest average runs and strike rate
- **Least successful against:** Pakistan — lowest average on both metrics

---

### 6. Venue Analysis

**Goal:** Analyse Kohli's batting performance across different cricket grounds.

- Aggregated total runs, average runs, average SR, and innings count per venue
- Filtered venues with a minimum of 5 innings for statistical reliability
- Plotted a horizontal bar chart sorted by average runs
- Identified best and worst venues using `idxmax()` and `idxmin()`

**Visual:**
- 📊 Horizontal bar chart — Average Runs by Ground (min. 5 innings)

**Insight:**
- **Best venues:** Dhaka and Chennai — average runs above ~55
- **Worst venue:** Dambulla — average drops sharply (~20)

---

### 7. Dismissal Analysis

**Goal:** Understand patterns in how Kohli gets dismissed.

- Filtered out "Not Out" entries and counted dismissal types
- Computed percentage distribution using `value_counts(normalize=True)`
- Visualized with a pie chart

**Visual:**
- 🥧 Pie chart — Dismissal % Distribution

**Insight:**
- **Caught** is the most common dismissal mode at ~63.6%, suggesting Kohli frequently plays attacking shots
- Bowled, run out, and LBW are far less frequent; stumped and hit wicket are very rare

---

### 8. Boundary Analysis

**Goal:** Analyse Kohli's boundary-hitting trends over time and per opponent.

- Computed total fours (4s) and sixes (6s) per year using `.groupby('Year')`
- Created a new `Boundaries` column = `4s + 6s`
- Computed average boundaries per opponent and per match
- Plotted line and bar charts

**Visuals:**
- 📈 Line chart — Trend of 4s vs 6s Over Time
- 📊 Bar chart — Average Boundaries vs Opponent

**Insight:**
- Highest 4s recorded in **2011**; highest 6s in **2013 and 2014**
- Boundary frequency varies significantly across opponents, reflecting match conditions and game strategy

---

### 9. Advanced Insights

**Goal:** Identify which factors most influence Kohli's high scores, and detect patterns before and after peak performance years.

#### Factor Analysis (Venue, Position, Opponent)

- Ranked venues, opponents, and batting positions by average runs
- Plotted three horizontal bar charts side by side

**Visual:**
- 📊 3-panel chart — Top Venues / Opponents / Positions by Average Runs

**Finding:**
- **Batting Position** is the strongest predictor — Positions 3 & 4 consistently deliver the highest averages (~50)
- **Venue** is the next important factor — grounds like Fatullah and Napier show significantly higher averages
- **Opponent** has an impact but is relatively less consistent compared to position and venue

#### Before vs After Peak Year Analysis

- Automatically detected the peak year using `idxmax()` on yearly averages
- Labelled each match as "Before Peak", "Peak Year", or "After Peak"
- Computed mean Runs, SR, 4s, and 6s across all three periods
- Plotted a 2×2 grid of bar charts

**Visual:**
- 📊 2×2 bar chart grid — Runs, SR, 4s, 6s: Before Peak / Peak Year / After Peak

**Finding:** Kohli peaked in **2016** with the highest average runs. Although consistency slightly declined afterward, his game evolved to be more aggressive — with higher strike rates and increased power hitting in post-peak years.

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

