# ARCHITECTURE

## System context

This repository is a Quarto book project with executable Python examples. The repo should support:

- authoring chapters in markdown plus code
- rendering a browsable HTML book
- organizing examples so they can later become reusable Python packages or notebooks

## Major components

### 1. Book source

Quarto source files live at the repository root and in `chapters/`.

Responsibilities:
- chapter content
- code cells
- cross references
- bibliography and references

### 2. Companion tooling

The `tools/` directory is reserved for code that grows alongside the book.

Responsibilities:
- reusable helper functions
- teaching utilities
- prototype synbio software extracted from chapter examples

### 3. Rendered site

The rendered book output should go to `docs/` so it can be published easily.

### 4. Data examples

Later versions should add `data/` for small example datasets and `notebooks/` for exploratory materials that are not part of the main chapter flow.

## Content boundaries

### Chapters
- stable, reader-facing narrative
- polished examples
- reproducible outputs

### Tools
- reusable code shared across chapters
- utility functions that would otherwise be duplicated
- code that may evolve into standalone packages

### Notebooks
- scratch work, exploration, workshops, and drafts

## Recommended Quarto model

- each chapter is a single `.qmd` file
- the table of contents is defined centrally in `_quarto.yml`
- Python code execution is enabled through Jupyter
- figures are rendered directly from code when possible

## Key flows

### Authoring flow
1. Draft a chapter in `chapters/`.
2. Add or refine code cells.
3. Extract repeated logic into `tools/`.
4. Preview with `quarto preview`.
5. Render to `docs/`.

### Tool growth flow
1. A chapter introduces a useful function.
2. The function is promoted into `tools/`.
3. Chapters import the helper.
4. If the helper grows enough, it becomes its own package.

## Operational concerns

### Reproducibility
- keep code examples lightweight
- prefer pinned dependencies later via `requirements.txt` or `pyproject.toml`
- avoid examples that require private infrastructure

### Testing
- basic smoke tests for helper code in `tools/`
- chapter rendering should be checked regularly

### Documentation
- update README and chapter roadmap whenever structure changes

### Security and licensing
- prefer permissive dependencies
- clearly track external example provenance
- avoid embedding code with unclear licensing

## Risks

- the scope can expand too quickly across biology, software, and pedagogy
- chapters may become notebook dumps instead of teaching text
- case studies can overwhelm the through-line unless structured consistently

## Open questions

- whether to ship notebooks as first-class artifacts from v1
- whether companion packages should live in this repo or separate repos
- whether to target HTML only first, or also PDF and EPUB early
