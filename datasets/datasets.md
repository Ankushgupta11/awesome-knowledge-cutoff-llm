# Datasets and Scholarly Data Sources

This file lists datasets and scholarly data sources that can support research on knowledge cutoff effects, literature retrieval, scientific text processing, citation analysis, and LLM-generated literature reviews.

## 1. S2ORC — Semantic Scholar Open Research Corpus

**Source:** Allen Institute for AI / Semantic Scholar

**Link:** https://allenai.org/data/s2orc

**Description:** S2ORC is a large structured corpus of scientific papers containing scholarly text and metadata. It is designed for research involving scientific document understanding and information retrieval.

**Potential use in this topic:**
- Build literature-retrieval benchmarks.
- Test whether an LLM can find relevant papers.
- Compare old and newly published literature.
- Study citation networks and scholarly relationships.
- Construct temporal literature-review evaluation sets.

**Why relevant:** Literature-review systems need a large and structured scientific corpus against which retrieval and synthesis can be evaluated.

---

## 2. arXiv Dataset / Metadata

**Source:** arXiv

**Link:** https://www.kaggle.com/datasets/Cornell-University/arxiv

**Official repository:** https://arxiv.org/

**Description:** arXiv provides a large collection of scientific preprints across computer science, mathematics, physics, statistics, and related areas. Its rapidly updated stream makes it particularly useful for studying temporal knowledge.

**Potential use in this topic:**
- Create time-sliced literature collections.
- Evaluate LLMs on papers published after a defined knowledge boundary.
- Study rapidly emerging research topics.
- Test retrieval and summarization systems on recent papers.
- Build temporal benchmarks.

**Why relevant:** A continuously expanding preprint source is naturally suited to studying the gap between static model knowledge and newly published research.

---

## 3. OpenAlex

**Source:** OpenAlex

**Link:** https://openalex.org/

**Documentation:** https://docs.openalex.org/

**Description:** OpenAlex is an open catalog of scholarly works, authors, institutions, venues, concepts, and citation relationships.

**Potential use in this topic:**
- Discover papers by topic.
- Retrieve bibliographic metadata.
- Analyze citation networks.
- Construct temporal research collections.
- Identify recent papers in rapidly evolving fields.
- Deduplicate and enrich scholarly records.

**Why relevant:** High-quality metadata is essential when evaluating whether an LLM generated a real paper, correct author list, correct year, and correct venue.

---

## 4. Semantic Scholar Academic Graph

**Source:** Semantic Scholar

**Link:** https://www.semanticscholar.org/

**API:** https://www.semanticscholar.org/product/api

**Description:** Semantic Scholar provides scholarly publication, author, citation, and venue data through its search system and Academic Graph API.

**Potential use in this topic:**
- Retrieve relevant literature.
- Examine citation relationships.
- Build paper recommendation systems.
- Compare LLM-selected references against scholarly databases.
- Retrieve metadata for citation verification.

**Why relevant:** Semantic Scholar is particularly useful for combining discovery, metadata, citations, and relevance signals.

---

## 5. Crossref Metadata

**Source:** Crossref

**Link:** https://www.crossref.org/

**API:** https://api.crossref.org/

**Description:** Crossref provides metadata for scholarly publications registered with Crossref members, including DOI information.

**Potential use in this topic:**
- Verify DOI records.
- Check titles, authors, publication dates, and venues.
- Detect citation metadata errors.
- Validate AI-generated references.
- Build automated citation-integrity checks.

**Why relevant:** The citation audit associated with this project emphasizes that an identifier should be checked rather than trusted merely because an AI system generated it.

---

## Suggested Dataset Strategy

For a temporal literature-review experiment, a useful setup is:

```text
Historical Papers ─────┐
                      ├──> LLM Literature Review ──> Evaluation
Recent Papers ─────────┤
                      │
Metadata + Citations ──┘
```

Evaluation can measure:

- Retrieval recall
- Precision of retrieved papers
- Recency coverage
- Citation correctness
- Citation completeness
- Claim-to-source support
- Missing important papers
- Hallucinated references
- Temporal awareness
- Human-rated usefulness
