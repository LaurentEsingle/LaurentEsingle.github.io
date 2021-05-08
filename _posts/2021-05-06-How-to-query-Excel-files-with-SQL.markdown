---
layout: post
title: How to query Excel files with SQL
subtitle: veeQuery HowTo Series - part 1
author: Laurent Esingle
date: 2021-05-06 10:50:00
categories: HowTo
description: "A simple way to query an Excel file using SQL."
published: true
canonical_url: https://vqueryfree.com/howto/2021/05/06/How-to-query-Excel-files-with-SQL.html

hero_height: is-medium

image: ../images/query_excel_files.png
summary: |-
    This article shows how to use veeQuery, a free application, to extract and explore data from Excel files.
    veeQuery can also be used to query several other types of files using SQL effortlessly.
---

#### The problem

In most situations, when we want to work with an Excel file, we just open it in Excel software.

What if we want to do some data analysis on the data contained in the file but we are not experts in data manipulation using Excel formulas? Could we use SQL languange and query Excel files in the same way we query a database?

#### About veeQuery

There are a few tools that could help with that task but we are going to tackle the challenge here using veeQuery.

veeQuery is a free application available here: **[https://vqueryfree.com](https://vqueryfree.com)**. 

You will find instructions on how to install the application on their website. The application itself contains a documentation that will help you to get used to most of its features quickly. veeQuery can do a lot more but we are going to focus on the task at hand.

#### Let's do it!

First we need to open an Excel file from the `Files` tab. If the file is not already in our workspace we can `Upload` it using the upload button. Next we click on `Open in Data` to open the file.

<p></p>
<div align="left"><img src="/images/open_excel_file.png" width="75%" height="75%" /></div>
<p></p>

On the `Data tab` that appears, we select `Dask-SQL` to open the query editor. The data from the Excel file will be automatically loaded in a table called `df`.

We can now execute SQL queries such as:

`select * from df where CZ_FIPS > 65 and MAGNITUDE_TYPE = 'EG' ;`

<p></p>
<div align="left"><img src="/images/query_excel_files.png" width="75%" height="75%" /></div>
<p></p>

And that's it! We can now proceed with Data Exploration/Data Analysis/Visulazation as needed.

#### What if my Excel file has several sheets?

On the `Files` tab, when opening the file, click on `Specify file options` then choose `sheet_name`. Type the desired sheet name i.e. `'Sheet1'`.
Note that you can also choose wich columns to load by selecting/deselecting them.

If you have any questions, suggestions, or looking for help, please join our Discord server: **[veeQuery-Discord-Server](https://discord.gg/chDcePajyV)**


