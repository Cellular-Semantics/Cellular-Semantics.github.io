---
title: "Agentic AI Workflows"
slug: "agentic-workflows"
description: "Evidence-grounded agentic AI tools for querying atlases, interpreting cell types, and recording annotation evidence."
summary: ""
date: 2026-07-07
lastmod: 2026-07-07
draft: false
weight: 840
toc: true
seo:
  title: ""
  description: "ask-census, Atlas-reporter and evidencell — agentic AI workflows from the Cellular Semantics team for single-cell atlas querying, cell type interpretation and evidence capture."
  canonical: ""
  noindex: false
---

We build **agentic AI workflows** that put semantic technologies and large language models to work on real single-cell problems. A common thread runs through all of them: every claim is grounded in verifiable evidence — ontology identifiers, atlas metadata, or verbatim quotes from the literature — with validation steps that catch and correct hallucination.

## ask-census

Query the [CELLxGENE Census](https://cellxgene.cziscience.com/) in plain English and have an AI coding agent do the rest. Describe the cells you want — for example "female T cells in lung tissue" or "expression of TP53 in lung fibroblasts" — and the agent resolves your terms to ontology identifiers (Cell Ontology, Uberon, MONDO, developmental stage), expands them via Ubergraph to include all relevant subtypes so you capture indirectly annotated content, resolves gene symbols to Ensembl IDs, and then either generates reviewable query code or fetches the data slice directly. It runs pre-flight cell counts, automatically relaxes over-restrictive filters that return no cells, and can enrich a retrieved slice with author-level annotations from the CL Knowledge Base.

**Status:** Usable — early release, in active development. [GitHub](https://github.com/Cellular-Semantics/ask-census)

## Atlas-reporter

Understand the terse, often cryptic cell type names used in single-cell atlases without leaving your browsing context. Atlas-reporter generates structured, literature-grounded reports for individual cell types — drawing evidence from the atlas's own paper and the studies it cites — and supports an interactive chat mode for asking questions across that literature. Every claim is backed by a verbatim quote from a source paper, and a validation step checks that each quote is a genuine substring of the cited text and that every DOI and reference actually exists, feeding failures back to the model to fix.

**Status:** In active development — usable (CLI and agentic workflows working; a validated report corpus generated). [GitHub](https://github.com/Cellular-Semantics/Atlas-reporter)

## evidencell

A knowledge base and agentic curation workflow for documenting how classical, richly described cell types (defined by morphology, electrophysiology, connectivity and markers) correspond to the molecularly defined clusters in modern transcriptomic atlases such as those from BICCN and HMBA. It treats every mapping as an evidence graph: typed nodes and edges record each proposed correspondence together with literature, atlas metadata and annotation-transfer evidence, each carrying a verbatim source quote and a machine-readable confidence level. Curation runs as a guided, gated collaboration with an AI agent, while anti-hallucination hooks block any write that fails validation and a human expert signs off at each stage — surfacing gaps and conflicts as first-class data.

**Status:** In active development — early-stage prototype. [GitHub](https://github.com/Cellular-Semantics/evidencell)
