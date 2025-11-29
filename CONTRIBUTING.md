\# Contributing Guide



Thank you for your interest in contributing to \*\*Python Refresher\*\*.  

This project currently has a single contributor, but this guide serves as a reference for future maintenance and consistency.



For now, the main contribution standard is the \*\*commit message style\*\*, following the Conventional Commits specification.



As the project grows, this document may expand to include guidelines on pull requests, branching, testing, and documentation structure.



---



\## 1. Commit Style Guide



This repository follows the \*\*Conventional Commits\*\* standard to ensure a clean, readable, and meaningful commit history.



\### Why Use Conventional Commits?

\- Makes the history easier to understand.

\- Helps track changes across modules and files.

\- Enables automatic changelog generation (optional).

\- Keeps teamwork consistent, even when working alone.



---



\## 2. Commit Message Format



Each commit message must follow this structure:



<type>(optional scope): <short description>



(optional body)

(optional footer)



\### Types (Required)

Use one of the following:



\- feat – New feature or content.

\- fix – Bug fix or correction.

\- docs – Documentation-only changes (Markdown, comments, READMEs).

\- style – Formatting or style changes (no content changes).

\- refactor – Non-breaking structure changes.

\- chore – Maintenance tasks (configs, dependencies, housekeeping).

\- perf – Performance improvements.

\- test – Adding or modifying tests.



\### Scope (Optional)

Examples:

\- modules

\- nav

\- colab

\- notebooks

\- images

\- site

\- config



\### Description (Required)

\- Concise (preferably under 60 characters).

\- Imperative mood (“add”, “fix”, “update”).



Correct example: fix(nav): restore left navigation panel  

Incorrect: fixed the nav because it was broken



---



\## 3. Examples for This Project



\- docs(modules): update numbering in data types lesson

\- feat(colab): add beginner guide with screenshots

\- fix(site): correct asset paths for GitHub Pages

\- style(images): unify width attributes in notebooks

\- chore(config): remove .nojekyll after resolving paths



---



\## 4. When to Use a Body



Use the body if the commit needs extra explanation. Example:



fix(nav): resolve missing sidebar on GitHub Pages



The issue was caused by misconfigured paths in mkdocs.yml.

Updated site\_url and repo\_url to match the public deployment URL.



---



\## 5. Optional Footer



Use it for references:



fix(nav): correct broken paths



Closes #12



---



\## 6. Quick Checklist Before Committing



\- Does the type accurately describe the change?

\- Is the description short and imperative?

\- Would this commit be clear in six months?

\- Does the scope help clarify the area modified?



---



\## 7. Shortcut Template



If unsure, use:



<type>(scope): brief description of what changed



Or ask ChatGPT:



“Generate a conventional commit message for the following changes: <paste changes>”



---



More contribution guidelines will be added as the project evolves.



