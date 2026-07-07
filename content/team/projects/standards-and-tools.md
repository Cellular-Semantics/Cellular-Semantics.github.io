---
title: "Standards & Tools"
slug: "standards-and-tools"
description: "The Cell Annotation Schema (CAS) and tools for recording, validating and reusing cell type annotations and their evidence."
summary: ""
date: 2026-07-07
lastmod: 2026-07-07
draft: false
weight: 850
toc: true
seo:
  title: ""
  description: "Cell Annotation Schema (CAS), CAS-tools and MapMyCells2CL — a standard and tools from the Cellular Semantics team for capturing and reusing cell type annotations."
  canonical: ""
  noindex: false
---

Standards and tools that let researchers record cell type annotations — and the evidence behind them — in a consistent, machine-readable, reusable form.

## Standards

### Cell Annotation Schema (CAS)

A general, open [LinkML](https://linkml.io/) schema for cell type annotations and their supporting metadata, developed as part of the [scFAIR](https://sc-fair.org/) initiative to standardise single-cell genomics metadata. CAS lets researchers record not just the cell type labels assigned to cells, but the **rationale and evidence** behind each annotation — including marker genes used as evidence and details of automated annotation transfer. It is a compact, validatable file that links to a cell-by-gene matrix, and is structured so it can be decomposed into tabular form or flattened onto `obs` in AnnData. A limited-required-field core is complemented by extensions (e.g. BICAN and CAP).

**Status:** In development. [GitHub](https://github.com/Cellular-Semantics/cell-annotation-schema)

## Tools

### CAS-tools

A Python utility package for working with the Cell Annotation Schema, available on [PyPI](https://pypi.org/project/cas-tools/) (`pip install cas-tools`) as both a library and a command-line tool. It generates CAS from CELLxGENE h5ad files and Allen Brain Cell Atlas taxonomy tables, validates annotations and their marker genes against linked AnnData, generates tabular reports from CAS, and handles interconversion between CAS and the flattened CAP-AnnData representation used by the [Cell Annotation Platform](https://celltype.info/).

**Status:** Released. [GitHub](https://github.com/cellannotation/cas-tools)

### MapMyCells2CL

A Python library and CLI that annotates [MapMyCells](https://brain-map.org/bkp/analyze/mapmycells) output with [Cell Ontology (CL)](https://obofoundry.org/ontology/cl.html) terms. MapMyCells assigns cells to Allen Brain Atlas taxonomy nodes; this tool maps those node IDs to CL or Provisional Cell Ontology (PCL) terms, using information-content ranking to pick the most specific applicable term. It works on both CSV/JSON MapMyCells outputs and h5ad files, adding CELLxGENE-schema-compliant cell type columns.

**Status:** Usable — early release (`pip install mapmycells2cl`). [GitHub](https://github.com/Cellular-Semantics/MapMyCells2CL)

### OBASK (Ontology Based Application Starter Kit)

A framework for rapidly building ontology-driven websites and knowledge portals: it ingests ontologies and linked data and stands up faceted search, term pages and a queryable graph. OBASK underpins [Virtual Fly Brain](https://virtualflybrain.org/), the Allen [Cell Type Knowledge Explorer](https://knowledge.brain-map.org/celltypes), and ontology search on the [Cell Annotation Platform](https://celltype.info/).

**Status:** Released. [Documentation](https://obasktools.github.io/obask/)
