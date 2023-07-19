---
title: "Coding Elements"
date: 2023-06-07T14:19:00-04:00
draft: false
weight: 1
---

{{% expand title="**Gene**" %}}
A basic unit of heredity and a sequence of nucleotides in DNA that encodes the synthesis of a gene product, either RNA or protein.

**Possible relationships:**
```
enhancer/gene -[regulate]-> gene

gene -[transcribe_into]-> transcript

gene -[belong_to]-> gene_ontology

sequence_variant -[correlate_with]-> gene (eQTL)

gene -[express_in]-> tissue_or_cell_line

gene -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Transcript**" %}}
The product of gene transcription. Due to alternative splicing, one gene might correspond to multiple transcripts. It is also the combination of introns and exons.

**Possible relationships:**
```
gene -[transcribe_into]-> transcript

transcript -[translate_into]-> protein

transcript -[include]-> exon

transcript -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Exon**" %}}
A transcript is a set of exons in GenomicKB (from Ensembl).

**Possible relationships:**
```
transcript -[include]-> exon
```
{{% /expand %}}

{{% expand title="**Protein**" %}}
The product of RNA translation.

**Possible relationships:**
```
transcript -[translate_into]-> protein
```
{{% /expand %}}