---
title: "3D structure"
date: 2023-06-07T14:20:33-04:00
draft: false
weight: 5
---

{{% expand title="**TAD**" %}}
Topological associating domains. A self-interacting genomic region, meaning that DNA sequences within a TAD physically interact with each other more frequently than with sequences outside the TAD.

**Possible relationships:**
```
TAD -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**Loop**" %}}
In a DNA looping event, chromatin forms physical loops, bringing DNA regions into close contact. Thus, even regions that are far apart along the linear chromosome can be brought together in three-dimensional space.

Since loops have two anchor locations, positional relationships “locate_in”, “upstream”, and “downstream” might be ambiguous, only “overlap” is supported in GenomicKB (i.e., an entity overlaps with loop anchors).

**Possible relationships:**
```
loop -[overlap]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**FIRE region**" %}}
Frequently interacting regions(FIREs) is identified by studying a compendium of Hi-C datasets across 14 human primary tissues and 7 cell types.

*Ref: https://www.sciencedirect.com/science/article/pii/S2211124716314814*

**Possible relationships:**
```
FIRE_region -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}

{{% expand title="**AB compartment**" %}}
Researchers noticed that the whole genome could be split into two spatial compartments, labelled A and B, where regions in compartment A tend to interact preferentially with A compartment-associated regions than B compartment-associated ones. Similarly, regions in compartment B tend to associate with other B compartment-associated regions.

**Possible relationships:**
```
AB_compartment -[overlap/locate_in/downstream/upstream]- (any entities with coordinates)
```
{{% /expand %}}