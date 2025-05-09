# Description
This folder contains our Jupyter Notebook that has iur entire project code. This notebook features code used to scrape the IMDb website, load in the Oscar Awards dataset, horizontally integrate the two dataframes, and finally, perform various tests and analyses to answer our five research questions.

### Steps we took to answer our 4 questions:
1. Scraped the IMDb website (250 entries)
2. Create a movies_df dataframe and convert the runtime to minutes
   - 250 rows x 4 columns
   - Create an Excel file called 'IMDB_Top_250.xlsx'
3. Read in 'the_oscar_award.csv' file
   - 11,110 rows x 8 columns
   - Create an Excel file called 'the_oscar_award.xlsx'
   - Drop NaN values to clean the dataframe
   - Run oscars_data_excel dataframe again to ensure that the null values were removed (10,751 rows x 8 columns)
   - Groupby 'film' column and create a left join to merge the two original files
     - This will add 'Nominations' and 'Winners' to the dataframe (10,751 rows x 10 columns)
4. Drop unnecessary columns (year_film', 'year_ceremony', 'ceremony', 'category', 'canon_category', 'name')
   - Remaining columns are 'film', 'winner', 'Nominations', and 'Winners'
   - Create a new Excel file called 'cleaned_oscars_data.xlsx'
5. Prepare to horizontally integrate oscars_data_excel and movies_df
   - Double-check the shape, datatypes, and NAs of the dataframes
6. Rename columns
   - 'film' to 'Movie_Name' in oscars_data_excel
   - 'winner' to 'Winner' in oscars_data_excel
   - Add the missing columns 'Winners', 'Winner', and 'Nominations' to movies_df
   - Add the missing columns 'Year', 'Run_Time_Minutes', and 'Score' to oscars_data_excel
7. Drop duplicates, so the number of rows after horizontal integration is less than 250
8. List the movies from the IMDb top 250
9. Successfully horizontally integrate the two dataframes using pd.merge and an inner join
    - Save the file as 'Horizontal_Integration_Films.csv'
10. Perform Univariate Analysis
    - Looking at the 'Nominations' tab, find the average number of nominations across all movies, and whether or not movies fall above or at/below the average
11. Perform Bivariate Analysis
    - Answer if movies with longer runtimes are more popular than movies with shorter runtimes or vice versa
    - Find the correlation coefficient between movie runtime and score (0.28)
12. Perform a Hypothesis T-Test
    - Read in 'Horizontal_Integration_Films.csv'
    - Perform the analysis and see that there is no significant difference between non-winning movies and winning movies compared to IMDb score
13. Perform Machine Learning
    - Use Logistic Regression, Decision Tree, and two KNN tests to find the accuracy score and if older movies (before 2000) are more popular than newer movies (after 2000)
14. Perform Sentiment Analysis
    - Use this test to find the lowest and highest popularity score based on movie name as well as the sentiment over time for the year column
