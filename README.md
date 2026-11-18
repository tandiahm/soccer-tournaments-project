# Chances, Luck and Style at International Football Tournaments

CS-215 final project (Fall 2026), by Ahmed.

The project uses StatsBomb event data from 314 matches across six recent men's tournaments: the 2018 and 2022 World Cups, Euro 2020 and 2024, AFCON 2023, and Copa América 2024. It asks three questions:
1. **What makes a shot likely to become a goal?** I built my own logistic-regression xG model, including defender positions from freeze frames.
2. **Which teams finished better or worse than expected, and were the champions lucky?** This uses a Monte Carlo simulation.
3. **Do teams fall into distinct playing styles, and has the game changed since 2018?** This uses PCA, k-means and silhouette scores.

## Repo contents
| path | what it is |
|---|---|
| `soccer_tournaments_analysis.ipynb` | the full analysis and narrative (open it in Colab) |
| `data/shots.csv` | one row per shot, with engineered features (7,622 rows) |
| `data/team_match_style.csv` | one row per team per match, with style metrics (628 rows) |
| `data/matches.csv` | match list with scores (314 rows) |
| `figures/` | the charts used in the notebook and on the project page |

## Reproducing
Open the notebook in Google Colab and choose **Runtime → Run all**. It downloads the raw StatsBomb JSON (~900 MB, about a minute) into `data/raw/`, rebuilds the CSVs, and regenerates every chart. The raw JSON isn't committed because it's too large for GitHub.

Dependencies: pandas, numpy, scikit-learn, matplotlib, requests, mplsoccer, adjustText (see `requirements.txt`).

## Data credit
[StatsBomb Open Data](https://github.com/statsbomb/open-data) (Hudl StatsBomb). Please credit StatsBomb if you reuse the data.
