Python Refresher
================

Python Refresher is a self-paced learning resource designed for students who need a concise and practical review of fundamental Python concepts before advancing to more complex Computational Thinking coursework.

The site is built with MkDocs Material and includes:
- Clear explanations of key Python concepts
- Worked examples and short practice exercises
- Interactive Google Colab notebooks
- Optional short video micro-lessons
- A simple and organized navigation structure

This resource is intended for quick study or revision, suitable for high-school and early undergraduate learners.

------------------------------------------------------------
Access the Live Site
------------------------------------------------------------

Python Refresher Website:
https://juanlealtec.github.io/python-refresher/

------------------------------------------------------------
Contents
------------------------------------------------------------

The site currently includes:

1. Computational Thinking
2. Input–Process–Output
3. Algorithms
4. Variables and Constants
5. Data Types
6. Arithmetic and Basic Expressions
7. Conditions (IF, ELIF, ELSE)
12. Final Challenge

Additional modules will be added as the project continues.

------------------------------------------------------------
Interactive Notebooks
------------------------------------------------------------

Most modules include links to interactive Google Colab notebooks. These notebooks allow learners to:

- Run code directly in the browser
- Explore and modify examples
- Complete small practice tasks
- Save their own working copies

Notebook links appear inside each module.

------------------------------------------------------------
Optional Video Micro-lessons
------------------------------------------------------------

Some modules include short optional videos ("Python Shorts") that reinforce the main idea in under one minute. These videos are supplementary.

------------------------------------------------------------
Local Development
------------------------------------------------------------

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

------------------------------------------------------------
Project Structure
------------------------------------------------------------

python-refresher/
    docs/
        index.md
        01_principles.md
        02_ipo.md
        03_algorithms.md
        04_variables.md
        05_data_types.md
        06_arithmetic.md
        07_conditions.md
        12_final_challenge.md
        glossary.md
        colab_instructions.md
        images/
    mkdocs.yml
    CONTRIBUTING.md

------------------------------------------------------------
Contributing
------------------------------------------------------------

Contributions are welcome.  
Please read CONTRIBUTING.md to follow the repository's conventions, including the use of the Conventional Commits format.

------------------------------------------------------------
Author
------------------------------------------------------------

Juan Carlos Leal Gonzalez  
Educator and developer of instructional materials for Computational Thinking and Python programming.

------------------------------------------------------------
License
------------------------------------------------------------

The educational content published on the website is licensed under  
Creative Commons Attribution-NonCommercial-ShareAlike 4.0 (CC BY-NC-SA 4.0),  
as stated in the site’s index page.

The source code of this repository (scripts, configuration files, and build assets)  
does not currently have a formal open-source license.  
A license may be added later once the structure of the repository is finalized.

