![](https://github.com/JCherryA050/phase_1_project/blob/main/images/title_screen.jpeg)

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
- Most Common Genres
- Foreign or Domestic Markets?
- Conclusion
## Data Sources

The analysis described below was conducted using the data obtained from the iMBD, The Numbers, and Box Office Mojo

## Regarding Hiring Top Directors

## Regarding Hiring Top Actors

## Regaurding Optimized Release Dates

- Define the best timeline to roll out original content
  - movies profit margin per movie by release month
  - number and gross of movies per month grouped by genre

### Optimal Release Months

Using data from the Numbers, we looked at the world grossing metric for the movies based on the month they were released. The following is how the data is grouped and the relavent analysis.

```python
world_gross_per_movie_by_month = tn_df.groupby('month').sum()['worldwide_gross']/\
    tn_df.groupby('month').count()['movie']
domestic_gross_per_movie_by_month = tn_df.groupby('month').sum()['domestic_gross']/\
    tn_df.groupby('month').count()['movie']
```

The data is grouped by month of the year and total revenue for each month is divided by the total number of movies releasesd for that month to give the average gross income per movie for that month. The results are shown below.

![Gross Profit per Movie by Maonth](https://github.com/JCherryA050/phase_1_project/blob/main/images/gross_income_by_month.png)

## Regarding Common Popular Genres

Using data from the iMBD, a count was taken of all of the available genres and comparisons were made.

- First, the movie genre in the data table was grouped for each movie. The

![Bar Plot Depicting Popular Genres](https://github.com/JCherryA050/phase_1_project/blob/main/images/number%20of%20movies%20by%20genre%20DARK.png)

## Regarding Foreign or Domestic Markets

Using data from The Numbers, the trend of gross income from the foreign and domestic markets is shown.

- Data was cleaned and the foreign gross was taken from the difference between the world gross and the domestic gross. The total gross income was then grouped and summed over each year.
- The line graph below shows the general trend of the foreign and domestic market from the years 1960 - 2017




## Conclusory Remarks
