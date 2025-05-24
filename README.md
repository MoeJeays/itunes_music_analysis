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

---

## Statistically:  
- **The data was not normally distributed with no homogeny of variance**, as shown by distribution plots and statistical tests. This justified the use of non-parametric tests like Kruskal-Wallis, Mood's median and Levene’s.
- **Levene’s test** showed that the variance in play counts differs significantly between genres (**p ≈ 0**), and both the **Kruskal-Wallis test** and **Mood's median test** confirmed that the distributions themselves also differ significantly across genres (**p ≈ 0**). This suggests that **genre plays a role in how often I listen to music**.
- **Correlation analysis** showed no meaningful relationship between play count and **song duration** or **how long ago the song was added**, which was supported by weak slopes in regression plots.
- **Boxplots and KDE plots** visually backed up the statistical findings, with some genres having wider spreads or higher medians than others.

**Conclusion**: Genre appears to influence listening frequency, while other metadata like duration or recency doesn’t show a consistent effect.

---

## Tools and Techniques

- **Language:** Python 
- **Libraries:** `pandas`, `matplotlib`, `seaborn`, `scipy.stats`
- **Statistical Methods:**
  - Levene’s Test (for equality of variances)
  - Kruskal-Wallis H Test (for differences between genres)
  - Mood's median test (due to a large number of outlying data points)
  - Correlation & linear regression
- **Visualizations:**
  - KDE plots
  - Boxplots by genre
  - Scatterplots with regression lines

---

## Future Improvements

- Run test with a frequently used playlist rather than a whole library to test correlation
- Integrate tableau for an interactive dashboard view

---
