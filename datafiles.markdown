---
layout: page
hide_hero: true
---

# Wording with data

**Note:** *for a Product tour and instructional videos please visit:* [vQuery Youtube Channel](https://www.youtube.com/channel/UCrLNHFgHfw3P0eqKlPLpTwQ)

### Overview

vQuery provides the ability to:

- Query files using SQL language
- Read files from various sources: local filesystem, network, web, ftp, cloud(Azure, Amazon, Google)
- Connect to remote Dask clusters to process data
- Merge files
- Export data to several file formats
- Export data to a remote database
- Upload files to your workspace
- Download files from your workspace

The data tab has many features including:

- Query data using a no-code interface, SQL or Pandas Dataframes
- Explore data using provided statistics and histograms
- Manipulate data
- Save data

The main approach of vQuery is to allow the user to query big or small data sources and extract a small amount of data (filtered or aggregated) that will give them the insights they are looking for.

They can extract data from local or network files, and Big Data repositories. They can do so through a no-code interface or scripting(python).

vQuery support several file types as well as protocols to access data, on Premise or in the Cloud. 

The following file formats are currently supported: csv, parquet, json, hdf5, orc and excel.

Several protocols - wich are used to access files in various repositories either local or remote - are supported including: s3fs (amazon), adlfs (Azure), gcs/gs (Google), hdfs (Hadoop), https, etc.

### Workflow

**When a file is opened, the application does not necessarily load all its data into memory.**

The amount of data loaded in memory depends on the ```Sample Rows``` setting. This settings determine how many rows will be loaded into memory.

For example, if a CSV file has 3 million rows and the ```Sample Rows``` setting is set to 10 thousands rows, only that number of rows will be loaded into memory. Which means only 10000 rows of data will be browsable through the User Interface.

The amount of data displayed in the data grid of the user interface at any given time will depend on the ```Rows per page``` setting. If the ```Rows per page``` is set to 100 then a 100 rows will be visible on the user interface. The user can navigate the results using pagination buttons.

In summary:
```File (3000000 rows) --> Application memory (10000 rows) --> User Interface (100 rows at a time)```

File sizes limit, ```Sample Rows``` and ```Rows per page``` parameters are adjustable in the settings.

**So how can a user extract the information he wants if only a sample of the file is loaded into the application?**

First of all, in the previous example, if ```Sample Rows``` is set to 3 millions, then the whole file will be loaded into memory. However this is not always possible as files sizes can be larger that the memory available to the application.

The suggested approach, is to filter or aggregate data so that they can fit in memory and vQuery has been designed around that principle.

Let's suppose our file contains 3 millions rows of information related to cars sold during the last 10 years in France. Since vQuery allows to directly query the file, the user could issue a query to select only the information he needs. For example:

```information about cars sold to married couples aged over 50 in Laval city during the first 3 months of year 2016```

Such a query would return a small subset of the file - i.e: 5000 rows - which could not only fit in the application memory, but also match the information the user was looking for in its entirety.

Aggregations usually return even a smaller number of rows, which in most cases is what the user wats: a meaningful subset of a large set of data that can easily be processed and displayed with charts or tables.

**Loading, exploration, data manipulation**

The user does not always know exactly what information a given file contains and how that information is formatted. He often goes through the sequence of steps described below:

- *Data exploration:* when a file is open the first time (and only a sample is loaded into memory), the user - with the help of the data exploration panel - has access to statistical and datatypes information that can give him a good idea of the content of the whole file.
He can issue several queries to confirm his assumptions even if he cannot load the whole file in memory. Each time he issues a query, that query is directly executed again the data file.

- *Data manipulation:* Once the data filtered/aggregated fits in memory, this enables numerous possibilities of data manipulation: change data formatting, clean and edit data, delete duplicates, update values, change column data type, further aggregate/filter and more.

- *Save data:* When the data manipulation is completed, the user can save the data in his workspace for later use.

<p></p>
<div align="center"><img src="/images/files.png" width="100%" height="100%" class="welcome_ui_img_center" /></div>

<p></p>
<div align="center"><img src="/images/data_3.png" width="100%" height="100%" class="welcome_ui_img_center" /></div>