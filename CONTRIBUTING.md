# Contributing to the RaukR Awesome Website 🪨

Welcome! This repo exists so you can **practise the GitHub workflow** by contributing
to a real, live website. Follow the steps below. If you get stuck, that's expected —
getting unstuck *is* the workshop.

> 💡 The golden rule: keep your content **short and fun**. The point is the git
> workflow, not writing essays.

---

## 🚀 The full workflow, step by step

### 1. Fork this repository
Click **Fork** (top-right on GitHub). You now have your own copy at
`https://github.com/YOUR-USERNAME/raukr-awesome-website`.

### 2. Clone your fork to your computer
```bash
git clone https://github.com/YOUR-USERNAME/raukr-awesome-website.git
cd raukr-awesome-website
```

### 3. Connect to the original repo (so you can stay up to date)
```bash
git remote add upstream https://github.com/ninanorgren/raukr-awesome-website.git
```
You now have two remotes: `origin` (your fork) and `upstream` (the class repo).

### 4. Create a branch for your change
Never work directly on `main`. Make a branch named after what you're doing:
```bash
git switch -c add-my-profile
```

### 5. Make your change
Pick a task (see below) and edit the files. Save.

### 6. Commit your change
```bash
git add .
git commit -m "Add my profile to participants"
```

### 7. Sync with the latest class version (IMPORTANT for shared pages)
Before you push, grab everyone else's changes:
```bash
git pull upstream main
```
If you edited a **shared page**, this is where a **merge conflict** may appear. 😈
See [Resolving merge conflicts](#-resolving-merge-conflicts) below.

### 8. Push your branch to your fork
```bash
git push origin add-my-profile
```

### 9. Open a Pull Request
Go to your fork on GitHub. Click **Compare & pull request**. Make sure it's pointing
at `ninanorgren/raukr-awesome-website` `main`. Write a short description and submit. 🎉

### 10. Respond to review
Nina (or a classmate) reviews your PR. If changes are requested, edit, commit, and
push again to the **same branch** — the PR updates automatically.

---

## ✅ Tasks you can do

| Task | File(s) | Difficulty |
|------|---------|:---:|
| Add your profile | new file in `people/` (copy `example-maria.qmd`) | 🟢 Clean PR |
| Add a bug horror story | `pages/worst-bug.qmd` | 🔴 Conflict likely |
| Rate a fika spot | `pages/fika.qmd` | 🔴 Conflict likely |
| Share an R one-liner | `pages/one-liners.qmd` | 🔴 Conflict likely |
| Recommend something | `pages/recommendations.qmd` | 🔴 Conflict likely |

**Start with your profile** for an easy win, then try a shared page to meet your first
merge conflict.

---

## 🧗 Resolving merge conflicts

When `git pull upstream main` reports a conflict, Git marks the clashing lines like this:

```
<<<<<<< HEAD
| Your row |
=======
| A classmate's row |
>>>>>>> upstream/main
```

To resolve it: open the file, **delete the `<<<<<<<`, `=======`, and `>>>>>>>` marker
lines**, and arrange the content so **both** rows are kept (this site is additive —
we almost never want to throw anyone's entry away). Then:

```bash
git add the-file-you-fixed.qmd
git commit            # finishes the merge
git push origin add-my-profile
```

That's it — you've resolved a merge conflict. 🏆

---

## 🔍 Previewing the site locally (optional)

You don't need this to contribute — you only edit Markdown — but if you have
[Quarto](https://quarto.org/docs/get-started/) installed:

```bash
quarto preview
```

Otherwise, just open your PR: the site rebuilds and deploys automatically once your
change is merged.
