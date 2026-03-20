# Movie Studio Analysis - Group 3 Phase 2 Project

## Overview

This project analyzes movie industry data to provide actionable insights for a company looking to launch a new movie studio. Using data from IMDB and Box Office Mojo, we identify what types of films perform best at the box office and translate those findings into strategic recommendations.

---

## Business Problem

Our company sees major players creating original video content and wants to enter the movie production space. However, the company has no prior experience in film creation. We are tasked with exploring what types of films are currently doing best at the box office and providing data-driven recommendations to guide the new studio's decisions.

---

## Data Sources

This analysis uses two primary datasets:

1. **IMDB Database (`im.db`)** — A SQLite database containing:
   - `movie_basics` — movie titles, genres, and release years
   - `movie_ratings` — average ratings and number of votes
   - `directors`, `writers`, `persons`, `principals` — crew information
   - `movie_akas` — alternative movie titles by region

2. **Box Office Mojo (`bom.movie_gross.csv.gz`)** — Contains:
   - Domestic and foreign gross revenue
   - Studio information
   - Release year (2010–2018)

---

## Repository Structure

```
├── zippedData/
│   ├── im.db.zip
│   ├── bom.movie_gross.csv.gz
│   └── other data files
├── images/
│   ├── genre_gross.png
│   ├── rating_vs_gross.png
│   └── studio_gross.png
├── imdb_analysis.ipynb
├── Group 3.ipynb
└── README.md
```

---

## Methods

- Connected to IMDB SQLite database using `sqlite3`
- Loaded Box Office Mojo data using `pandas`
- Cleaned missing values in both datasets
- Merged datasets on movie title using `pandas merge` (2,447 matched movies)
- Performed Exploratory Data Analysis (EDA) with visualizations

---

## Visualizations & Key Findings

### 1. Average Total Gross by Genre

![Genre vs Gross](images/genre_gross.png)

**Finding:** Adventure-based genres dominate box office performance. The top combinations are:
- Adventure, Drama, Sport — highest average gross (~$1.2 billion)
- Adventure, Fantasy — second highest
- Adventure, Drama, Sci-Fi — third highest

Adventure appears in almost every top-performing genre combination, making it the strongest indicator of box office success.

---

### 2. Movie Rating vs Total Gross

![Rating vs Gross](images/rating_vs_gross.png)

**Finding:** There is a positive relationship between movie ratings and total gross revenue. Movies rated between 6–8 tend to earn more at the box office. However, high ratings alone do not guarantee commercial success — market appeal and genre also play a major role.

---

### 3. Average Total Gross by Studio

![Studio vs Gross](images/studio_gross.png)

**Finding:** A small group of studios consistently outperform others in average revenue. These top studios represent proven production and distribution strategies that a new studio should benchmark against.

---

## Recommendations

### Recommendation 1: Prioritize Adventure-Based Genres
The studio should focus on Adventure-based films, particularly combinations of Adventure with Drama, Fantasy, or Sci-Fi. These genres have historically generated the highest box office returns.

### Recommendation 2: Invest in Film Quality
While ratings do not perfectly predict revenue, there is a positive relationship. Investing in strong storytelling, acting, and production value improves ratings and strengthens revenue potential.

### Recommendation 3: Benchmark Top Studios
The new studio should study and benchmark against top-performing studios in terms of genre selection, production scale, and distribution strategies.

---

## Conclusion

This project demonstrates that data-driven decision-making can significantly reduce risk and improve strategic planning in the film industry. By combining IMDB and Box Office Mojo data, we identified that genre selection — particularly Adventure-based films — is the strongest driver of box office success. Studios that align creative decisions with proven market trends are better positioned for profitability.

---

## Technologies Used

- Python 3
- Pandas
- Matplotlib
- Seaborn
- SQLite3

---

## Group Members

- Alex (Alexk-creator)
- Joy (JoyN-fixer)
- [Add remaining group members]
