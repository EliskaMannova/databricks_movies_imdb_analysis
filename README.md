# databricks_movies_imdb_analysis
Learning project - Databricks processing of an IMDB movies data

The original dataset contains information about 999 movies including:
 - Poster_Link
 - Series_Title
 - Released_Year
 - Certificate
 - Runtime
 - Genre
 - IMDB_Rating
 - Overview
 - Meta_score
 - Director
 - Star1
 - Star2
 - Star3
 - Star4
 - No_of_Votes
 - Gross

Project Steps:
1. Data ingestion
- Loaded raw csv file to Databricks and converted data into delta format

2.Data cleaning and transformation
- Removed spaces from genre column
- Converted genre column into an array
- Created new column called Stars with all the stars(1,2,3,4) in it, data type array
- Deleted unnecessary columns
- Extracting min from Runtime column and converting it to an integer
- Removing bad rows from a Released_Year column and converting it to an integer
- Removing commas from Gross column to be able to convert it to an integer
- Filtering all the null columns
- Counting nulls in each column to see if I should delete the rows or not
- Filling missing values in Gross with 0
- Filling missing values in certificate with 'Unknown'
- Filling missing values in Metas_score with an average
- saving a cleaned dataframe

3.Data Modeling
 - stored structured data as processed tables
 - created bronze, silver, gold schema

4.Data Analysis (SQL)

5.Saving tables in bronze, silver and gold
