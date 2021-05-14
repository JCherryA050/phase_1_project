![](https://github.com/JCherryA050/phase_1_project/blob/main/images/wp5556216.jpg)

# Microsoft Studios: Rise to the Surface

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

 - Outstanding directors are an essential part of a successful movie.
 - Directors make their vision of the product come alive.
 - Create value - high ratings, awards, gross, impact on viewer.
 - Use the data to determine the highest rating Directors with an overall impressive budget to worldwide grossings.
 
### Top Directors

Using the data from iMDB, we averaged the movie ratings for each director and the movies they directed. We then sorted by the highest rating directors and removed any negative profiting directors and directors with an average budget of around $200,000.00. Below is the recommended top directors with profit.

![Director's Avg Rating vs Gross](addd link after pushing ev dark images)

## Regarding Hiring Top Actors

- Actors and actresses are the face of movies.
- Consistently high performing actors and actresses will return positively received movies.
- How the consumers view the actor/actress helps in creating studio recognition.
- Determine the top rated actors who are releasing movies and are trending upwards in ratings received.

### Top Actor/Actress

Using the data from iMDB, we averaged the movie ratings for each actor/actress and the movies they were in for each year and created a bar chart representing the trend of the ratings the movies they were in received. Our positively recommended actor and actress is Chris Evans and Jennifer Garner.

![Actor Recommendation](add link after pushing ev dark images)

![Actress Recommendation](add link after pushing ev dark images)

## Regaurding Optimized Release Dates

- Define the best timeline to roll out original content
  - Look at gross profit per movie by month

Using data from the Numbers, we looked at the world grossing metric for the movies based on the month they were released. The following is how the data is grouped and the relavent analysis.

```python
world_gross_per_movie_by_month = tn_df.groupby('month').sum()['worldwide_gross']/\
    tn_df.groupby('month').count()['movie']
domestic_gross_per_movie_by_month = tn_df.groupby('month').sum()['domestic_gross']/\
    tn_df.groupby('month').count()['movie']
```

The data is grouped by month of the year and total revenue for each month is divided by the total number of movies releasesd for that month to give the average gross income per movie for that month. Results are shown below:

![Gross Profit per Movie by Month](https://github.com/JCherryA050/phase_1_project/blob/main/images/gross_income_by_month_DARK.png)


## Regarding Common Popular Genres

- Define the best genres of movies to produce
  - Look at genres that are saturated
  - Look at genres with most votes

Using data from the iMBD, a count was taken of all of the available genres and comparisons were made. 

![Bar Plot Depicting Popular Genres](https://github.com/JCherryA050/phase_1_project/blob/main/images/number_of_movies_by_genre_DARK.png)

The average number of votes per genre was calculated and can be seen in the following figure:

![Bar Plot of the Most Voted Over Genres on iMBD](https://github.com/JCherryA050/phase_1_project/blob/main/images/number_of_genres_DARK.png)


## Conclusory Remarks


## Authors


Aaron Cherry
- email: acherrya050@gmail.com
- LinkedIn: <a href="https://www.linkedin.com/in/aaron-cherry-8aa728124/" target="_top">https://www.linkedin.com/in/aaron-cherry-8aa728124/</a>
