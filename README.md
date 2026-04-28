# What Explains Winning in the NBA?

This project analyzes which team-level statistics best explain regular-season win percentage in the NBA using team-level advanced data from 2015-2024.

## Data
Team-level advanced statistics were collected using the official NBA Statistics API.
The dataset includes regular-season team metrics such as Net Rating, shooting efficiency, rebounding rates, and pace for all NBA teams across ten seasons.

A cached CSV is saved after the initial fetch to avoid repeated API calls and rate limits.

## Methodology
The analysis follows four steps:

1. **Exploratory Data Analysis (EDA)**
    Scatter plots visualize relationships between win percentage and key team metrics.

2. **Correlation Analysis**
    Pearson correlations quantify the strength of association between win percentage and each metric.

3. **Baseline Regression**
    An ordinary least squares (OLS) regression models team win percentage as a function of Net Rating.

4. **Robustness Check**
    Additional regressions test whether shooting efficiency (True Shooting Percentage) and defensive rebounding add explanatory power beyond Net Rating.

## Results
- Net Rating exhibits a very strong positive relationship with team win percentage.
- A one-point increase in Net Rating is associated with approximately a three percentage point increase in win percentage.
- Net Rating alone explains over 90% of the variation in team win percentage.
- Once Net Rating is included, shooting efficiency and defensive rebounding do not provide meaningful additional explanatory power.

## Conclusion
Net Rating is the dominant determinant of NBA team success at the season level.
The results suggest that Net Rating effectively aggregates the key components of team performance relevant to winning, leaving limited incremental value for additional metrics once point differential is accounted for.

## Notes
- The analysis focuses on regular-season performance only.
- Results do not account for injuries, strength of schedule, or playoff outcomes.
- This project is intended for educational and analytical purposes.

- NB Viewer in case github fails to load repo: https://nbviewer.org/github/karmeendesai/nba-win-percentage-analysis/blob/main/analysis.ipynb
