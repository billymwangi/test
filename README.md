# Movie EDA project

## Project Overview

For this project, i conducted exploratory data analysis on data from the movie industry to generate insights for business stakeholders.


* This file contains these sections:
       * Overview
       * Business Understanding
          * Include stakeholder and key business questions
       * Data Understanding and Analysis
          * Source of data
          * Description of data
          * Three visualizations (the same visualizations presented in the slides and notebook)
       * Conclusion
          * Summary of conclusions including three relevant findings

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

##### Relationship between the number of votes and the ratings


For the `movie_gross` data, I started by cleaning the data. I dropped dropped the `foreign_gross` column since it contained a huge amount of missing data making it not useful for data analysis. I then dropped the rows associated with the missing values in the `domestic_gross` column since they were just few they could be ignored and still result in good data analysis.

Afterwards i analysed the relationship showing the domestic gross performance of the top ten movie studios over the years. 
  
##### Relationship showing the domestic gross performance of the top ten movie studios over the years


### Key Points

* **Your analysis should yield three concrete business recommendations.** The ultimate purpose of exploratory analysis is not just to learn about the data, but to help an organization perform better. Explicitly relate your findings to business needs by recommending actions that you think the business (Microsoft) should take.

* **Communicating about your work well is extremely important.** Your ability to provide value to an organization - or to land a job there - is directly reliant on your ability to communicate with them about what you have done and why it is valuable. Create a storyline your audience (the head of Microsoft's new movie studio) can follow by walking them through the steps of your process, highlighting the most important points and skipping over the rest.

* **Use plenty of visualizations.** Visualizations are invaluable for exploring your data and making your findings accessible to a non-technical audience. Spotlight visuals in your presentation, but only ones that relate directly to your recommendations. Simple visuals are usually best (e.g. bar charts and line graphs), and don't forget to format them well (e.g. labels, titles).

[Presentation Content](https://github.com/learn-co-curriculum/dsc-project-presentation-content)


* Business Understanding
* Data Understanding
* Data Preparation
* Data Analysis
* Visualization
* Code Quality




