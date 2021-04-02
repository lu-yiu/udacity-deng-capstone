The final project completed in Udacity's Data Engineering Nanodegree

# Project Goal
#### What's the goal? What queries will you want to run? How would Spark or Airflow be incorporated? Why did you choose the model you chose?
This project aims to consolidate 4 disparate data sets into a collection of analytics tables that can be leveraged to explore US immigration behaviour, specifically to uncover a correlation (if any) between immigration numbers and local populations and temperatures. 

Spark is utilised to read in and process the data to achieve the desired analytics tables because it allows for efficient handling of big data - the immigration data set is more than 1 million rows. 

The data model was defined to minimise duplication -> reducing the storage needed for maintaining these tables. 
We chose to aggregate the immigration table by month, which yields a rich table where consumers can write simple + quick queries for maximum insights. 

# Tools
#### Clearly state the rationale for the choice of tools and technologies for the project.


# ETL Steps
#### Document the steps of the process.
1. Read in the raw data files as spark dataframes. 
2. Prep the data for analytics tables - filtering for the interested time period, only keeping relevant columns, joining data sources where needed (demographics + temperature data)
3. Write the tables to S3 as parquet files. 
4. Perform data quality checks on the tables - ensure not null ids, no duplicates, correct types. 



# Future Refreshes
#### Propose how often the data should be updated and why.

# Data Model
#### Post your write-up and final data model in a GitHub repo.

# Possible Scenarios and Solutions
#### Include a description of how you would approach the problem differently under the following scenarios:
#### * If the data was increased by 100x.
#### * If the pipelines were run on a daily basis by 7am.
#### * If the database needed to be accessed by 100+ people.
