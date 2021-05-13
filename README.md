# Film Production Insights

Concerns Entering the Market
- Data Sources
- Directors
  - Top director’s avg budget vs avg gross
- Actors
  - Male actor recommendation
  - Female actor recommendation
- Release Dates
  - Film Gross by Month
  - Film Gross by Day in Month
    - Month of  May
    - Month of November
- Conclusion
## Data Sources

The analysis described below was conducted using the data obtained from the iMBD, The Numbers, and Box Office Mojo

## Regarding Hiring Top Directors

## Regarding Hiring Top Actors

## Regaurding Optimized Release Dates

- Define the best timeline to roll out original content
  - movies profit margin per movie by release month
  - number and gross of movies per month grouped by genre

### Best Months

Using data from the Numbers we looked at the world grossing metric for the movies based on the month they were released. The following is how the data is grouped and the relavent analysis.

```python
world_gross_per_movie_by_month = tn_df.groupby('month').sum()['worldwide_gross']/\
    tn_df.groupby('month').count()['movie']
domestic_gross_per_movie_by_month = tn_df.groupby('month').sum()['domestic_gross']/\
    tn_df.groupby('month').count()['movie']
```

The data is grouped by month of the year and total revenue for each month is divided by the total number of movies releasesd for that month to give the average gross income per movie for that month. The results are shown below.

![Gross Profit per Movie by Maonth](https://github.com/JCherryA050/phase_1_project/blob/main/images/gross_income_by_month.png)

## Conclusory Remarks
