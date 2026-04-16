# Publishing `Python for Synthetic Biology`

This project is configured for GitHub Pages at:

- Site: `https://gonza10v.github.io/Python_for_Synthetic_Biology/`
- Repository: `https://github.com/Gonza10V/Python_for_Synthetic_Biology`

## What is already configured

The project is set up to:

- render the Quarto book to `docs/`
- build both **HTML** and **PDF** outputs
- show repository links in the book sidebar
- deploy automatically on every push to `main`

The PDF file is expected at:

- `https://gonza10v.github.io/Python_for_Synthetic_Biology/python-for-synthetic-biology.pdf`

## Files involved

- `_quarto.yml`
- `index.qmd`
- `.github/workflows/publish.yml`
- `requirements.txt`
- `.nojekyll`
- `.gitignore`

## One-time GitHub setup

In your GitHub repository:

1. Open **Settings → Pages**.
2. Set **Source** to **GitHub Actions**.
3. Open **Settings → Actions → General**.
4. Under **Workflow permissions**, enable **Read and write permissions** if your repository settings require it.

After that, every push to `main` will trigger a fresh build and deployment.

## Local preview

Create and activate a virtual environment, then install dependencies:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Check Quarto and Jupyter:

```bash
quarto check
quarto check jupyter
```

Run the local preview server:

```bash
quarto preview
```

## Local render

To build the site and PDF locally:

```bash
quarto render
```

Expected output:

- HTML site in `docs/`
- PDF at `docs/python-for-synthetic-biology.pdf`

## Publishing model used here

This repository uses a GitHub Actions workflow that:

1. installs Python dependencies
2. installs Quarto
3. renders the book
4. uploads the rendered `docs/` directory
5. deploys the result to GitHub Pages

This means you do **not** need to commit rendered HTML to Git history for deployment to work.

## Linking the book from your main homepage

Use the ready-to-paste snippet in:

- `snippets/homepage-book-card.md`

Paste that into the homepage content for `gonza10v.github.io` to make the book easy to discover.
