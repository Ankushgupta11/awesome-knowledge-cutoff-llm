# GitHub Implementations and Open-Source Projects

This file lists open-source repositories that can help implement or reproduce retrieval, RAG, scholarly search, and LLM-based research workflows.

## 1. Awesome Refreshing LLMs

**Repository:** https://github.com/hyintell/awesome-refreshing-llms

**Purpose:** Curated collection of research on refreshing or updating LLM knowledge.

**Why relevant:** This repository is directly aligned with the research problem of keeping LLM knowledge current as the external world changes.

**Use in this project:** Useful as a starting point for discovering methods addressing knowledge freshness and model updating.

---

## 2. LangChain

**Repository:** https://github.com/langchain-ai/langchain

**Purpose:** Framework for building LLM applications with retrieval, tools, agents, document loaders, and chains.

**Why relevant:** A literature-review assistant can use retrieval components to obtain current papers instead of relying exclusively on parametric model knowledge.

**Use in this project:** Useful for prototyping a retrieval-grounded literature-review pipeline.

---

## 3. LlamaIndex

**Repository:** https://github.com/run-llama/llama_index

**Purpose:** Data framework for connecting LLMs with documents, indexes, retrieval systems, and external data.

**Why relevant:** Literature reviews require document ingestion, indexing, retrieval, and evidence-grounded synthesis.

**Use in this project:** Useful for creating a local research-paper index and querying it with an LLM.

---

## 4. Pyserini

**Repository:** https://github.com/castorini/pyserini

**Purpose:** Reproducible information-retrieval toolkit supporting sparse and dense retrieval experiments.

**Why relevant:** It provides conventional retrieval baselines that can be compared with LLM-driven search and RAG.

**Use in this project:** Useful for measuring whether an LLM retrieves the correct recent literature.

---

## 5. Haystack

**Repository:** https://github.com/deepset-ai/haystack

**Documentation:** https://haystack.deepset.ai/

**Purpose:** Framework for building search, RAG, question-answering, and document-processing applications.

**Why relevant:** Literature-review systems can use pipelines for retrieval, ranking, generation, and evaluation.

**Use in this project:** Useful for building modular research-assistant pipelines.

---

## 6. DSPy

**Repository:** https://github.com/stanfordnlp/dspy

**Purpose:** Framework for programming and optimizing LLM-based systems using declarative modules and evaluation.

**Why relevant:** Literature-review generation benefits from structured pipelines rather than a single unconstrained prompt.

**Use in this project:** Useful for experimenting with structured retrieval, synthesis, and evaluation workflows.

---

## 7. OpenAlex

**Repository / API resources:** https://github.com/ourresearch/openalex-api-tutorials

**Purpose:** Resources for working with OpenAlex scholarly metadata.

**Why relevant:** A literature-review system needs programmatic access to current scholarly metadata.

**Use in this project:** Useful for constructing time-aware collections of papers and citation information.

---

## Selection Criteria

Repositories were selected based on:

- Relevance to retrieval or literature research.
- Availability of source code.
- Documentation.
- Reproducibility potential.
- Connection to recognized research tools or methods.
- Usefulness for building or evaluating knowledge-grounded LLM systems.

## Suggested Implementation

A practical student project could combine:

```text
OpenAlex / Semantic Scholar / arXiv
              ↓
        Paper Retrieval
              ↓
      Metadata Validation
              ↓
        Local Paper Index
              ↓
        RAG / LLM System
              ↓
       Literature Review
              ↓
    Claim + Citation Audit
```
