


Project Title: Exploring and Analyzing Movie Data.

Project Description:
    To conduct analysis on movie data with the purpose of developing a market 
    overview for our stakeholder, Microsoft Corporation, and coming up with
    recommendations.

Data:
    In the folder `zippedData` are movie datasets from:

* Box Office Mojo
* IMDB
* Rotten Tomatoes
* TheMovieDB.org 

Setting Up Our Data:
The modules I imported were:

- pandas for data analysis
- numpy for scientific computation
- matplotlib for basic plotting
- seaborn for advanced plotting

Used read_files function to read the files from zippeddata folder and return each file as dataframes.

Key Findings:

1. When is the best time of year to release a movie?

Loading data file 'tn.movie_budgets.csv.gz' to a dataframe, this file consists of data about movies release dates, movie titles, production budgets, domestic gross, and worldwide gross. Through this data, we can analyze how the movie performed in the box office and group them by the month they released to find out most profitable month to release a movie.
Performed conversion, cleaned the data and grouped the data by month they were released and plotted a bar graph
using seaborn.

Conclusion: December is the most profitable month to release the month followed by June.


![image1.png](attachment:image.png)

2.Which Studios have the most profitable films?

Loading data file 'bom.movie_gross.csv.gz' to a dataframe, this file consists of movie titles, studios, years, domestic gross, and foreign gross. Through this data, we can analyze the best performed movies and studios.
Checked for missing values and cleaned the data, sorted the data based on domestic gross and grouped them by  
studio.
Conclusion: Buena Vista(BV) studio have the most profitable films followed by Universal(Uni.).

![image2.png](attachment:image.png)

3.How does rating of the movie affect  on other factors?
 
 Loading the files 'imdb.title.ratings.csv.gz' and 'imdb.title.basics.csv.gz' these to dataframe. 
Analyzing movie data to figure out the top rated movies we need data from title_rating and title_basics files. 
Merging dataframes on columns 'tconst' to get movie titles,ratings and assigning to a new dataframe. Performing left merge because title_rating_df have less records when compare with title_basic_df to avoid the missing data.
Sorted the data by average rating and plotted a bar graph using seaborn. 
Noticed more then 10 movies have a average rating 10, to investigate further grouped the dataframe by average rating  and counted the movies, and assigned to a new dataframe. Sorted the dataframe by average rating and plotted a line graph.
Further investigate how rating of the movie affect the profit/loss of a movie, by merging the dataframe to movie_budget dataframe. Noticed duplicate entries in dataframe with columns movie and release date. Eliminated duplicates values need by drop them from dataframe. Analyze the correlation between the rating, budget, profit/loss, runtime, start year and number votes. Creating new database and assigning those columns. Plotting a seaborn heatmap to visualize correlation of those columns.
Conclusion:
1. Average rating Vs profit/loss both have 0.16 correlation between them. Means there is a low possibility that movies with higher average rating in profits.
2. Production_budget Vs profit both have 0.65 correlation between them. Means there is a good possibility that movies with higher investments result in better revenue.
3.Start_year Vs numvotes have a negative(-0.088) correlation. Means that movie rating (numvotes) do not depend on the release year.


![image3.png](attachment:image.png)

Recommendations:

1.Plan production schedule to release the movie in December(Holiday season) for better profits.

2.The profit of the movie does not necessarily depend on high ratings of the movies, don't worry about the rating.

3.Higher production budgets are likely to have a higher profits.

blog post: https://gvijayared.medium.com/data-visualization-made-simple-using-python-seaborn-a62f87623956
