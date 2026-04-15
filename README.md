# Python for Synthetic Biology

A Quarto book project for teaching Python through synthetic biology workflows.

## What this project is

This repository contains a book-in-progress that combines:

- practical Python tutorials
- synthetic biology concepts and workflows
- executable code examples
- case studies inspired by tools and projects from:
  - RudgeLab
  - MyersResearchGroup
  - Gonza10V
  - the future DRAGGON Lab vision

The target style is a technical, example-driven book where every important concept is paired with code, explanation, and visible output.

## Core goals

- teach Python from a synthetic biology perspective
- use real software tools as motivating examples
- connect beginner-friendly code to research-grade workflows
- make the book itself a platform for developing reusable tooling alongside the text

## Book shape

The first version is organized into five parts:

1. Foundations
2. Biological Data in Python
3. Models, Standards, and Design Automation
4. Tooling and Workflows from Real Labs
5. Building the Future Lab

## Local development

### Prerequisites

- Quarto
- Python 3.11+
- Jupyter

### Recommended setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -U pip jupyter numpy pandas matplotlib networkx biopython
```

### Preview the book

```bash
quarto preview
```

### Render the book

```bash
quarto render
```

## Repository layout

```text
.
├── _quarto.yml
├── index.qmd
├── preface.qmd
├── roadmap.qmd
├── references.qmd
├── styles.css
├── chapters/
│   ├── 01-why-python-for-synbio.qmd
│   ├── 02-python-basics-for-biologists.qmd
│   ├── 03-jupyter-and-reproducibility.qmd
│   ├── 04-sequences-as-data.qmd
│   ├── 05-tabular-experimental-data.qmd
│   ├── 06-networks-circuits-and-graphs.qmd
│   ├── 07-modeling-gene-expression.qmd
│   ├── 08-design-build-test-learn.qmd
│   ├── 09-sbol-and-tooling.qmd
│   ├── 10-rudgelab-case-studies.qmd
│   ├── 11-myers-lab-case-studies.qmd
│   ├── 12-personal-projects.qmd
│   ├── 13-draggon-lab-vision.qmd
│   └── 14-capstone-projects.qmd
├── PRODUCT.md
├── ARCHITECTURE.md
├── AGENT.md
└── docs/
```

## Working approach

- keep chapters executable
- prefer small examples over giant notebooks
- keep code examples reusable as standalone teaching assets
- evolve companion tools in `tools/` as the book matures

## How to use the planning docs

- `PRODUCT.md` explains the reader, goals, and scope
- `ARCHITECTURE.md` explains how the repo should be organized
- `AGENT.md` explains how ChatGPT and coding agents should collaborate on this repo
- `ADR-001.md` records the main structural decision for the book
