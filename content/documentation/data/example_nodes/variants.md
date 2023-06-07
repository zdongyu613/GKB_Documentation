---
title: "Variants"
date: 2023-06-07T14:19:43-04:00
draft: false
weight: 3
---

{{% expand title="**Sequence variant**" %}}
Short genomic variants (several base pairs).

**Possible relationships:**
```
sequence_variant -[correlate_with]-> gene (eQTL)

sequence_variant -[correlate_with]-> phenotype_or_disease (GWAS)

sequence_variant -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Structural variant**" %}}
Long genomic variants (several thousand base pairs)

**Possible relationships:**
```
structural_variant -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}