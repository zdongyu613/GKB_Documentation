---
title: "Non Coding Elements"
date: 2023-06-07T14:19:10-04:00
draft: false
weight: 2
---

{{% expand title="**Enhancer**" %}}
An enhancer is a short (50–1500 bp) region of DNA that can be bound by proteins (activators) to increase the likelihood that transcription of a particular gene will occur. Enhancers are cis-acting. They can be located up to 1 Mbp (1,000,000 bp) away from the gene, upstream or downstream from the start site.

**Possible relationships:**
```
enhancer/gene -[regulate]-> gene

enhancer -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Promoter**" %}}
A sequence of DNA to which proteins bind to initiate transcription of a single RNA transcript from the DNA downstream of the promoter. Promoters are located near the transcription start sites of genes, upstream on the DNA.

**Possible relationships:**
```
promoter -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Insulator**" %}}
A type of cis-regulatory element known as a long-range regulatory element. Insulators function either as an enhancer-blocker or a barrier, or both.

**Possible relationships:**
```
insulator -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Super enhancer**" %}}
The term 'super-enhancer' has been used to describe groups of putative enhancers in close genomic proximity with unusually high levels of Mediator binding, as measured by chromatin immunoprecipitation and sequencing (ChIP-seq).

**Possible relationships:**
```
super_enhancer -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Non coding RNA**" %}}
An RNA molecule that is not translated into a protein. Abundant and functionally important types of non-coding RNAs include transfer RNAs (tRNAs) and ribosomal RNAs (rRNAs), as well as small RNAs such as microRNAs, siRNAs, piRNAs, snoRNAs, snRNAs, exRNAs, scaRNAs and the long ncRNAs such as Xist and HOTAIR.

**Possible relationships:**
```
non_coding_RNA -[belong_to]-> gene_ontology
```
{{% /expand %}}