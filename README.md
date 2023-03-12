# Movie EDA project

## Project Overview

For this project, i conducted exploratory data analysis to generate insights for a business stakeholders.

### Business Problem




### The Data

In the folder `zippedData` are movie datasets from:

* `im.db.zip`
  * Zipped SQLite database (you will need to unzip then query using SQLite)
  * `movie_basics` and `movie_ratings` tables are most relevant
* `bom.movie_gross.csv.gz`
  * Compressed CSV file (you can open without expanding the file using `pd.read_csv`)
  
Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Note that the above diagram shows ONLY the IMDB data. 


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

See the [Grading](#grading) section for further explanation of these elements.

### GitHub Repository

The GitHub repository is the cloud-hosted directory containing all of your project files as well as their version history.

This repository link will be the project link that you include on your resume, LinkedIn, etc. for prospective employers to view your work. Note that we typically recommend that 3 links are highlighted (out of 5 projects) so don't stress too much about getting this one to be perfect! There will also be time after graduation for cosmetic touch-ups.

A professional GitHub repository has:


2. Commit history
   * Progression of updates throughout the project time period, not just immediately before the deadline
   * Clear commit messages
   * Commits from all team members (if a group project)
3. Organization
   * Clear folder structure
   * Clear names of files and folders
   * Easily-located notebook and presentation linked in the README



