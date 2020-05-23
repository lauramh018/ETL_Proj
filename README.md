# ETL_Project

**Extract**: your original data sources and how the data was formatted (CSV, JSON, pgAdmin 4, etc).

We download the data from Kaggle as csv, there were 4 files.

1. movies= 81,273 rows, 22 columns. 
2. ratings= 81,273 rows, 49 columns. 
3. names= 175,719 rows, 20 columns. 
4. title_principals= 377,848 rows, 6 columns.

<table>
'imdb_title_id',
 'title',
 'original_title',
 'year',
 'date_published',
 'genre',
 'duration',
 'country',
 'language',
 'director',
 'writer',
 'production_company',
 'actors',
 'description',
 'avg_vote',
 'votes',
 'budget',
 'usa_gross_income',
 'worlwide_gross_income',
 'metascore',
 'reviews_from_users',
 'reviews_from_critics'
</table>

This kind of data is relational because in each table they have common ids like imdb_name_id and imdb_title_id

**Transform**: what data cleaning or transformation was required. 
Selection of some columns. We conclude that columns like biography or reason of death were not important for this exercise so they were deleted.

We merged the 4 files according to their ids using Pandas on Jupyter Notebooks.

**Load**: the final database, tables/collections, and why this was chosen. 
The final database was uploaded as a collection to MongoDb and we chose this option because it was easier to download the data according to a search. For this we used Pymongo and MongoDb Compass.
