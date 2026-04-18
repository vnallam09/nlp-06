# Web Mining and Applied NLP

This project implements a structured EVTAL pipeline to extract, validate, transform, analyze,
and load text data from HTML web pages.

The pipeline is applied to the arXiv abstract page for
**Attention Is All You Need** (Vaswani et al., 2017) — the paper that introduced the Transformer architecture.

## Pipeline Stages

- **Extract** — fetch raw HTML from the arXiv abstract page and save it locally
- **Validate** — confirm required HTML elements (title, authors, abstract, subjects, dateline) are present
- **Transform** — extract fields, clean and normalize text using spaCy, engineer NLP features
- **Analyze** — compute token frequency distributions and generate word cloud and bar chart visualizations
- **Load** — write the analysis-ready DataFrame to a CSV file

## Paper Analyzed

| Field | Value |
|---|---|
| Title | Attention Is All You Need |
| Authors | Vaswani, Shazeer, Parmar, Uszkoreit, Jones, Gomez, Kaiser, Polosukhin |
| Subject | Computer Science > Computation and Language |
| arXiv ID | 1706.03762 |

## Key Results

| Metric | Value |
|---|---|
| Raw abstract word count | 166 |
| Token count (after cleaning) | 99 |
| Unique token count | 79 |
| Type-token ratio | 0.798 |

The cleaned abstract removes stopwords, punctuation, and casing — reducing the text by ~40%.
The most frequent tokens (`transformer`, `attention`, `translation`, `models`, `bleu`) confirm
the paper's focus on a new attention-based architecture benchmarked on machine translation tasks.

## Project Documentation Pages

- **Home** - this documentation landing page
- **NLP Evolution** - a concise discussion of NLP evolution
- **Glossary** - project terms and concepts
