---
title: "Single Cell Knowledge Graph"
description: "Guides lead a user through a specific task they want to accomplish, often with a sequence of steps."
summary: ""
date: 2023-09-07T16:04:48+02:00
lastmod: 2023-09-07T16:04:48+02:00
draft: false
weight: 810
toc: true
seo:
  title: "" # custom title (optional)
  description: "" # custom description (recommended)
  canonical: "" # custom canonical URL (optional)
  noindex: false # false (default) or true
---

As part of our collaborations, we have access to a large and growing volume of consistently annotated single cell transcriptomics data for human, mouse and non-human primates.

By integrating this data, we have created a visual representation of the single cell annotations, their place within the ontology hierarchy and genes associated with this annotation.

The majority of this data is organised and stored in CZI CellxGene and annotation uses OBO-Foundry ontologies; CL, Uberon, Mondo.

The resulting graph acts as a queryable store of cell type markers and supporting evidence.

Internally we use this to identify potential gaps in the cell ontology. This enables us to add new terms that are supported by the data in the knowledge graph.

Externally, you can use this resource to search for markers and marker sets for specific cell types of interest or to quickly access a breakdown of the known functions and structural components of a cell type.

The knowledge graph is hosted on Neo4j and makes use of Cypher queries. Please see the query guide for more information on how to use this resource https://github.com/Cellular-Semantics/CL_KG/blob/c0e0fe094464123c16a3e9802f373cf1f53cc999/doc/query_guide.md


## Project Repository

- See [project repository](https://github.com/Cellular-Semantics/CL_KG) for details
