---
layout: page
title: About vQuery
subtitle: By Laurent Esingle
permalink: /about/
---

I started this project because I could not find a simple, free and easy to deploy application that could let me connect to various database systems and query big data files effortlessly. It was intended for personal use only.

But with time I added more features and decided to make it available to others.

This free version of the application is easy to deploy, on a single machine (laptop, server) but wih one application user only.

The full version is more suited for enterprise/multi-users deployment scenarios as it includes the following features:

- multiple users
- SSL configuration
- Ability to configure and connect to a remote cluster for better scalability (process larger sets of data):
  - Under the hood vQuery uses DASK, a Python parallel computing framework that enables Big data analytics
  - With the Full version of vQuery, a separate Dask cluster can be setup using the provided vQuery-Dask container images (i.e: 1 scheduler and 2 workers)
  - Whith the Free version, everything is integrated in a single container image, which limits its ability to scale. Consequently the following limitations are set:
    - File size limit for CSV, Parquet, ORC, Json, HDF5:  10Gb
    - File size limit for Excel: 2GB
    - Maximum size of data sample:  100000 rows (see "Big data" tab for more information)
    - Maximum size of data retrieved per query from a database: 100000
- and more

If you are interested in learning more about vQuery you can use the links below:

- My email: **laurent.esingle1@outlook.com**

- My developer page on Github: **[https://github.com/LaurentEsingle](https://github.com/LaurentEsingle)**

- Twitter: **[@v_Query](https://twitter.com/vQuery_Free)**

- To see vQuery in action please visit: **[vQuery Youtube Channel](https://www.youtube.com/channel/UCrLNHFgHfw3P0eqKlPLpTwQ)**
