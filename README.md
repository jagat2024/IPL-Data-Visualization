# 🏏 IPL 2022 Data Analysis & Visualization

An exploratory data analysis and visualization project based on **IPL 2022 match data**.

The goal of this project is to analyze match-level data and extract meaningful insights about teams, players, toss decisions, winning margins, venues, batting performances, and bowling performances using Python.

---

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** and **Data Visualization** on IPL 2022 match data.

The dataset contains **74 matches and 20 columns**, including information about:

* Match details
* Teams
* Venues
* Toss decisions
* Innings scores
* Match winners
* Winning margins
* Player of the Match
* Top scorers
* Bowling performances

The analysis uses Python's data analysis and visualization libraries to understand different trends in the tournament.

---

## 🎯 Objectives

The major objectives of this project are:

* Analyze IPL match results
* Find teams with the most wins
* Analyze toss decisions
* Study the relationship between toss decisions and match outcomes
* Analyze winning margins
* Identify top-performing players
* Analyze top scorers
* Analyze bowling performances
* Identify frequently used venues
* Compare wins by runs and wickets
* Extract useful insights from the dataset

---

## 🗂️ Dataset

The dataset contains **74 rows and 20 columns**.

### Important Columns

| Column                | Description              |
| --------------------- | ------------------------ |
| `match_id`            | Unique match identifier  |
| `date`                | Match date               |
| `venue`               | Match venue              |
| `team1`               | First team               |
| `team2`               | Second team              |
| `stage`               | Group, Playoff, or Final |
| `toss_winner`         | Team that won the toss   |
| `toss_decision`       | Bat or Field             |
| `first_ings_score`    | First innings score      |
| `second_ings_score`   | Second innings score     |
| `match_winner`        | Winning team             |
| `won_by`              | Runs or Wickets          |
| `margin`              | Winning margin           |
| `player_of_the_match` | Player of the Match      |
| `top_scorer`          | Highest scorer           |
| `highscore`           | Highest individual score |
| `best_bowling`        | Best bowling performer   |
| `best_bowling_figure` | Best bowling figures     |

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Plotly** — Interactive visualizations
* **Jupyter Notebook** — Analysis environment

---

## 🔍 Data Analysis Performed

### 1. Data Understanding

The dataset was initially explored using:

```python
df.head()
df.shape
df.info()
df.describe()
df.isnull().sum()
```

This helped understand the structure, data types, dimensions, and missing values.

---

### 2. Match Wins Analysis

The number of matches won by each team was calculated using:

```python
match_wins = df["match_winner"].value_counts()
```

A bar chart was then used to visualize team wins.

---

### 3. Toss Decision Analysis

The distribution of toss decisions was analyzed using:

```python
df["toss_decision"].value_counts()
```

This helped understand whether teams preferred to **bat first** or **field first** after winning the toss.

---

### 4. Winning Margin Analysis

Matches won by runs were filtered and grouped by the winning team:

```python
margin_runs = (
    df[df["won_by"] == "Runs"]
    .groupby("match_winner")["margin"]
    .mean()
)
```

This was visualized using a horizontal bar chart to compare average winning margins.

---

### 5. Player of the Match Analysis

The frequency of Player of the Match awards was analyzed to identify players who received multiple awards during the tournament.

```python
df["player_of_the_match"].value_counts().head(10)
```

---

### 6. Top Scorer Analysis

The dataset was analyzed to identify players who recorded high individual scores.

```python
df["top_scorer"].value_counts()
```

The corresponding `highscore` column was also used for performance analysis.

---

### 7. Bowling Performance Analysis

Bowling performances were explored using:

```python
df["best_bowling"].value_counts()
```

This helped identify bowlers who appeared frequently among the best bowling performers.

---

### 8. Venue Analysis

The number of matches played at different venues was analyzed using:

```python
df["venue"].value_counts()
```

This was visualized to understand the distribution of matches across venues.

---

## 📊 Visualizations

The project includes visualizations such as:

* 📈 Team-wise match wins
* 🏏 Toss decision trends
* 📊 Average winning margin
* 👑 Top Player of the Match award winners
* 🎯 Top scorers
* 🎳 Best bowling performers
* 🏟️ Matches played by venue
* 🏆 Wins by runs vs wickets

Screenshots of important visualizations can be stored inside the `images/` directory.

---

## 💡 Key Insights

The analysis explores questions such as:

1. Which teams won the most matches?
2. What was the most common toss decision?
3. How frequently did teams win after choosing to field?
4. Which teams had larger average winning margins?
5. Which players received the most Player of the Match awards?
6. Which players produced the highest individual scores?
7. Which bowlers appeared most frequently among the best bowling performances?
8. Which venues hosted the most matches?
9. How many matches were won by runs versus wickets?

The answers are derived directly from the dataset through Python-based analysis and visualization.

---

## 📁 Project Structure

```text
IPL-Data-Visualization/
│
├── data/
│   └── ipl_matches.csv
│
├── notebooks/
│   └── IPL_Data_Analysis.ipynb
│
├── images/
│   ├── matches_by_team.png
│   ├── toss_decision.png
│   ├── winning_margin.png
│   ├── top_players.png
│   └── venues.png
│
├── README.md
├── requirements.txt
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/jagat2024/IPL-Data-Visualization.git
```

### 2. Navigate into the project

```bash
cd IPL-Data-Visualization
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the environment

**Windows:**

```bash
venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/IPL_Data_Analysis.ipynb
```

and run the cells.

---

## 🚀 Future Improvements

Some possible improvements for this project:

* Add an interactive **Plotly dashboard**
* Add team-wise performance comparison
* Analyze toss winner vs match winner
* Analyze batting first vs chasing performance
* Add player performance rankings
* Add more IPL seasons
* Build a **Streamlit dashboard**
* Deploy the dashboard online
* Add interactive filters for team, venue, and season

---

## 👨‍💻 Author

**Jagat**

Engineering Student | Python | Data Analysis | Machine Learning

---

## ⭐ If you found this project useful

Feel free to ⭐ the repository and explore the notebook.
