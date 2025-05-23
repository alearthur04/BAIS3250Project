# Description
This folder shows our data dictionary and has the links to the webistes we gathered our data from.

### Data Dictionary
| Field | Type | Description |
| ------ | ------ | ------ |
| Movie_Name | Text | Movie Title |
| Winner | Boolean | Did this movie win an Oscar or not (True or False)? |
| Run_Time_Minutes | Numeric | How long (in minutes) is the movie? |
| Year | Numeric | What year did the movie air? |
| Nominations | Numeric | How many nominations did the movie have? |
| Score | Numeric | What does IMDb rate the movie? |
| Winners | Numeric | How many times has the movie won an Oscar? |

Data Dictionary Breakdown:
- Movie_Name is simply the name of the movie, which is from the IMDb and Oscars website
- Winner is whether or not the movie has won an Oscar. We will simply say 'True' or 'False' (Boolean) based on the results
- Run_Time_Minutes is how long the movie runs for, in minutes. We originally had the movie in hours and minutes, but that caused errors in our code, so we changed it to just minutes
- Year is simply the year that the movie was released/aired
- Nominations are the number of nominations that the movie has received. This integer column was created from the orginal winner column which contained True/False values
- Score is the IMDb rating of the movie. This is out of a scale of 10. Since these movies are considered the top 250 movies of all-time, they are rated pretty high (around 8 and 9)
- Winners, not to be confused with Winner, are the number of times the movie has won an Oscar. This integer column was created from the orginal winner column which contained True/False values

## Data Websites
| Website Name | Website Link |
| ------ | ------ |
| IMDb | https://www.imdb.com/chart/top/ |
| Kaggle | https://www.kaggle.com/datasets/unanimad/the-oscar-award |
