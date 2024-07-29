---
title: "Database Download"
date: 2023-07-11T14:35:27-04:00
draft: false
weight: 3
---

{{% notice style="orange" title="Disclaimer" icon="download" %}}
The dump of GenomicKB database is **freely** available for **academic users** by following the download link. **Commercial/nonacademic users**, please reach out to us by clicking 'contact' on the same download link.
{{% /notice %}}

The database is managed by FlintBox at the University of Michigan. **Please follow the instructions to download.**
1. Choose the version you prefer to download and click the link in the “Database Dump” column in the table. You will be guided to GenomicKB’s FlintBox Page.
2. After reading and confirming the in licensing information, click “BUY” in the bottom to submit a request form.
3. The GenomicKB team will review your form within 3 working days. If approved, a link for the dump of the database will be sent to your mailbox.

{{% expand title="Download List" open="true" %}}
| Database Version | Database Dump | Meta Data |
| ---------------- | --------- | --------- |
| 1.0 | [GenomicKB 1.0 Data Dump](https://available-inventions.umich.edu/product/genomickb-a-knowledgebase-for-the-human-genome) | [Meta Data table]({{< ref "documentation/data/data_coverage.md" >}}) |


{{% /expand %}}

{{< tabs title="Usage Instructions">}}
{{% tab title="How to Load the Database"%}}
#### Neo4j Environment Settings
Before using the dump, you need to set up neo4j environment, which requires downloading the neo4j platform and java 11. Please skip this section if you’ve already had a neo4j server. 

[Neo4j Installation](https://neo4j.com/download-center/#community): Choose free **Neo4j Community Server Edition 4.4** based on your own Operating System. In the sections below, follow the instructions for community edition.

[Java 11 Installation](https://www.oracle.com/java/technologies/downloads/#java11): Scroll down to choose **Java 11** and download the correct version based on your own Operating System.

#### Load Neo4j Database Dump

Once the environment is set up, follow the instructions below to load the dump of GenomicKB into your server, replace `<…>` with your own content:

1. Open your terminal and run this command to go to the folder of neo4j server.: 
```
cd <input the path to the neo4j server directory>
```
2. Load dump file with the following command: 

If you are using a **community edition**:
```
./bin/neo4j-admin load --from=<input the path to the downloaded neo4j dump file> --database=neo4j --force
```
Attention: Neo4j community edition only hosts one database. Running this command will **overwrite your previous neo4j database**.

If you are using an **enterprise edition**:
```
./bin/neo4j-admin load --from=<input the path to the downloaded neo4j dump file> --database=<input a name for your database>
```
Attention: If you are **replacing an existing database**, you should specify `--force` at the end of the above command. Otherwise, you must **create a database** after the load operation completes. See **Create a DBMS from a Dump File** section.


Ideally, you’ll see this message if the dump file is successfully loaded: 
```
Done: <some number> files, <some number> GiB processed
```
To experiment with the dump database, see **Test Dump Database** section.

Notes:
If you are using **Neo4j v5**, you have to migrate the dump database. Please refer to [Neo4j documentation: Migration](https://neo4j.com/docs/upgrade-migration-guide/current/version-5/migration/) for more information.

For more details, please refer to [Neo4j documentation: Restore-dump](https://neo4j.com/docs/operations-manual/4.4/backup-restore/restore-dump/).

#### Create a DBMS from a Dump File
You can either create a database against the system database in the neo4j browser, or use the Neo4j Desktop.

**Neo4j Browser**

1. Start neo4j from terminal with command: 
```
./bin/neo4j console
```
2. Open the neo4j browser, by default the url should be http://localhost:7474/.
3. Type in the following commands:
```
:USE system
CREATE DATABASE <name>;
```
For more details about the CREATE DATABASE command, please refer to [Neo4j documentation: Databases](https://neo4j.com/docs/cypher-manual/4.4/administration/databases/)

**Neo4j Desktop**

In Neo4j Desktop, add the dump file to the File section for the DBMS. From the File section, open `...` the drop-down menu and select `Create new DBMS` from dump.
For more details, please refer to [Neo4j documentation: Creat from dump](https://neo4j.com/docs/desktop-manual/current/operations/create-from-dump/).

#### Test Dump Database
1. Start neo4j from terminal with command: 
```
./bin/neo4j console
```
2. Open the neo4j browser, by default the url should be `http://localhost:7474/`. If you’ve changed the port in configuration, replace 7474 with your configuration.
3. Choose `bolt://` instead of `neo4j://` in the drop down menu, and type in `localhost:7687`. If you’ve changed the port in configuration, replace 7687 with your configuration.
4. If it’s the first time you open the neo4j browser, type in **neo4j for both username and password**. Neo4j browser will then ask you to change the password. Otherwise, please type in your own password.
5. Click connect and you should be able to see nodes and edges on the left panel.
6. Visit GenomicKB Data API Doc or Neo4j Cheat Sheet for detailed instructions on how to write a query. [Neo4j Cheat Sheet](https://neo4j.com/docs/cypher-cheat-sheet/4/neo4j-community/)

{{% /tab %}}

{{< /tabs >}}
