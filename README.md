# Overview

The Wedge Data Engineering Project is designed to be an end to end exercise in data engineering. The Wedge is a Co-op in Minneapolis that has provided customer data for analysis. I will be using 53 zipped CSV files in differing format from The Wedge for this project. The project begins with unzipping, formatting, and cleaning irregular customer transaction files from The Wedge Co Op in Minneapolis Minnesota. Once these files are cleaned, each file is pulled into a uniform pandas dataframe, (datatypes, delimiters, and headers are all uniform across the 53 customer transactions files), and uploaded to cloud storage in Google Big Query. Once the data is uploaded to GBQ I'll perform a few different analyses on the data, and finally create a local SQL database based on these results. I have gone into more detail for each of these steps in the tasks below.

# Task 1 
Files for this task:

Wedge Task_1A Read, Clean, Upload Wedge Files.ipynb

This code file is the beginning stage of the wedge data cleaning process. Here the program will start by reading in and unzipping 53 different data files (different delimiters, different data types, different headers). Once the files are unzipped, the code file will normalize the data types, account for null values, choose the correct delimiter, add uniform headers if needed and convert the zip file to a pandas dataframe. Once the cleaned zip file has been converted to a pandas dataframe, the cleaned dataframe is uploaded into Google Big Query.

# Task 2
Files for this task:

Wedge Task 2- A Sample of Owners.ipynb

This code file will work with the cleaned Wedge Data we previously uploaded to GBQ in task 1. The code file establishes a connection to GBQ, and starts by querying a sample of Card Numbers (owners) from the data. Next the code file chooses a random sample of 400 owners from the list of card numbers recently pulled. Finally, the code file queries all of the data entries from GBQ associated with those 400 card numbers, and converts the results into a pandas dataframe. As a final step, the code file writes the pandas dataframe to a CSV output file, so as a finished product we have a CSV file containing all the data associated with our 400 card numbers.

# Task 3
Files for this task:

Wedge Task 3_Creating_database (Queries).ipynb

This code file is designed to create a local SQL database from the cleaned files we uploaded into GBQ in task 1. To begin I wrote 3 individual queries in GBQ, one query for Sales by date/hour, one query for Sales by owner/year/month, and one query for Sales by product description. I saved all three resulting tables from these queries locally to my device.

# Task 4
Files for this task:

Wedge Task 4 Creating A SQL Database.ipynb

Now in the python code file I start by initializing a connection to sqlite3 and creating an empty database. Next I create three empty tables in my python code file, that will store the data from my 3 GBQ queries. After committing all three empty tables to sqlite3 database, I begin reading the three local files I stored from the prior GBQ queiries into the empty tables. Once each table has been filled with the correct data, I commit each file to the SQL database I initialized earlier in the python code file. As a finished result, I have a SQL database containing three tables filled with the GBQ data I recently queried.

# Task 5 
Files for this task:

Wedge Data Engineering Final Results.ipynb

This file will measure the accuracy of Tasks 1,2, and 3, by comparing the results of a set of queries on my data against a master set of data. Please refer to the table at the bottom of the document to see the acuracy of my work. 
