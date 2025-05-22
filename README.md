# Music Library Analysis — Personal Apple Music Data

This project explores my personal music listening habits using data exported from Apple Music. The aim was to investigate whether features such as **genre**, **song duration**, and **date added** influence how frequently I listen to songs (measured by play count).

All analysis was conducted in Python using standard data science libraries and statistical testing.

---

## Project Overview

### Objectives:
- Clean and preprocess Apple Music library data
- Explore distributions and patterns in song play counts
- Statistically test whether features like genre, duration, and recency influence listening behavior
- Visualize results using Matplotlib and Seaborn

---

## Key Findings

> - **Play counts are not normally distributed** — a few songs dominate play frequency.
> - A **Kruskal-Wallis H-test** (p = 0.44) showed **no significant difference** in play counts across genres.
> - **Boxplots** and **KDE plots** further confirmed similar distributions across genres.
> - **Correlation and regression analysis** revealed **no strong relationships** between play count and:
>   - **Song duration**
>   - **Date added**

**Conclusion**: Listening frequency appears to be driven more by subjective preferences rather than genre, length, or recency.

---

## Tools & Libraries

- Python 3.10+
- pandas
- seaborn
- matplotlib
- scipy (for statistical testing)
- Jupyter Notebook

---

## Data Cleaning Process

- Removed songs with 0 play count
- Filtered to top 10 genres with ≥10 songs each
- Converted time and date formats
- Standardised unnecessarily splintered genres for analysis

---

## Statistical Methods Used

- **KDE plots** to inspect distribution shapes
- **Shapiro-Wilk test** to check for normality
- **Kruskal-Wallis H-test** for genre-based comparison
- **Correlation matrix** and **regression line fitting** for recency analysis

---
