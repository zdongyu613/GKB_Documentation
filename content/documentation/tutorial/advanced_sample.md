---
title: "Complex Query Sample"
date: 2023-11-06T15:33:30-05:00
draft: true
weight: 2
---
### first sample
First, we are going to find all GWAS variants of type II diabetes.
We will start with creating the node of type II diabetes.
![pic1](/images/tutorial_img/picture1.png?width=600px)
Then the quick add function gives us hint on the connected nodes. We are going to choose GWAS association from a sequence variant to type II diabetes.
![pic2](/images/tutorial_img/picture2.png?width=500px)
We could submit this query and get a list of result.
![pic3](/images/tutorial_img/picture3.png?width=500px)
We can also use “export” to obtain the complete query result.

### second sample
Then, let’s give more restrictions to the GWAS variant. We want to get all variants that locate in enhancers.
We need to add a node for enhancer and add an edge between them with the label “locate in”.
![pic4](/images/tutorial_img/picture4.png?width=600px)
We can also submit the query now, but we are planning to include more criteria.
Many enhancers regulate the distal genes by physical interactions in 3D space. Therefore, we want to find the examples that enhancers form 3D chromatin loops with certain genes.
To do this, we need to add two nodes - a gene and a loop.
![pic5](/images/tutorial_img/picture5.png?width=500px)
And then add two edges “overlap” from the loop to the gene and the enhancer.
![pic6](/images/tutorial_img/picture6.png?width=500px)
We can submit this query and get the example results.
![pic7](/images/tutorial_img/picture7.png?width=500px)
In this example, the SNP on chrX locates in an enhancer and forms a loop with the gene ATP2B3.

### third sample
We could even make the query more complicated. For example, we require the sequence variant to be the eQTL of the gene in pancreas.
![pic8](/images/tutorial_img/picture8.png?width=600px)
By submitting the query, we can obtain an example result. This SNP on chr16 is the eQTL of gene IRX3. It also locates in an enhancer and forms a chromatin loop with the gene. This can serve as an example of 3D interactions play an important role in gene regulation.
![pic9](/images/tutorial_img/picture9.png?width=500px)

