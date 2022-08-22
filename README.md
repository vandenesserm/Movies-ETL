# Movies ETL
## Overview:
The goal of this project is to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. 
#
## List of requested deliverables:
- Deliverable 1: Write an ETL Function to Read Three Data Files
- Deliverable 2: Extract and Transform the Wikipedia Data
- Deliverable 3: Extract and Transform the Kaggle data
- Deliverable 4: Create the Movie Database
#
## Tools:
- GitBash
- Jupyter Notebook
- pgAdmin 4
- PostgreSQL
- Virtual Studio Code

#
## Summary: 
The following files were added into the Github repository:

The ETL_function_test.ipynb file:
- With an ETL function written to read in the three data files.
- Functions that convert the Wikipedia JSON file, the Kaggle metadata, and the MovieLens ratings to a Pandas DataFrame.

The ETL_clean_wiki_movies.ipynb file:
- That contains the wiki_movies_df DataFrame with TV shows filtered out.
- A try-except block to catch errors while extracting the IMDb IDs with a regular expression and dropping duplicate IDs.
- The following columns are cleaned in the Wikipedia DataFrame:
        - Box office
        - Budget
        - Release date
        - Running time
- ​The cleaned Wikipedia data is converted to a Pandas DataFrame.

The ETL_clean_kaggle_data.ipynb file:
- Cleaned Kaggle metadata.
- The Wikipedia and Kaggle DataFrames are merged.
    - Unnecessary columns are dropped.
    - Missing Kaggle data is filled using a function.

The ETL_create_database.ipynb file: 
- The data from the movies_df DataFrame replaces the current data in the movies table in the SQL database, as determined by the movies_query.png.
![Picture](/Resources/movies_query.png)

- The data from the MovieLens rating CSV file is added to the ratings table in the SQL database, as determined by the ratings_query.png.
![Picture](/Resources/ratings_query.png)

The elapsed time to add the data to the database is displayed in the ETL_create_database.ipynb file.
![Picture](/Resources/time_elapsed.png)