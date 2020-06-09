# Project: Data Lake

---
## Introduction
A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

----
# The Project
To build an ETL solution that extracts data from S3 and outputs a number of files in parquet format. 

----
# Source Data
Two sources reside in S3. Here are the S3 links for each:

- **Song data**: s3://udacity-dend/song_data
- **Log data**: s3://udacity-dend/log_data

### Song Data 
Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID.
### Log Data
The second path consists of log files in JSON format based on the songs in the dataset above. The files contain app activity logs from the Sparkify music streaming app. The log files in the dataset you'll be working with are partitioned by year and month.

----
# Project Files
### dl.cfg
Contains your AWS (Secret) Access Keys

### testing code.ipynb
A notebook to help in generating the code that goes into the etl.py file. This is where tests were conducted ona  subset of the data. 

### etl.py 
Reads data from S3 into Spark and back out to parquet files.

----
# Output files
5 files are created and stored within S3
#### Fact Table
- **songplays** - records in event data associated with song plays

#### Dimension Tables
- **users** - users in the app
- **songs** - songs in music database
- **artists** - artists in music database
- **time** - timestamps of records in songplays broken down into specific units

----

