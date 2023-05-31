---
title: "FAQ"
date: 2023-05-31T14:54:30-04:00
draft: false
weight: 3
---
###### **Q: Are there any requirements for user queries?**

A: User can draw customized sub-graph queries and add node property constraints. **There can only be one connected component in the query.** For example, a four-node query [A-->B, C-->D] is not allowed since two components should be submitted separately.


###### **Q: How can I know where to find a node type (e.g., gene) in the “add node” window?**

A: The hierarchical node type/relation type is shown in the tables below.


###### **Q: How can I know more information about a node/relation type? E.g., which other nodes does a gene usually connect to.**

A: In **Example nodes and edges**, users can check the example nodes/relations from all node types.


###### **Q: The database I am interested in is not covered by GenomicKB, is it possible to import it?**

A: Currently we do not support users importing their data. **But since knowledge graphs are flexible to adapt updates of nodes, relations, and entire data sources, we are open to any new data from well-established data sources.** You can suggest our team of new data sources by e-mail, and we are happy to include more!


###### **Q: How many nodes/relations are displayed on the result page?**

A: It depends on the complexity of the query. **The neo4j backend tries to find sub-graphs that match the user query. At most twenty sub-graphs will be visualized for a one-node query, ten for two-node a query, and five for queries with more nodes.** However, two identified sub-graphs might have some overlaps, and therefore ten result sub-graphs of a two-node query do not mean twenty nodes.


###### **Q: How to get a complete result?**

A: **By clicking “export”, users can download the complete result of the user query.** “Export summary” returns the count of all node/relation types, and “export all” returns the complete result graph in Microsoft Excel format.


###### **Q: The “export all” takes a long time.**

A: Exporting complete results requires searching the entire knowledge graph (with more than 300 million nodes and 1 billion relations), which is normal to take a longer time. **If the waiting time is more than 10 minutes, you can try to narrow down the results by adding node constraints** (e.g., chromosomes).