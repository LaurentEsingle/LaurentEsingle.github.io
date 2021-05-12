---
layout: post
title: MongoDB Data Analysis and Visualization with veeQuery
subtitle: veeQuery HowTo Series - part 2
author: Laurent Esingle
date: 2021-05-09 18:50:00
categories: HowTo
description: "A simple way to do data analysis on MongoDB data."
published: true
canonical_url: https://vqueryfree.com/howto/2021/05/09/mongodb-data-analyis-and-visualization.html

hero_height: is-medium

image: ../images/mongo.png
summary: |-
    This article shows how to use veeQuery, a free application, to extract and performa data analysis and visualization with MongoDB data.
    The same can be done with other types of databases.
---

#### The Challenge

MongoDB is essentially a database system that makes it possible to store data without defining a fixed schema, which offers a lot of flexibility.

However when it comes to manipulate and analyse its data, most tools are not up to the task as they are usually made for data in a tabular format.

veeQuery offers a workaround for this as we will see below.

We will work with a tweets sample database. Each record holds more than a hundred attributes. The image below shows a document view of the records.

<p></p>
<div align="left"><img src="/images/mongo2.png" width="75%" height="75%" /></div>
<p></p>

To facilitate our data exploration, data analysis and data visualization tasks, we will convert the data into a tabular format. To accomplish this, we simply have to select the tabular view option at the top of the result pane. We can also dertermine the depth level to apply when flattening the data. Here we will choose "max" as each record has several nested pieces of data.

<p></p>
<div align="left"><img src="/images/mongo3.png" width="75%" height="75%" /></div>
<p></p>

Normally, we would only extract the fields we need, but for the sake of this tutorial, we will take all the information contained in each record.

We can now save the data as we will load it later in the Data Tab to perform data exploration an data analysis tasks.

<p></p>
<div align="left"><img src="/images/mongo4.png" /></div>
<p></p>

**Note:** we could have saved the data without converting it to tabular format. In wich case veeQuery would save it in a JSON format, instead of Parquet, Excel or CSV. veeQuery is still able to load JSON data in a tabular format but it is usually better to convert it first as can we see the result before hand, adjust the level of flattening, alter the database query to retrieve only the fields we need.

Now let's open the file in the Data tab. As usual, after opening a file we have some basic statistics displayed on the statistics panel, such as standard deviation, count, unique, missing values, frequency, histograms, etc.

<p></p>
<div align="left"><img src="/images/mongo_analysis.png" width="75%" height="75%" /></div>
<p></p>

Let's extract some insights from the data. For the sake of the demonstration, we will do it using the no-code interface, pandas and SQL. But you are free to use the method that is more convenient for you.

Fist we use the "Filters" option to select only the columns we need (see image above) and get a small subset of columns as a result:

<p></p>
<div align="left"><img src="/images/mongo_analysis2.png" width="75%" height="75%" /></div>
<p></p>

Next we use Pandas in the Python code editor to further filter our selection. We will select the tweets having english as language:

<p></p>
<div align="left"><img src="/images/mongo_analysis3.png" width="60%" height="60%" /></div>
<p></p>

**Note:** Remember that in veeQuery, once you open a file, the content of that file is referenced as `df` in code editors. To display the results of your code, simply use `show(df)` or `show(<variable_name>)` if you saved the result of your computation in that variable.

Next we will use a the SQL Query editor to aggregate the data. To do that we must first extract the number of followers per user since the this number is repeated in each tweet of that user (this is achived in the subquery), then aggregate per region (outer query):

<p></p>
<div align="left"><img src="/images/mongo_analysis4.png" width="75%" height="75%" /></div>
<p></p>

The last step is to generate a chart. We do this by saving the file and opening it in the Chart Tab.

The data grid in the Chart section allows us to edit the Data if we need to. We will use that ability to remove the trailing "(US & Canada)" words:

<p></p>
<div align="left"><img src="/images/mongo_analysis5.png" width="40%" height="40%" /></div>
<p></p>

Here is the final result showing a chart generated using the no-code interface. It is also possible to use the code editor to generate charts using Matplotlib, Plotly, or Seaborn libraries.

<p></p>
<div align="left"><img src="/images/mongo_analysis6.png" width="75%" height="75%" /></div>
<p></p>

You can now save your chart as an interactive html file or in a `png`format.

Thank you for reading and remember that veeQuery can do a lot more!
