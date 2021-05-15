---
layout: post
title: An enhanced notebook to speed up your data analysis and visualisation tasks
subtitle: Learn how veeQuery compares to a notebook
author: Laurent Esingle
date: 2021-05-10 19:30:00
categories: general
description: "Features comparison between veeQuery and a notebook"
published: yes
canonical_url: https://vqueryfree.com/howto/2021/05/09/mongodb-data-analyis-and-visualization.html

hero_height: is-medium

image: ../images/vquery_welcome_1_flat.png
summary: |-
    This article shows how veeQuery, a free application for data analysis and visualization tasks compares to a notebook.
---

#### Introduction

If you frequently use a notebook for coding activities such as data exploration, data analysis and data visualization, then you will feel at home with veeQuery.

veeQuery can significantly increase your productivity by speeding up most task involved with the above mentioned activities.

Although less flexible and versatile than a traditional notebook, it allows you to perform those activities within a frame that suit most needs.

Now let's look in details how veeQuery might help you.

#### Extracting data from databases

**With a traditional notebook**

- You need to make sure the target database driver is installed in your system
- Then define the database connection, issue your query and display the results

The code might look like this:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_1.png" width="85%" height="85%" /></div>
<p></p>

**With veequery**

Once you have registered your connection, it is easy to:

- connect to the database
- browse tables content
- issue queries
- get the result nicely displayed in a grid

<p></p>
<div align="left"><img src="/images/enhanced_notebook_2.png" width="85%" height="85%" /></div>
<p></p>

The next step is to save database results into a file that can then be use later for data analysis and data visualization:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_3.png" width="85%" height="85%" /></div>
<p></p>

#### Reading Files

To perform Data Exploration, Data preparation and Data Analysis you usually start by loading file data into memory.

You might have to read a single file or a group of files.

**With a traditional notebook**

The code might look like this for a single file:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_4.png" width="85%" height="85%" /></div>
<p></p>

For a group of files (this is MUCH slower than with veeQuery):

<p></p>
<div align="left"><img src="/images/enhanced_notebook_5.png" width="85%" height="85%" /></div>
<p></p>

**With veequery**

Although you can also write some code on the python editor to load a file, the fastest way with veeQuery is to simply select the file on the UI and open it.
veeQuery offers the ability to load only a subset of the file's columns. This can significantly improve performance.

For a single file:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_6.png" width="85%" height="85%" /></div>
<p></p>

For a group of files (this is MUCH faster with veeQuery as it uses Dask, a Python parallel computing under the hood):

<p></p>
<div align="left"><img src="/images/enhanced_notebook_7.png" width="85%" height="85%" /></div>
<p></p>

#### Data Exploration

Some of the steps during data exploration activity usually include:

- load a file in a dataset
- get a sample of data
- find out the number of columns and their data type
- find out the number of rows
- display basic statistics such as standard deviation, mean, unique count, frequency, etc.

**With a traditional notebook**

The code might look like this:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_8.png" width="85%" height="85%" /></div>
<p></p>

**With veequery**

veeQuery automatically computes many statistics relevant to your dataset.

<p></p>
<div align="left"><img src="/images/enhanced_notebook_9.png" width="85%" height="85%" /></div>
<p></p>

<p></p>
<div align="left"><img src="/images/enhanced_notebook_10.png" width="85%" height="85%" /></div>
<p></p>

<p></p>
<div align="left"><img src="/images/enhanced_notebook_11.png" width="85%" height="85%" /></div>
<p></p>

<p></p>
<div align="left"><img src="/images/enhanced_notebook_12.png" width="85%" height="85%" /></div>
<p></p>

#### Data Preparation

Data preparation might include the following steps:

- filtering data
- Handling missing data
- Changing data types
- handling duplicates
- Formating values
- replacing values
- removing and renaming columns
- merging data
- subsetting and sorting

**With a traditional notebook**

The code might look like this:

<p></p>
<div align="left"><img src="/images/enhanced_notebook_14.png" width="85%" height="85%" /></div>
<p></p>

**With veequery**

veeQuery provide a no-code interface for some of data cleaning activities. It is also possible to generate a script from the no-code interface for later use.

For advanced funtionality, a Python code editor is available.

<p></p>
<div align="left"><img src="/images/enhanced_notebook_13.png" width="75%" height="75%" /></div>
<p></p>

<p></p>
<div align="left"><img src="/images/enhanced_notebook_15.png" width="75%" height="75%" /></div>
<p></p>

<p></p>
<div align="left"><img src="/images/enhanced_notebook_16.png" width="75%" height="75%" /></div>
<p></p>

#### Summarizing Data

This is usually the step where we extract insights from the data. We perform some computation on the data that will reduce its size to a more meaningful subset.

One way of doing this is to make aggregations.

**With a traditional notebook**

The code might look like this:

List the top five storms with the highest magnitude per timezone that occurred during April-May period group by storm type (EVENT_TYPE).