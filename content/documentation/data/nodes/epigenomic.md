---
title: "Epigenomic Features"
date: 2023-06-07T14:20:03-04:00
draft: false
weight: 4
---

{{% expand title="**TF binding site**" %}}
TF binding sites from ChIP-seq experiments.

**Possible relationships:**
```
TF_binding_site -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Histone binding site**" %}}
Histone binding sites from ChIP-seq experiments.

**Possible relationships:**
```
Histone_binding_site -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**DNase hypersensitivity site(DHS)**" %}}
Open chromosome regions from ChIP-seq experiments.

**Possible relationships:**
```
DNase_hypersensitivity_site -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**TF binding motif**" %}}
DNA motifs that a specific TF binds to.

**Possible relationships:**
```
TF_binding_motif -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Replication timing**" %}}
Replication timing refers to the order in which segments of DNA along the length of a chromosome are duplicated. We include early/late two-stage timing in GenomicKB.

**Possible relationships:**
```
replication_timing -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**ChromHMM state**" %}}
ChromHMM is software for learning and characterizing chromatin states. The 15-state results are included in GenomicKB.

**Possible relationships:**
```
ChromHMM_state -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}