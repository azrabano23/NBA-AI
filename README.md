# 🏀 NBA AI: Interactive Basketball Insight Program

Welcome to **NBA AI**, your all-in-one interactive command-line tool that empowers NBA fans to explore player stats, team performance, and trivia using real data from 2010 to 2024. Whether you're studying the game, debating stats with friends, or prepping for sports trivia, this tool has you covered.

---

## 📌 Problem Statement

In the age of data, NBA fans still lack easy access to **personalized**, **interactive**, and **data-driven tools** for answering simple yet exciting questions about their favorite teams and players.

> 🔍 *Most fans rely on fragmented sources like social media, sports sites, or broadcasts, which don’t offer on-demand answers to custom queries.*  
>  
> 🏀 *Meanwhile, over 75% of Gen Z sports fans express interest in real-time and interactive stats tools for deeper engagement.*  
> — *(Deloitte Sports Fan Insight Report, 2023)*

---

## 🚀 What the Program Does

The `NBA_Fan_AI.py` program pulls from comprehensive NBA datasets to offer:

### ✅ Game & Player Insights
- **Recent Game Results**: View a team’s most recent matchups, scores, and outcomes.
- **Player Stats Lookup**: Pull season-by-season game stats like points, assists, and rebounds.

### 🥇 Smart Comparisons
- **Compare Players**: Evaluate two players head-to-head based on average points, rebounds, and assists.
- **Compare Teams**: Analyze team performance by comparing win percentage and scoring averages.

### ❓ Fun Trivia Generator
- Auto-generates trivia questions such as:
  - "Which team had the most blocks in 2017?"
  - "Which player scored the most points in a single game?"
  - "Who led the league in wins in 2020?"

---

## 🧠 Technical Specifications

### 🔧 Programming Language
- **Python 3.x**

### 📂 Datasets Used (included in this repo)
- `regular_season_box_scores_2010_2024_part_1.csv`
- `play_off_box_scores_2010_2024.csv`
- `regular_season_totals_2010_2024.csv`

### 📚 Libraries & Tools
| Category              | Libraries Used                       |
|-----------------------|--------------------------------------|
| Data Manipulation     | `pandas`, `numpy`                    |
| Display & Interaction | `IPython.display`, `input()`        |
| Randomization         | `random`                             |

---

## 🖥️ How to Run

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/nba-fan-ai.git
   cd nba-fan-ai
   ```

2. **Install Required Libraries** (if not already installed):
   ```bash
   pip install pandas numpy
   ```

3. **Make Sure CSV Files Are in the Same Folder**

4. **Run the Program**:
   ```bash
   python NBA_Fan_AI.py
   ```

---

## 🎯 Target Audience

- 🧑‍💻 **Sports Analytics Enthusiasts**
- 👩‍🏫 **Students and Educators** learning data science through real-world sports data
- 🎮 **Fantasy League Players** making informed decisions
- 🗣️ **Casual NBA Fans** who love stats and trivia

---

## 📁 Output Example

Choose an option: 2
Enter player name: Stephen Curry

season_year  game_date     teamName     points  assists  reboundsTotal
2022         2022-12-15    Warriors     38      7        5
...
```
---

# NBA-Data-2010-2024 🏀
This dataset contains CSV files containing comprehensive NBA data spanning from the year 2010 to 2024, offering valuable insights into player statistics, team performances, game outcomes, and more.


## Authors of Dataset
[@NocturneBear](https://github.com/NocturneBear)

## License
[MIT](https://github.com/NocturneBear/NBA-Data-2010-2024/blob/main/LICENSE)
