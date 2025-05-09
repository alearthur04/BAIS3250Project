## Description
This folder contains the various CSV and Excel files used throughout our Jupyter notebook. Some files contain uploaded datasets used to begin our coding process, while others are saved DataFrames generated from our completed code.

## Table of Contents
| File Name | File Type | Description |
| ------ | ------ | ------ |
| IMDb_Top_250.xlsx | Excel file | This Excel file was used to save our movies_df DataFrame. We scraped data about the Top 250 Movies from the IMDb website, edited the run time to minutes, saved the data into a DataFrame, and then saved the DataFrame into the Excel file. |
| the_oscar_award.csv | CSV file | This CSV file contains data about the Oscar ceremonies spanning the years 1927 to 2025. The file was downloaded from Kaggle and read into our Jupyter Notebook for analysis. |
| the_oscar_award.xlsx | Excel file | We converted the_oscar_award.csv file into an Excel file to make horizontal integration with the IMDb_Top_250.xlsx file easier. We uploaded the_oscar_award.xlsx file into a DataFrame called oscars_data_excel. |
| cleaned_oscars_data.xlsx | Excel file | This Excel file contains the cleaned version of the oscars_data_excel DataFrame made from the_oscar_award.xlsx file. We removed missing values, created two integer columns (Nominations and Winners) based off the 'winner' column that had True/False values, and dropped all the unnecessary columns. |
| Horizontal_Integration_Films.csv | CSV file | This CSV file contains our final DataFrame after horizontal integration. We did some final data cleaning and put IMDb_Top_250.xlsx file in a new DataFrame called movies_clean and put the cleaned_oscars_award.xlsx file in a new DataFrame called oscars_clean. We then horizontally merged these two DataFrames into a new DataFrame called integrated_films and saved that in the Horizontal_Integration_Films.csv file. |
| IMDB_Top_250_raw_data.csv | CSV file | This CSV file is the same as the IMDB_Top_250.xlsx file it's just been converted into a CSV. We added the raw data description to the file name to make it clear that this file contains our raw, scraped data from the IMDb website. |
