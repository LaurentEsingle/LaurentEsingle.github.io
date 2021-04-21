---
layout: page
title: About vQuery
subtitle: By Laurent Esingle
permalink: /about/
---

I started this project because I could not find a simple, free and easy to deploy application that could let me connect to various database systems and query big data files effortlessly. It was intended for personal use only.

But with time I added more features and decided to make it available to others.

**Differences between the FREE and FULL versions**

This free version of the application is easy to deploy, on a single machine (i.e Laptop) but wih one application user only.

The full version is more suited for enterprise/multi-users deployment scenarios as it includes the following additional features:

- multiple users
- SSL configuration
- Ability to configure and connect to a data server for better scalability (process larger sets of data):
  - Under the hood vQuery uses DASK, a Python parallel computing framework that enables Big data analytics
  - The full version has a companion container image (vQuery-data) which acts as a data server
  - With the Full version of vQuery, the application server (vQuery container image) can be setup on one machine and the data server (vQuery-data container image) on another
  - Whith the Free version, everything is integrated in a single container image (vQuery-free), which limits its ability to scale. Consequently the following limitations are set:
    - File size limit for CSV, Parquet, ORC, JSON, HDF5:  10Gb
    - File size limit for Excel: 2GB
    - Maximum size of sample data:  100000 rows (see "Big data" tab for more information)
    - Maximum size of data retrieved per query from a database: 100000
- Databases connectors for the free version are limited to:
  - Cassandra
  - MySql
  - MongoDB
  - Postgres
  - Microsoft SQL Server
  - MariaDB

**Roadmap for the Free version:**

- Oracle database connector
- Undo feature in script editors using keyboard shortcuts (i.e: CTRL+Z)
- Code completion in script editors

**vQuery-Free support**

For features requests or to report issues and bugs:

- If you have a github account please visit the following page: [https://vqueryfree.com/issues](https://vqueryfree.com/issues)
- otherwise feel free to send an email to: *vquery@outlook.com*

**If you are interested in learning more about vQuery you can use the links below:**

- My email: *laurent.esingle1@outlook.com*

- My developer page on Github: [https://github.com/LaurentEsingle](https://github.com/LaurentEsingle)

- Twitter: [@v_Query](https://twitter.com/vQuery_Free)

- To see vQuery in action please visit: [vQuery Youtube Channel](https://www.youtube.com/channel/UCrLNHFgHfw3P0eqKlPLpTwQ)

**Credits**

This application uses open source frameworks and components. A few of them are listed below:

- jupyter notebook:  [https://jupyter.org/](https://jupyter.org/)
- Voila:  [https://github.com/voila-dashboards/voila](https://github.com/voila-dashboards/voila)
- ipymonaco:  [https://sodennis.github.io/ipymonaco/](https://sodennis.github.io/ipymonaco/)
- ipyaggrid:  [https://dgothrek.gitlab.io/ipyaggrid/](https://dgothrek.gitlab.io/ipyaggrid/)
- qgrid:  [https://github.com/quantopian/qgrid](https://github.com/quantopian/qgrid)
- plotly:  [https://plotly.com/python/plotly-express/](https://plotly.com/python/plotly-express/)
- dask:  [https://dask.org/](https://dask.org/)
