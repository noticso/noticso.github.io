# noticso's Cybersecurity Notes

A free documentation website built with **MkDocs Material** and designed for publication on **GitHub Pages**.

## Local preview on Windows PowerShell

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
mkdocs serve
```

Then open `http://127.0.0.1:8000` in your browser.

## Update the site

1. Edit a Markdown file inside `docs/`.
2. Save it.
3. Check the local preview.
4. Commit and push to the `master` branch.
5. GitHub Actions deploys the website automatically.

## Important

This repository is intended for educational notes and authorized labs only. Do not upload passwords, private keys, API tokens, personal information, or content from systems you do not own or have explicit permission to test.
