# TMDb Movie Performance Analysis

An exploratory analysis of 10,866 movies in The Movie Database (TMDb), focused on the attributes associated with inflation-adjusted revenue and the popularity of major genres.

This project was completed for the **Introduction to Data Analysis with Pandas and NumPy** course in the Data Analyst Nanodegree and polished as a portfolio-ready, reproducible report.

## Project Highlights

- Audited duplicate rows, missing values, data types, and zero-valued financial fields.
- Preserved incomplete records while using analysis-specific subsets instead of dropping rows globally.
- Reshaped pipe-separated genres into a tidy movie–genre table.
- Compared adjusted revenue with budget, popularity, audience rating, and runtime.
- Used inflation-adjusted financial fields for comparisons across release years.
- Exported the fully executed notebook as a standalone HTML report.

## Key Findings

- Adjusted budget had the strongest monotonic association with adjusted revenue in the complete financial subset (Spearman correlation approximately 0.66).
- TMDb popularity was also positively associated with adjusted revenue (approximately 0.61), but neither relationship establishes causation.
- Adventure, Fantasy, Animation, Crime, and Family had the highest median popularity among genres represented by at least 100 movies.
- Genre and decade comparisons are sensitive to TMDb's platform-specific popularity metric and missing financial data.

## Dataset

The project uses the cleaned [TMDb movie dataset supplied by Udacity](https://video.udacity-data.com/topher/2025/September/68c92ee0_tmdb-movies/tmdb-movies.csv), originally derived from TMDb data distributed through Kaggle. The snapshot covers releases from 1960 through 2015.

## Run Locally

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m jupyter lab
```

Open `Investigate_a_Dataset.ipynb` and choose **Restart Kernel and Run All Cells**. The notebook reads `tmdb-movies.csv` using a relative path.

## Repository Structure

```text
.
├── Investigate_a_Dataset.ipynb  # Executed analysis notebook
├── Investigate_a_Dataset.html   # Shareable rendered report
├── tmdb-movies.csv              # Source dataset snapshot
├── requirements.txt             # Python dependencies
└── README.md
```

## Limitations

Financial fields are missing for many records and may not be missing at random. TMDb popularity is time-sensitive, a movie can contribute to multiple genres, and the snapshot ends in 2015. The findings are descriptive associations, not causal estimates.
