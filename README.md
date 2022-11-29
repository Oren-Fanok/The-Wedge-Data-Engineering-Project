Wedge Project

Nice project, all sections were very doable and provided a great introduction on data engineering. I am proud of the fact I took messy incongruent data, cleaned it, uploaded it to the cloud (GBQ), queried it, and then created a database in sql from it.
Task 1

    Files for this task: Wedge Task_1A Read, Clean, Upload Wedge Files.ipynb

This code file is the beginning stage of the wedge data cleaning process. Here the program will start by reading in and unzipping 53 different data files (different delimiters, different data types, different headers). Once the files are unzipped, the code file will normalize the data types, account for null values, choose the correct delimiter, add uniform headers if needed and convert the zip file to a pandas dataframe. Once the cleaned zip file has been converted to a pandas dataframe, the cleaned dataframe is uploaded into Google Big Query.
Task 2

    Files for this task: Wedge Task 2- A Sample of Owners.ipynb

This code file will work with the cleaned Wedge Data we previously uploaded to GBQ in task 1. The code file establishes a connection to GBQ, and starts by querying a sample of Card Numbers (owners) from the data. Next the code file chooses a random sample of 400 owners from the list of card numbers recently pulled. Finally, the code file queries all of the data entries from GBQ associated with those 400 card numbers, and converts the results into a pandas dataframe. As a final step, the code file writes the pandas dataframe to a CSV output file, so as a finished product we have a CSV file containing all the data associated with our 400 card numbers.
Task 3

    Files for this task: Wedge Task 3_Creating_database.ipynb

This code file is designed to create a local SQL database from the cleaned files we uploaded into GBQ in task 1. To begin I wrote 3 individual queries in GBQ, one query for Sales by date/hour, one query for Sales by owner/year/month, and one query for Sales by product description. I saved all three resulting tables from these queries locally to my device. Now in the python code file I start by initializing a connection to sqlite3 and creating an empty database. Next I create three empty tables in my python code file, that will store the data from my 3 GBQ queries. After committing all three empty tables to sqlite3 database, I begin reading the three local files I stored from the prior GBQ queiries into the empty tables. Once each table has been filled with the correct data, I commit each file to the SQL database I initialized earlier in the python code file. As a finished result, I have a SQL database containing three tables filled with the GBQ data I recently queried.
Query Comparison Results
Query 	Your Results 	My Results 	Difference 	Rel. Diff
Total Rows 	85760071 	85760139 	68 	<1%
January 2012 Rows 	1070905 	1070907 	2 	<1%
October 2012 Rows 	1042285 	1042287 	2 	<1%
Month with Fewest 	February 	February 	Yes 	NA
Num Rows in Month with Fewest 	6556768 	6556770 	2 	<1%
Month with Most 	May 	May 	Yes 	NA
Num Rows in Month with Most 	7578369 	7578372 	3 	<1%
Null_TS 		7123792 		
Null_DT 	0 	0 	0 	0
Null_Local 		234843 		
Null_CN 	0 	0 	0 	0
Num 5 on High Volume Cards 	14987 	14987 	Yes 	NA
Num Rows for Number 5 	460625 	460630 	5 	<1%
Num Rows for 18736 	12153 	12153 	0 	0
Product with Most Rows 	banana organic 	banana organic 	Yes 	NA
Num Rows for that Product 	908637 	908639 	2 	<1%
Product with Fourth-Most Rows 	avocado hass organic 	avocado hass organic 	Yes 	NA
Num Rows for that Product 	456771 	456771 		
Num Single Record Products 	2741 	2769 	28 	1%
Year with Highest Portion of Owner Rows 	2014 	2014 	Yes 	NA
Fraction of Rows from Owners in that Year 	.7591 	.7591 	0 	0
Year with Lowest Portion of Owner Rows 	2011 	2011 	Yes 	NA
Fraction of Rows from Owners in that Year 	.7372 	.7372 	0 	0
Reflections

I thought it was pretty straight forward and I liked the finished product. As I said above, a very digestable introduction to data engineering.
