# NBA Insight — an interactive explorer over 14 seasons of box scores

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

An interactive tool for asking questions of **real NBA data (2010–2024)** — player stat lookups, head-to-head comparisons, recent-game results, and an auto-generated trivia mode — over the full regular-season and playoff box scores. CLI plus a React front end, containerized with Docker.

A note up front, because the repo name oversells it: today this is a **data-exploration and analytics tool**, not a predictive model. The "AI" is the roadmap (see below), and I'd rather say that than dress up `groupby` as machine learning.

---

## The problem

Sports fans are drowning in data but starved of *answers*. Box-score data for every NBA game is public, yet getting a specific answer — "how do these two players compare on rebounds over their careers?", "what was the highest-scoring game since 2010?" — still means stitching together broadcasts, social posts, and stat sites. **Over 75% of Gen Z sports fans say they want real-time, interactive stats tools for deeper engagement** ([Deloitte Sports Fan Insight, 2023](https://www2.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions.html)). The data is there; the *interface* to it isn't.

## Market

Fan-facing sports analytics is a large and growing space — sports analytics overall is projected past **USD 10B by the late 2020s** (MarketsandMarkets), pulled by fantasy, betting, and second-screen engagement. The won part of the market is professional/enterprise (Stats Perform, Second Spectrum); the open part is lightweight, fan-facing tools that make public data conversational. This project lives in that second category.

## What it does

- **Recent games** — a team's latest matchups, scores, and outcomes.
- **Player lookup** — season-by-season points, assists, rebounds for any player.
- **Head-to-head** — compare two players (or two teams) on average points, rebounds/assists, win %, scoring.
- **Records** — e.g. the highest single-game point total in the dataset.
- **Trivia mode** — auto-generates questions from the data ("which team had the most blocks in 2017?").

## Technical breakdown

- **Real, non-trivial data.** The full 2010–2024 box scores ship in the repo — regular season and playoffs, totals and per-game — split across multiple CSV parts because the row counts are large. The interesting work is consistent joins/filters across files with differing schemas (`personName` vs `TEAM_NAME`, `game_date` vs `GAME_DATE`).
- **Query layer** (`pandas` / `numpy`) — name-tolerant lookups (case-insensitive substring matching), date-sorted recency, and aggregate comparisons computed on the fly.
- **Two front ends** — an interactive Python CLI and a **React** web app (`frontend/`), with a **Dockerfile** so the whole thing runs reproducibly.

**Skills demonstrated:** wrangling a real multi-file dataset with inconsistent schemas; designing a forgiving query interface for messy human input (player names); and packaging a data tool with both a CLI and a web front end behind Docker.

## Roadmap — earning the "AI"

The natural next step is the predictive layer the name promises: game-outcome prediction from rolling team form, player-performance projection, and similarity search ("players most like this one") via simple embeddings over the stat vectors. The dataset already supports it; that's the honest gap between what this is and what it's named.

## Run it

```bash
pip install -r requirements.txt
python app.py            # interactive CLI

# or the containerized web app
docker build -t nba-insight . && docker run -p 8501:8501 nba-insight
```

## License

MIT — see [LICENSE](LICENSE). Author: **Azra Bano**.
