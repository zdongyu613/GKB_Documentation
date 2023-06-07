---
title: "Ontology"
date: 2023-06-07T14:20:50-04:00
draft: false
weight: 6
---

{{% expand title="**Tissue or cell line**" %}}

**Possible relationships:**
```
gene -[express_in]-> tissue_or_cell_line

tissue_or_cell_line -[subclass_of]-> tissue_or_cell_line
```
{{% /expand %}}

{{% expand title="**Gene ontology**" %}}
Gene function annotation.

**Possible relationships:**
```
gene_ontology -[subclass_of]-> gene_ontology

gene/non_coding_RNA -[subclass_of]-> gene_ontology
```
{{% /expand %}}

{{% expand title="**Phenotype or disease**" %}}
Phenotypes or diseases from experimental factor ontology.

**Possible relationships:**
```
phenotype_or_disease -[subclass_of]-> phenotype_or_disease

sequence_variant -[correlate_with]-> phenotype_or_disease (GWAS)
```
{{% /expand %}}