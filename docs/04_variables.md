---
hide:
  - toc
---

# 4. Variables and Constants

Variables and constants are fundamental concepts in programming. They allow a program to **store**, **reuse**, and **manipulate** data. In Python, variables can change during program execution, while constants represent values intended to remain fixed.

??? info "1. Brief Explanation"

    ## 1.1 Variables
    A **variable** is a name that stores a value in the computer’s memory.  
    Variables:

    - hold data (numbers, text, etc.)  
    - can change during program execution  
    - are created when you assign a value using `=`

    Example:
    ```python
    age = 17       # Integer
    price = 4.99   # Float
    name = "Ana"   # String
    ```

    ## 1.2 Constants
    A **constant** is a name used for a value meant to remain unchanged throughout the program.

    Python does **not** have true constants,  
    but by convention we write them in **ALL_CAPS**:

    ```python
    TAX_RATE = 0.16
    MAX_STUDENTS = 30
    ```

    ## 1.3 Variable: Memory Diagram

    ```mermaid
    flowchart LR
        A[age = 17] --> B((age))
        B --> C[17]
    ```

    ## 1.4 Input: Receiving User Data
    The `input()` function **ALWAYS** returns a value as a **string**.

    ```python
    grade_str = input("Enter your grade: ")
    ```

    To use this value in math, convert it:

    ```python
    grade = float(grade_str)
    ```

    ## 1.5 Naming Conventions

    All variable names must start with a letter (a-z) or an underscore (`_`), and they cannot contain spaces or reserved keywords (like `print` or `if`).

    When using multiple words, two common styles exist:

    | Style | Variable Name (Example) | Constant Name (Example) |
    | :--- | :--- | :--- |
    | **PEP 8 (Snake Case)** | `student_name` | `MAX_CAPACITY` |
    | **Camel Case** | `studentName` | `MAX_CAPACITY` |

    **Consistency is the Rule**: While you may choose either **Snake Case** or **Camel Case** for *variables* based on the specific course or team preference, the most important rule is **consistency**. Do not mix styles in the same project.  
    For **Constants**, the convention is universal: always use **ALL_CAPS**.

    ### 1.5.1 Case Sensitivity in Python

    Python is **case-sensitive**, meaning that uppercase and lowercase letters are treated as different characters.

    This means:

    - `Total`, `total`, and `TOTAL` are **three different identifiers**  
    - A variable must always be used **exactly** as it was defined  
    - Changing a single letter from lowercase to uppercase will cause a `NameError`

    Example:

    ```python
    score = 95
    print(Score)   # ❌ Error — “Score” is not the same as “score”
    ```

??? example "2. Commented Examples"

    ## 2.1: Variable Assignment and Data Types

    ```python
    name = "Ana"      # String
    result = 25        # Integer
    num = 4.5          # Float
    ```

    Explanation:

    - `"Ana"` is stored as text (`str`)
    - `25` is an integer (`int`)
    - `4.5` is a decimal value (`float`)

    ## 2.2: Handling Input and Using a Constant

    ```python
    tickets_str = input("Enter the number of tickets: ")

    # Convert input (string → int)
    ticket_count = int(tickets_str)

    # Constant (by convention)
    TICKET_PRICE = 75

    total = ticket_count * TICKET_PRICE
    print("Total cost:", total)
    ```

    Notes:

    - `input()` → string  
    - `int()` converts it  
    - `TICKET_PRICE` behaves like a constant  

??? question "3. Short Practice Exercises"

    ### 3.1: Value Prediction  
    What is the final value and data type of `total`?

    ```python
    variable2 = 18.4
    variable3 = 2.6
    total = variable2 + variable3
    ```

    ??? note "Show solution"
        `total = 21.0`  
        Data type: **float**

    ### 3.2: Naming Conventions  
    Identify which names follow Python best practices (lowercase + underscores):

    - `total_amount`  
    - `Value1`  
    - `client.id`  
    - `CustomerName`

    ??? note "Show solution"
        Only:  
        - `total_amount`

    ### 3.3: Input Conversion  
    Write one line of code asking for a grade and storing it as a float in `final_grade`.

    ??? note "Show solution"
        ```python
        final_grade = float( input("Enter your grade: ") )
        ```

    ### 3.4: Error Identification  
    What error occurs with `"Count" + 7`?

    ??? note "Show solution"
        A **TypeError** occurs because you cannot add a string and an integer.

??? tip "4. Google Colab: Try It Yourself"

    Use the following Colab notebook to practice:

    👉 [Open the Variables & Constants Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/04_variables.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="/colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"

    ### Q1. What is the primary function of a variable?
    A) Execute repetitive actions  
    B) Print text  
    C) Store a value in memory  
    D) Convert strings to integers  

    ??? info "Show answer"
        **C) Store a value in memory**

    ### Q2. What is the result of `10 + 4.1`?
    A) Integer  
    B) Boolean  
    C) String  
    D) Float  

    ??? info "Show answer"
        **D) Float**

    ### Q3. Which function always returns input as a string?
    A) print()  
    B) int()  
    C) input()  
    D) float()  

    ??? info "Show answer"
        **C) input()**

    ### Q4. What describes a constant?
    A) Changes many times  
    B) Stays fixed during execution  
    C) Stores only names  
    D) Stores decimals  

    ??? info "Show answer"
        **B) Stays fixed during execution**

    ### Q5. What happens after the second line is executed?
    ```python
    id = "Ana"
    id = 12
    ```
    A) The variable `id` is updated to hold the value 12, and its data type becomes an integer  
    B) The program execution stops because a syntax error is raised at that line of code  
    C) The variable `id` continues to store the string value "Ana" without being changed    
    D) The variable `id` is removed entirely from memory and no longer exists in the program  

    ??? info "Show answer"
        **A) The variable `id` is updated to hold the value 12, and its data type becomes an integer**

??? warning "6. Common Mistakes"

    - Forgetting to convert input values using `int()` or `float()`
    - Starting variable names with numbers or invalid characters
    - Trying to add strings and numbers directly (`"hello" + 3`)
    - Using ALL_CAPS for regular variables (reserve for constants)
    - Confusing `=` (assignment) with `==` (comparison)

??? note "7. Summary Diagram"

    ```mermaid
    mindmap
      root((Variables & Constants))
        Variables
          Changeable
          Store data
          Created with =
        Constants
          Fixed value
        Input
          Always string
          Convert with int or float
        Naming Conventions
          Consistency is key
          Variables
            snake_case
            camelCase
          Constants     
            ALL_CAPS
    ```

??? tip "8. Optional Extensions"

    - Write three valid and three invalid variable names.  
    - Identify constants in a real-world situation.
    - Create a small program that multiplies two input values.  
