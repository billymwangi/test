# Movie EDA project

### Project Overview

For this project, i conducted exploratory data analysis on data from the movie industry to generate insights for business stakeholders.


### Business Understanding
The movie industry includes a number of stakeholders namely investors, movie studios, directors, producers, actors, writers, supporting staff and the fanbase or audience. Some of the business questions that might arise in the movie industry includes:-
- How investors can evaluate different movie studios depending on their revenues
- How ratings affect or are affected by different aspects of a movie
-

### Data Understanding and Analysis

#### The Data
The data used for analysis is included in the `zippedData` folder
In the folder `zippedData` are movie datasets from:

* `im.db.zip`
  * Zipped SQLite database (you will need to unzip then query using SQLite)
  * `movie_basics` and `movie_ratings` tables are most relevant
* `bom.movie_gross.csv.gz`
  * Compressed CSV file (you can open without expanding the file using `pd.read_csv`)

Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Note that the above diagram shows ONLY the IMDB data. 

#### Data Cleaning & Data Analysis
For the `movie_ratings` and `movie_basics` data, I started by cleaning the data. I dropped the rows with missing values after using the `genres` column and `original_title`. These missing values were few and would therefore not have impacted my analysis. I then replaced the missing values in the `runtime_minutes` column with the mean since it was the best measure of central tendency and the amount of missing values here was significant, so it would have been imprudent to drop the rows with missing values.

I then merged the `movie_ratings` and `movie_basics` tables since they both had a similar column named `movie_id`. Afterwards i decided to introduce a new column named `new_rating` which was made by running a function to group the different average ratings for the movies into three categories i.e. low, average and high. 

I then analysed the data to see the relationship between the runtime and ratings & the relationship between the number of votes and the ratings.

##### Relationship between the runtime and ratings
![Total runtime by ratings](https://github.com/billymwangi/test/blob/main/Total%20Runtime%20by%20Rating.png)
These results show that:-
- Movies with an average rating tend to have a longer total runtime than movies with low ratings and  movies with high ratings.
- Movies with a average rating tend to have the longest total runtime, while movies with a low rating tend to have the shortest total runtime.

These observations could be explained by several factors. For example, movies with higher ratings may be more likely to have complex or intricate plots that require a longer runtime to fully develop. Additionally, movies with higher ratings may have more nuanced characters, more intricate cinematography, or more elaborate special effects that contribute to a longer total runtime. On the other hand, movies with lower ratings may be more formulaic or simplistic, and may not require as much time to fully tell their story.

##### Relationship between the number of votes and the ratings
![Average number of votes by ratings](https://github.com/billymwangi/test/blob/main/Average%20number%20of%20votes%20by%20rating.png)
These results show that:-
- Movies with a high rating tend to receive more votes than movies with low ratings, while movies with an average rating receive an intermediate number of votes.
- Movies with a low rating tend to receive the fewest votes overall.

These observations could be explained by several factors. For example, movies with higher ratings may have a larger fan base or a more dedicated following, leading to more votes from enthusiastic viewers. Additionally, movies with higher ratings may receive more critical acclaim or positive reviews, leading to more interest from general audiences.

On the other hand, movies with lower ratings may have less widespread appeal or may receive negative reviews, leading to fewer votes overall. It is also possible that movies with an average rating may be more likely to fall between the extremes of high and low ratings, leading to a less passionate response from viewers.

For the `movie_gross` data, I started by cleaning the data. I dropped dropped the `foreign_gross` column since it contained a huge amount of missing data making it not useful for data analysis. I then dropped the rows associated with the missing values in the `domestic_gross` column since they were just few they could be ignored and still result in good data analysis.


Afterwards i analysed the relationship showing the domestic gross performance of the top ten movie studios over the years. 
  
##### Relationship showing the domestic gross performance of the top ten movie studios over the years
![Domestic gross performance of top 10 movie studios over the years](https://github.com/billymwangi/test/blob/main/Domestic%20Gross%20by%20Studio%20and%20Year.png)

For investors looking to invest in movie studios, this visualization can be further analyzed to look at the studios that have maintained their earnings year over year before making an investment

### Conclusion
From the relationship between the runtimes and ratings we can conclude that So as to prevent your movie from getting a low rating you should have a more complex or intricate plot line that draws in audiences which would lead to a highly rated movie. This recommendation would be appropriate for movie directors and writers.

From the relationship between the number of votes and the ratings we can conclude that if movie studios or producers would want their movies to be highly rated then it`s best to look at producing films that already have a fan base. This is evident in how movie studios go for books or comic books that already have a huge fan base. It is also the reason why movie studios sometimes reenact and produce sequels to their movies.

From the relationship showing the domestic gross performance of the top ten movie studios over the years we can conclude that For investors looking to invest in movie studios, this visualization can be further analyzed to look at the studios that have maintained their earnings year over year before making an investment. A high domestic gross revenue would most likely lead to rising cashflows and hence a rising stock price. If you are a film director getting the top ten movie studios to back you will most probably lead to your film grossing highly since backing of a studio with high cashflows might lead the studio to spend more money to make a better quality film and also in marketing the film.





