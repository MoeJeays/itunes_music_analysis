# Apple Music Listening Data Analysis

Quick project to look at my own listening habits from Apple Music. I wanted to figure out if things like genre, song duration, or when I added the track had anything to do with how often I listen to it (play count).

I used the iTunes XML export to get my data, then cleaned it up in Python using pandas. Focused mostly on the top 10 genres with enough songs to be worth comparing (10+ songs per genre).

After cleaning, I ran some distribution checks, statistical tests, and visualised the results with seaborn/matplotlib.

---

## Key stuff:

- Removed songs with 0 plays
- Filtered out genres with less than 10 songs
- Converted date/time formats and durations
- Looked at:
  - distribution of play counts
  - correlation with song duration and date added
  - whether genre affects play count

Statistically:  
- **Play counts are not normally distributed** — a few songs dominate play frequency.
- A **Kruskal-Wallis H-test** (p = 0.44) showed **no significant difference** in play counts across genres.
- **Boxplots** and **KDE plots** further confirmed similar distributions across genres.
- **Correlation and regression analysis** revealed **no strong relationships** between play count and date added or song length

**Conclusion**: Listening frequency appears to be driven more by subjective preferences rather than genre, length, or recency.

---

## Tools

- Python (Jupyter)
- pandas
- matplotlib
- seaborn
- scipy

---
