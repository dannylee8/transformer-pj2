### This is a **submodule** of our [main project 2 repository](https://github.com/EdwardReed1/revature_project_2) at [EdwardReed1](https://github.com/EdwardReed1)'s Github page.

## pj2 SparkRunner

#### I. Description
A spark runner file

#### II. Done
1. Read in json (11/13)
2. Apply nested schema (11/13)
3. Read and write to HDFS - code in src/util_HDFS.txt (11/13 - 11/14)
4. Create account at https://cloud.mongodb.com/ (11/14)
5. Create cluster, db user and load sample data (11/14)
6. Connected MongoDb - code in src/MongoDB.txt (11/14) 
7. Added TrendObj case class (name, location, rank, as_of)
8. Extract Trend names from Nested Struct(11/15)
9. Output (trend text, location, time stamp, rank, tweet volume) as a 5-tuple (11/16)
10. Write tuple as CSV file to text file (process files or directories)
11. Process data, produce single trend case class object (IV.1)

figure a:
```
          root
      |-- as_of: string (nullable = true)
      |-- created_at: string (nullable = true)
      |-- locations: array (nullable = true)
      |    |-- element: struct (containsNull = true)
      |    |    |-- name: string (nullable = true)
      |    |    |-- woeid: long (nullable = true)
      |-- trends: array (nullable = true)
      |    |-- element: struct (containsNull = true)
      |    |    |-- name: string (nullable = true)
      |    |    |-- promoted_content: string (nullable = true)
      |    |    |-- query: string (nullable = true)
      |    |    |-- tweet_volume: long (nullable = true)
      |    |    |-- url: string (nullable = true)
```

#### III. Doing
1. SQL queries (assigned: Edward)
2. Spark Streaming of Twitter request (assigned: Nahshon)
3. Generate SQL - single topic rank change over time in a specific geo
4. Generate SQL - location change of a topic over time
5. Generate index measuring proximity between geos?


#### IV. Doable
1. Produce (date, location, single-trend, rank) objects 
   * Analyze change of rank over time
   * Analyze rank and rank change between locations over time
2. Chart change graphically per topic
3. Chart location list that changes over time


#### V. Links to resources:
- Sample data (gDrive): [sample-trend-data-11_13-19_20202.tar.gz](https://drive.google.com/file/d/1fN3BjOMfke32r7TVxRaNu-1yT9JtYYah/view?usp=sharing) 823kb gzipped, 13mb unzipped.
- Larger sample data set (gDrive):  [sample-trend-data_larger_response_set.tar.gz](https://drive.google.com/file/d/1DHmJCIs2r4OK4BBj6d-uFtGiFX1jSLNO/view?usp=sharing) 2mb gzipped, 54mb unzipped.
- Consolidated all data to one file (gDrive): [sample_trend_data_whole_set.tar.gz](https://drive.google.com/file/d/1jeaPTZlcY1JbZh3W_J6T1Xv1M09eAXrp/view?usp=sharing) 3.2mb,  67mb unzipped.
