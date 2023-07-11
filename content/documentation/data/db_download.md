---
title: "Database Download"
date: 2023-07-11T14:35:27-04:00
draft: false
---
#### Download the entire database of GenomicKB
The database of GenomicKB is driven by Neo4j graph database. If you want to have a copy of the database, here we provide the download of the dumps of GenomicKB database:
{{% expand title="Download List" %}}
[Download: GKB DB version: 0.0.0{{% icon icon="download" %}}]()
{{% /expand %}}


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