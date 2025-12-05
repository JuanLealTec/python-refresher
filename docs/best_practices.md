# Programming Best Practices

This guide introduces the concept of **Clean Code**: code that is easy to read, understand, and maintain by anyone—including your future self. Adopting these habits is critical for success in academic settings and professional careers.

## 1. Why Style Matters: The Clean Code Principle

Most programming work involves maintaining or modifying existing code, not just writing it from scratch. Clean code is easier to read, debug, and improve.

- Readability: You and others can quickly understand the purpose of a section of code.
- Consistency: Consistent style is a fundamental habit valued highly in all academic assignments and future projects.
- Debugging: Well-structured code simplifies the process of finding and fixing errors.

## 2. Naming Conventions (Nomenclature)

Consistent and clear naming is fundamental to ensure your code is readable.

### Fundamental Rules for All Names
- Names must start with a letter (a-z, A-Z) or an underscore (`_`).
- Names cannot contain spaces or use Python's reserved keywords (like `print`, `if`, or `for`).
- Avoid Cryptic Names: Names should clearly describe the data they hold (e.g., `user_age` is better than `x`).

### Styles for Variables
When a name consists of multiple words, you must choose a style.

| Style | Description | Example |
| :--- | :--- | :--- |
| **Snake Case** (PEP 8 Standard) | All lowercase letters, words separated by underscores. | `student_name`, `total_amount` |
| **Camel Case** (Alternative Option) | First word lowercase, the first letter of subsequent words capitalized. | `studentName`, `totalAmount` |

### Style for Constants
Constants (values that do not change) have a universal convention, regardless of your chosen variable style.

| Element | Convention | Example |
| :--- | :--- | :--- |
| **Constants** | `ALL_CAPS` (All uppercase with underscores) | `PI = 3.14`, `MAX_CAPACITY` |

Consistency is the Critical Rule: You must choose one style (Snake Case or Camel Case) for your variables and functions and use it consistently throughout your entire project. Do not mix styles.

Clarity over Brevity: A variable name should clearly describe its purpose. For instance, `days_in_the_month` is always better than `d`.

## 3. Code Formatting and Indentation

Python relies heavily on indentation for structure, making consistency vital.

- Indentation: Use 4 spaces per level of indentation.
- Spacing around Operators: Place spaces around binary operators (like `=`, `+`, `==`, `*`, etc.).
    - Good: `age = 18 + 5`
    - Bad: `age=18+5`
- Blank Lines: Use a single blank line to separate logical blocks or sections of code, improving overall readability.
- Line Length: Keep lines reasonably short to avoid horizontal scrolling.

## 4. Smart Comments and Documentation

Comments should explain the why, not the obvious what.

| Type | Example | Purpose |
| :--- | :--- | :--- |
| **The "Why"** | `# The age is incremented here to handle the leap year jump.` | Explains the reason or context behind a non-obvious calculation. |
| **The Obvious** | `# add 1 to x` | Avoid redundant comments. If the code is clear, the comment is often unnecessary. |
| **Placeholders** | `# TODO: Implement logic to handle negative inputs here.` | Use `# TODO:` to mark code that is incomplete or needs future attention (a professional standard). |

## 5. Structuring Control Flow

### Conditionals
- Use `elif`: Always use the `if...elif...else` chain when conditions are mutually exclusive, instead of multiple independent `if` statements.
- Simplify Logic: Avoid excessive nesting (more than 3 levels of `if` inside `if`) in favor of compound conditions (`and`/`or`).

### Common Beginner Errors to Avoid

*Attention:* Fixing these common errors will save you hours of debugging!

| Error | Description | Fix |
| :--- | :--- | :--- |
| **Assignment vs. Comparison** | Confusing the assignment operator (`=`) with the comparison operator (`==`). | Always use `==` inside `if` or `while` conditions. |
| **Indentation Errors** | Incorrect spacing (`Misindentation`) is a common source of errors. | Always use exactly 4 spaces and check the alignment of your code blocks. |
| **Incomplete Conditions** | Writing `if x and y:` when you meant `if x == 1 and y == 1:`. | You must state the full condition for every variable. |
| **Infinite Loops** | Forgetting to update the variable that controls a `while` loop. | Ensure the loop condition will eventually become `False`. |

## 6. Testing and Input Validation

A good programmer tries to break their own program to ensure it is robust.

- Test with Normal Data: Use typical values that the program is designed to handle.
- Test with Edge Cases: Try extreme values (zero, very large numbers, negative numbers, empty strings).
- Test with "Wrong" Input: Check how the program reacts to incorrect data (e.g., entering text when a number is expected).
    - Input Validation: Check that user inputs are of the expected type, provide clear prompts, and avoid allowing the program to crash due to predictable input errors.
- Debugging: Use `print()` statements strategically to track the value of variables, but remember to clean them up before submitting your final work.

## 7. Project Organization and Workflow

Good file and code management is essential for success and effective debugging.

- Separate Projects: Keep distinct assignments or projects in separate files or folders to prevent confusion and accidental data mixing.
- Documentation: Always document your files with clear titles, section headers, and your name to ensure clarity for yourself and your others.
- Clean Code: Keep your code files clean and well-structured. Avoid leaving "dead code" (code that is no longer used but hasn't been deleted).
- Versioning: Adopt habits of saving versions (e.g., `project_v1.py`, `project_v2.py`) to easily revert changes or track progress.

## 8. Ethical Programming Basics

Writing code involves social responsibility and academic honesty, especially when using external tools.

- Integrity & Attribution: Always cite any code used. Never present material generated in whole or part by AI as your own work (Plagiarism).
- Transparency: If you use an AI tool, you must declare and reference its use in your assignments. Undue use is a lack of academic integrity.
- Understanding: Do not use tools to produce work you don't understand or to gain an unfair academic advantage. The goal is learning.
- Social Responsibility: Respect privacy when handling data. Do not use tools to promote bias or act against human dignity.