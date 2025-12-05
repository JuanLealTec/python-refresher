# Python Refresher

Python Refresher is a self-paced learning resource designed for students who need a concise and practical review of fundamental Python concepts before advancing to more complex Computational Thinking coursework.

The site is built with MkDocs Material and includes:

- Clear explanations of key Python concepts
- Worked examples and short practice exercises
- Interactive Google Colab notebooks
- Optional short video micro-lessons
- A simple and organized navigation structure

This resource is intended for quick study or revision, suitable for high-school and early undergraduate learners.

---

## Access the Live Site

Python Refresher Website:
https://juanlealtec.github.io/python-refresher/

---

## Contents

The site currently includes:

1. Computational Thinking
2. Input-Process-Output
3. Algorithms
4. Variables and Constants
5. Data Types
6. Arithmetic Operators
7. Conditionals & Relational Operators
8. Nested & Multiple Conditionals
9. Compound Conditions
10. While Loop
11. For Loop
12. Final Challenge

### Aditional Resources

- Glossary
- Google Colab - Beginner Guide
- Programming Best Practices

---

## Interactive Notebooks

Most modules include links to interactive Google Colab notebooks. These notebooks allow learners to:

- Run code directly in the browser
- Explore and modify examples
- Complete small practice tasks
- Save their own working copies

Notebook links appear inside each module.

---

## Optional Video Micro-lessons

Some modules include short optional videos ("Python Shorts") that reinforce the main idea in under one minute. These videos are supplementary.

---

## Local Development

To build or preview the site locally:

1. Install MkDocs and required extensions:

   pip install mkdocs-material
   pip install pymdown-extensions

2. Serve the site locally:

   mkdocs serve

   This opens a local development server with live reload.

3. Deploy to GitHub Pages:

   mkdocs gh-deploy

GitHub Pages must be configured as:

- Source: Deploy from a branch
- Branch: gh-pages
- Folder: root directory

---

## Project Structure

The project structure follows the standard MkDocs layout:

```text
python-refresher/
├── .gitignore               # Files ignored by Git
├── CONTRIBUTING.md          # Guide for contributions
├── LICENSE.md               # The MIT License (Source Code)
├── LICENSE-CONTENT.md       # CC BY-NC-SA 4.0 License (Educational Content)
├── mkdocs.yml               # MkDocs configuration file
└── docs/                    # Source files for the website content
    ├── 01_principles.md     # Main modules (.md files)
    ├── ... (content files)
    ├── glossary.md          # Resources and supplementary files
    ├── index.md             # Site homepage
    └── assets/              # Static assets for the site
        ├── img/             # Images used in the markdown files
        └── notebooks/       # Google Colab notebooks (.ipynb files)
```

---

## Contributing

Contributions are welcome.  
Please read CONTRIBUTING.md to follow the repository's conventions, including the use of the Conventional Commits format.

---

## Author

Juan Carlos Leal González  
Adjunct High School Lecturer at PrepaTec Eugenio Garza Lagüera, Tecnológico de Monterrey, teaching Computational Thinking I and II.

---

## License

This repository uses a dual-licensing approach based on the content type:

### 1. Educational Content

The original educational content (e.g., text, examples, and markdown files in `docs/`) is licensed under:
**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0)**.
* See the full terms in [LICENSE-CONTENT.md].

### 2. Source Code & Configuration

The source code, build scripts, and configuration files (e.g., `mkdocs.yml`, deployment assets) are licensed under:
**The MIT License**.
* See the full terms in [LICENSE.md].