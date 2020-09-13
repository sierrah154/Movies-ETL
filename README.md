<h1><center>Module 8 Challenge</h1></center>

___

## ETL : Extract, Transform, Load

___

### Objectives

- Create an automated ETL pipeline.

- Extract data from multiple sources.
  - Wikipedia, Kaggle, MovieLens

- Clean and transform the data automatically using Pandas and regular expressions.

- Load new data into PostgreSQL.

### Summary

To meet the objectives listed above, I created a function that took in three arguments:

- Wikipedia data
- Kaggle metadata
- MovieLens rating data (from Kaggle)

Then I used the code I wrote during the module's lesson and applied it to the function, so that the function would perform all of the transformation steps. I also added the lesson code I wrote for the load steps and applied it to the function. I confirmed the function worked correctly on the current Wikipedia and Kaggle data.

Several assumptions are being made in this automated ETL pipeline.

1. The uploaded data will stay in the same formats:

    - Wikipedia data in JSON format.

    - Kaggle metadata and rating data in CSV formats.

2. There are null or mostly null columns that need to be removed.
3. The list of 'alternate titles' is valid.
4. There will not be any *new* 'alternate titles' added to the data.
5. The data types will be correct when loaded into SQL.
6. When creating regular expressions for budget and box office figures, we need to capture 'million' and 'billion' as expressions.
