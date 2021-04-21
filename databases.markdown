---
layout: page
title: Databases
subtitle: working with databases
permalink: /databases/
hide_hero: true
---

# Database Query

**Note:** *for a Product tour and instructional videos please visit:* [vQuery Youtube Channel](https://www.youtube.com/channel/UCrLNHFgHfw3P0eqKlPLpTwQ)

### Overview

vQuery provides a lightweight interface to query databases while minimizing database overhead.

It does not keep open connections to databases. It disconnects as soon as the query execution is completed.

As a consequence it does not support transaction management. Queries are executed in auto commit mode. Once a Create/Update/Insert/Delete statement is executed you cannot issue a rollback command. If you need to revert your modifications, you must execute another query with the appropriate commands or data.

Keep in mind that the purpose of vQuery is to extract data, not to insert, update or delete, although nothing prevents the user from doing it.

In order to query a database first go to the "Connections" tab and configure a connection using the available connectors. The connection tab provides dedicated help/instructions for each connector.

The following database systems are currently supported. They can be accessed on premise or in the cloud:

- Cassandra
- MySql
- MongoDB
- Postgres
- Microsoft SQL Server
- MariaDB

<p></p>
<div align="center"><img src="/images/query_1.png" width="100%" height="100%" class="welcome_ui_img_center" /></div>

<p></p>
<div align="center"><img src="/images/Connections.png" width="100%" height="100%" class="welcome_ui_img_center" /></div>
