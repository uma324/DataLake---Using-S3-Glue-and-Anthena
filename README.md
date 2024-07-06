# DataLake-UsingS3,Glue and Anthena
Maintaining and Managing a Data Lake architecture on AWS using Amazon S3 for storage, AWS Glue for data cataloging and ETL, and Amazon Athena for querying data directly from S3.
Create a database
Configure a crawler to explore data in the S3 bucket, create tables for the csv data
Query data lake data with Amazon Athena
Steps for Reading the Data from S3 using Amazon Athena Management Console
1.Upload the CSV file to the S3 bucket — I have downloaded a sample CSV file from the Website.Now upload this CSV file to S3 and create a bucket with the name then, press “Next” for all the steps.
2.To create a database and to define a crawler we use the AWS Glue service. We can locate AWS Glue in the Analytics section. We create a database to house our glue catalog. 
A crawler is a program that connects to a data store and using a classifier determines the schema for our data. Let’s use a crawler to create multiple tables. To add a crawler, we enter the crawler’s name and click Next.
Let’s select and run this crawler now. This will queue and start the crawler. We can refresh the page to see the status of the crawler. It will take a few minutes to start and process the data. When the crawler finishes, our tables are added to the database. We select the tables from the left pane and click on the first table.
3.We query these tables with AWS Athena using SQL. Let’s launch AWS Athena. Athena needs a location to store the query output. In the settings we set this location to S3 bucket. Now we can query the database using Athena.
4.Database selected and we see the list of tables in this database. Let’s query the product’s table to make sure it has data. The query runs successfully and we see the product’s data. We can perform data analysis in AWS Athena using SQL against this data lake.
