# Video Game Sales Analysis

Python analysis of 16,715 game-platform release records to examine platform lifecycles, genre performance, regional preferences, and user-rating hypotheses. Completed as TripleTen coursework for the fictional retailer Ice, with a historical 2017 marketing-planning scenario.

## Tools and methods
Python, pandas, NumPy, matplotlib, SciPy; data cleaning, missing-value analysis, grouping, visualization, Pearson correlations, and two-sided Welch’s t-tests at alpha=0.05. The recent-period analysis covers 2,233 records from 2013–2016.

## Findings from saved notebook outputs
- PS4 leads recorded 2013–2016 platform sales: **314.14 million copies**.
- Action leads total genre sales: **321.87 million copies**. Shooter has the highest displayed mean (1.246 million copies) and median (0.450 million copies) per title.
- Action accounts for 28.80% of North American and 30.12% of European sales; Role-Playing accounts for 36.26% in Japan.
- PS4 critic-score/sales correlation is **0.4066**; user-score/sales correlation is **-0.0320**.
- Xbox One vs PC mean user ratings: p=0.1476, fail to reject equal means. Action vs Sports: p≈1.446e-20, reject equal means. Failure to reject does not establish equivalence.

## Run locally
Use Python 3.10 or newer in a virtual environment:

```bash
pip install -r requirements.txt
jupyter lab
```

Obtain the course-provided `games.csv` through your authorized course access and put it in `data/games.csv`. Alternatively set `GAMES_DATA_PATH` to its path. Open `video_game_sales.ipynb` and run cells in order. The dataset is excluded from this repository; no redistribution permission is assumed.

## Data and limitations
Sales columns represent **millions of copies**, not dollars, revenue, or profit. The original columns are Name, Platform, Year_of_Release, Genre, NA_sales, EU_sales, JP_sales, Other_sales, Critic_Score, User_Score, Rating. Global total sales include all four sales columns; NA/EU/JP comparison totals exclude Other_sales.

Saved numeric outputs originate from the supplied completed coursework notebook and were not recomputed during portfolio preparation because the CSV was not supplied. The portfolio copy corrects a record-count typo, unit labels, unsupported narrative claims, test conclusions, duplicate displays, and the local data path. Old chart outputs with incorrect units were cleared and require rerunning. Original dependencies were not version-pinned; exact environment reproduction is not guaranteed.

2016 may have incomplete coverage. Missing scores and ratings can bias comparisons. Repeated titles across platforms may weaken t-test independence; no equivalence test or effect-size analysis is included. Correlation and aggregated regional shares do not establish causality. No predictive model, forecast backtest, campaign lift, or realized business outcome is claimed. This is historical analysis, not a current gaming-market assessment.

## Files
- `video_game_sales.ipynb`: analysis notebook
- `results.json`: selected saved results and provenance
- `requirements.txt`: dependencies
- `UPLOAD_GUIDE.md`: GitHub upload steps
