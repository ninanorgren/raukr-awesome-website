# RaukR 2026 — Awesome Co-Created Website 🪨

A Quarto website **built by the whole RaukR cohort** to practise the GitHub workflow:
forking, branching, committing, pushing, pull requests, and (deliberately!) resolving
merge conflicts.

🔗 **Live site:** https://ninanorgren.github.io/raukr-awesome-website/

## For students

👉 **Start with [CONTRIBUTING.md](CONTRIBUTING.md)** — it walks you through the entire
fork → clone → branch → commit → push → PR workflow, plus how to resolve merge conflicts.

The quick version:
1. **Fork** this repo.
2. **Add yourself** to `people/` (easy, conflict-free first PR).
3. Edit a **shared page** in `pages/` (and enjoy your first merge conflict 😈).
4. Open a **pull request** back here.

## How it's structured

| Path | What it is |
|------|------------|
| `index.qmd` | Home page |
| `people/` | One `.qmd` per participant; auto-generated gallery (clean PRs) |
| `pages/` | Shared append-to pages — the merge-conflict practice grounds |
| `_quarto.yml` | Site config (navbar, theme) |
| `.github/workflows/publish.yml` | Auto-renders & deploys to GitHub Pages on merge to `main` |

## For the instructor — one-time setup

1. **Push this repo** to `github.com/ninanorgren/raukr-awesome-website`.
2. The first push to `main` triggers the **Render and Publish** Action, which creates a
   `gh-pages` branch with the rendered site.
3. In **Settings → Pages**, set **Source = Deploy from a branch**, branch **`gh-pages`**,
   folder **`/ (root)`**. Save.
4. Under **Settings → Actions → General → Workflow permissions**, ensure
   **Read and write permissions** is enabled (so the Action can push `gh-pages`).
5. Done — every merged PR now rebuilds and redeploys the site automatically. 🎉

> Students editing only Markdown don't need Quarto installed locally. To preview
> locally yourself: install [Quarto](https://quarto.org/docs/get-started/) and run
> `quarto preview`.
