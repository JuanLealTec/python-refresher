# Contributing Guide

Thank you for your interest in contributing to **Python Refresher**!
This project currently has a single maintainer, but this guide establishes standards that will help keep the repository organized, clear, and sustainable as it grows.

This document covers:

- how to contribute,
- commit message standards,
- notebook guidelines,
- and instructions for maintaining the documentation site.

# 1. How to Contribute

Even though contributions are limited for now, this workflow keeps changes consistent:

1. Fork the repository (optional for the maintainer).
2. Create a new branch for your changes.  
   Recommended format:
   <type>/<short-description>

   Examples:
   feat/new-arithmetic-lesson
   docs/update-links

3. Make your changes.
4. Follow the Commit Style Guide below.
5. Open a Pull Request if collaborating, or merge directly if you are the maintainer.

# 2. Commit Style Guide

This project follows the Conventional Commits specification to maintain a clean and meaningful commit history.

Consistent commit messages make it easier to:

- understand changes,
- trace edits across modules,
- generate changelogs (optional),
- keep the project clear over time.

# 3. Commit Message Format

Each commit message must follow this structure:

```
<type>(optional scope): <short description>

(optional body)

(optional footer)
```

## 3.1 Allowed Types

- feat: New feature or content.
- fix: Bug fix or correction.
- docs: Documentation-only changes.
- style: Formatting-only changes.
- refactor: Non-breaking structure changes.
- chore: Maintenance tasks.
- perf: Performance improvements.
- test: Adding or modifying tests.

## 3.2 Optional Scope Examples

- modules
- notebooks
- images
- colab
- site
- config

## 3.3 Description Rules

- Keep it concise (under 60 characters preferred).
- Use imperative mood ("add", "fix", "update").

Correct:

```
fix(nav): restore left navigation panel
```

Incorrect:

```
fixed the nav because it was broken
```

# 4. Examples for This Project

- docs(modules): update numbering in data types lesson
- feat(colab): add beginner guide with screenshots
- fix(site): correct asset paths for GitHub Pages
- style(images): unify width attributes in notebooks
- chore(config): remove .nojekyll after resolving paths

# 5. When to Use a Commit Body

Use a body when the change requires additional explanation.

Example:

```
fix(nav): resolve missing sidebar on GitHub Pages

The issue was caused by misconfigured paths in mkdocs.yml.
Updated site_url and repo_url to match the public deployment URL.
```

# 6. Optional Footer

Use the footer to reference issues or related items.

Example:

```
fix(nav): correct broken paths

Closes #12
```

# 7. Quick Checklist Before Committing

- Does the type accurately describe the change?
- Is the description short and imperative?
- Would this message still make sense in six months?
- Does the scope add useful clarity?

# 8. Shortcut Template

Use the following if unsure:

```
<type>(scope): brief description of what changed
```

Or ask ChatGPT:

"Generate a conventional commit message for the following changes: <paste changes>"

# 9. Notebook Guidelines

All `.ipynb` notebooks must be committed executed and clean, because the documentation site opens them directly in Google Colab.

This means:

- Keep meaningful outputs visible (prints, examples, tables, plots).
- Remove debugging cells, temporary code, or unnecessary logs.
- Run the notebook from top to bottom before committing  
  (Restart & Run All).
- Maintain ordered execution counters (In [1], In [2], etc.).
- Ensure the notebook contains no execution errors.
- Avoid committing extremely large outputs unless necessary for teaching.

Notebooks are opened via:
https://colab.research.google.com/github/<user>/<repo>/blob/main/docs/assets/notebooks/

Therefore, outputs must remain visible for students reviewing the material.

# 10. Documentation Guide

This section applies to changes in content (.md files) or the documentation configuration (mkdocs.yml).

## 10.1 Testing Changes Locally

Before committing any documentation changes, verify that the site renders correctly:

```
mkdocs serve
```

Then open:
http://127.0.0.1:8000/

## 10.2 Deployment (Maintainers Only)

To build and push the documentation to the `gh-pages` branch:

```
mkdocs gh-deploy
```

If you encounter a rejected push (usually due to history mismatch), force the deployment:

```
mkdocs gh-deploy --force
```
