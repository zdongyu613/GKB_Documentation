---
title: "Database Download"
date: 2023-07-11T14:35:27-04:00
draft: false
---

{{% notice style="orange" title="Disclaimer" icon="download" %}}
This is the disclaimer of db download
{{% /notice %}}

#### Download the entire database of GenomicKB
The database of GenomicKB is driven by Neo4j graph database. If you want to have a copy of the database, here we provide the download of the dumps of GenomicKB database:
{{% expand title="Download List" open="true" %}}
| Database Version | Neo4j | Neptune | csv | meta data |
| ---------------- | ----- | ------- | --- | --------- |
| 0.0.0 | [neo4j dump file name]() | [neptune dump file name]() | [gkb_db_0.0.0.csv]() | [0.0.0_metadata]() |

{{% /expand %}}

{{< tabs title="Usage Instructions">}}
{{% tab title="neo4j"%}}
#### Load the dump of the Neo4j database

Use the following command to load the dump of database:
```
./neo4j-admin database load --from-path=/full-path/data/dumps <database> [—overwrite-destination[=true|false]]
```
If you are **replacing an existing database**, you should specify: `—overwrite-destination=true`

If not, you must **create a database** after the load operation completes.

*For more details, please refer to [Neo4j documentation: Restore a database dump](https://neo4j.com/docs/operations-manual/current/backup-restore/restore-dump/)*

#### Create a DBMS from a dump file

You can either create database against system database in the Neo4j browser, or use the Neo4j Desktop.

###### Neo4j Browser
Open the neo4j browser, and type in the following commands:
```
:USE system
CREATE DATABASE [name];
```
*For more details about the CREATE DATABASE command, please refer to [Neo4j documentation: Creating databases](https://neo4j.com/docs/cypher-manual/current/administration/databases/#administration-databases-create-database)*

###### Neo4j Desktop
In Neo4j Desktop, add the dump file to the File section for the DBMS.
From the File section, open the `...` drop-down menu and select `Create new DBMS from dump`.

*For more details, please refer to [Neo4j documentation: Create a DBMS from a dump file](https://neo4j.com/docs/desktop-manual/current/operations/create-from-dump/)*
{{% /tab %}}

{{% tab title="neptune"%}}
load dump to neptune
{{% /tab %}}

{{% tab title="csv"%}}
csv file structure
{{% /tab %}}

{{< /tabs >}}