![](https://github.com/JCherryA050/phase_1_project/blob/main/images/wp5556216.jpg)

# Microsoft Studios: Rise to the Surface

## Table of Contents
1. Business Problem
2. Data Sources
3. Regarding Directors
    - Top director’s avg budget vs avg gross
4. Regarding Actors
  a. Male actor recommendation
  b. Female actor recommendation
5. Regarding Release Dates
6. Regarding Genres
  a. Most Common Genres
  b. Most Voted Genres
7. Conclusion
8. Authors

##1) Business Problem

Starting a movie studio in today's market can be extremely challenging with huge key name competitors sweeping the market. We want our studio to explode onto the scene with hit after hit by trying to identify successful trends and patterns behind what makes a movie successful. We asked ourselves the following questions:
- Who we can hire to the team?
- The type of content to create?
- What is our release date structure?

Identifying these successful trends and behaviors and then emulating them will enable our new studio to keep costs low, maximize profit, and become a mighty competitor and successful in the movie industry.

##2) Data Sources

The analysis described below was conducted using the data obtained from:
- iMBD
  - 331,703 titles
  - 73,856 ratings
  - 1,028.186 employee records
- The Numbers
  - 5,782 records
 
##3) Regarding Directors

 - Outstanding directors are an essential part of a successful movie.
 - Directors make their vision of the product come alive.
 - Create value - high ratings, awards, gross, impact on viewer.
 - Use the data to determine the highest rating Directors with an overall impressive budget to worldwide grossings.
 
###3a) Top Directors

Using the data from iMDB, we averaged the movie ratings for each director and the movies they directed. We then sorted by the highest rating directors and removed any negative profiting directors and directors with an average budget of around $200,000.00. Below is the recommended top directors with profit.

![Director's Avg Rating vs Gross](https://github.com/JCherryA050/phase_1_project/blob/main/images/Director_avg_budget_vs_avg_gross_figure_dark.png)

##4) Regarding Actors

- Actors and actresses are the face of movies.
- Consistently high performing actors and actresses will return positively received movies.
- How the consumers view the actor/actress helps in creating studio recognition.
- Determine the top rated actors who are releasing movies and are trending upwards in ratings received.

###4a) Top Actor/Actress

Using the data from iMDB, we averaged the movie ratings for each actor/actress and the movies they were in for each year and created a bar chart representing the trend of the ratings the movies they were in received. Our positively recommended actor and actress is Chris Evans and Jennifer Garner.

![Actor Recommendation](https://github.com/JCherryA050/phase_1_project/blob/main/images/Chris_evans_ratings_over_years_dark.png)

![Actress Recommendation](https://github.com/JCherryA050/phase_1_project/blob/main/images/Jennifer_garner_ratings_over_years_dark.png)

##5) Regaurding Release Dates

- Define the best timeline to roll out original content
  - Look at gross profit per movie by month

Using data from The Numbers, we looked at the world grossing metric for the movies based on the month they were released. The following is how the data is grouped and the relavent analysis.

```python
world_gross_per_movie_by_month = tn_df.groupby('month').sum()['worldwide_gross']/\
    tn_df.groupby('month').count()['movie']
domestic_gross_per_movie_by_month = tn_df.groupby('month').sum()['domestic_gross']/\
    tn_df.groupby('month').count()['movie']
```

The data is grouped by month of the year and total revenue for each month is divided by the total number of movies releasesd for that month to give the average gross income per movie for that month. Results are shown below:

![Gross Profit per Movie by Month](https://github.com/JCherryA050/phase_1_project/blob/main/images/gross_income_by_month_DARK.png)

This plot of the net prifits of films released after 1960 shows the total net profits of movies divided by the number of movies in the month that they were released. This gives an Idea of the average net profit per movie given a specific month. Judging from this comparrison, it can be concluded that the months that generally yeild the most profit for a new release are the Summer months of May, June, July and the holliday months of November and December.

##6) Regarding Genres

- Define the best genres of movies to produce
  - Look at genres that are saturated
  - Look at genres with most votes

### 6a) Most Common Genres
The data from the iMDB website was grouped by the genre and, after splicing genres, a function was applied to count the number of movies in each genre.

![Bar Plot Depicting Popular Genres](https://github.com/JCherryA050/phase_1_project/blob/main/images/number_of_movies_by_genre_DARK.png)

### 6b) Most Voted Genres
The average number of votes were gathered and sorted by genre. The average of the number of votes was taken for each genre and plotted in the table below:

![Bar Plot of the Most Voted Over Genres on iMBD](https://github.com/JCherryA050/phase_1_project/blob/main/images/number_of_genres_DARK.png)

These plots show the most made and most voted movies released after the year 1960. From these figures it can be concluded that the popular genres (Adventure, Sci-Fi, Action, Fantasy) and most made genres (Comedy, Drama) do not necessarily align. There could be a saturation in the most made movies that gives way to not one movie being singled out. It is recommended however to focus mostly on the most voted over genres as they will be in the public eye.

##7) In Conclusion

Our results of our analysis indicate that we recommend Microsoft hire top directors such as Christopher Nolan, Adrian Molina, Lee Unkrich, Pete Docter and top actor Chris Evans and top actress Jennifer Garner for our action, adventure, or sci-fi film released in May or November. Although our data indicates we should go with these people, there could be external factors that impact our results or future alternate results. For example, these recommended artists could have been cancelled on social media and current data on the movie ratings would not be sufficient to measure this. We could get data from their social media to determine their sentiment with people. We could also investigate further specific foreign markets or when to release specific genres.

##8) Authors


Aaron Cherry
- email: cherrya050@gmail.com
- LinkedIn: <a href="https://www.linkedin.com/in/aaron-cherry-8aa728124/" target="_top">https://www.linkedin.com/in/aaron-cherry-8aa728124/</a>

Erin Vu
- email: erin.vu94@gmail.com
