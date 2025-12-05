---
hide:
  - toc
---

# 4. Variables & Constants

**Variables** and **constants** are fundamental concepts in programming. They allow a program to store, reuse, and manipulate **data** efficiently during execution.

Understanding their distinction is key: **variables** are changeable containers of **data**, while **constants** represent values that are intended to remain fixed throughout the program's lifecycle.

??? info "1. Variables, Constants, and Naming"

    ### 1.1. Variables

    A **variable** is a name that stores a value in the computer's memory.
  
    Variables:

    - hold **data** (numbers, text, etc.)  
    - can change during program execution  
    - are created when you assign a value using `=`

    Example:
    ```python
    age = 17       # Integer
    price = 4.99   # Float
    name = "Ana"   # String
    ```

    ### 1.2. Constants

    A **constant** is a name used for a value meant to remain unchanged throughout the program.

    Example:
    ```python
    TAX_RATE = 0.16
    MAX_STUDENTS = 30
    ```

    ### 1.3. Naming Conventions

    All variable names must start with a letter (a-z) or an underscore (`_`), and they cannot contain spaces or reserved keywords (like `print` or `if`).

    When using multiple words, two common styles exist:

    | Style | Variable Example | Constant Example (always ALL_CAPS) |
    | :--- | :--- | :--- |
    | **Snake Case (PEP 8)** | `student_name` | `MAX_CAPACITY` |
    | **Camel Case** | `studentName` | `MAX_CAPACITY` |

    Consistency is the Rule: While you may choose either **Snake Case** or **Camel Case** for **variables** based on the specific course or team preference, the most important rule is consistency. Do not mix styles in the same project.

    For **Constants**, the convention is universal: always use **ALL_CAPS**.

    ### 1.4. Case Sensitivity in Python

    Python is **case-sensitive**, meaning that uppercase and lowercase letters are treated as different characters. This means:

    - `Total`, `total`, and `TOTAL` are three different identifiers.
    - A variable must always be used exactly as it was defined.
    - Changing a single letter from lowercase to uppercase will cause a `NameError`.

    Example:
    ```python
    score = 95
    print(Score)   # Error - "Score" is not the same as "score"
    ```

??? example "2. Commented Examples"

    ### 2.1. Variable Assignment and Data Types

    ```python
    # 1. Setup: Assign text data (string)
    name = "Ana"
    # 2. Setup: Assign a whole number (integer)
    result = 25
    # 3. Setup: Assign a decimal number (float)
    num = 4.5 
    ```

    Explanation:

    - Python automatically infers the data type from the assigned value.
    - `str` is used to store text data.
    - `int` is used for whole numbers.
    - `float` is used for decimal numbers, preserving precision.

    ### 2.2. Handling Input and Using a Constant

    ```python
    # 1. Input: Get user data (always returns a string)
    tickets_str = input("Enter the number of tickets: ")

    # 2. Process: Convert string input to integer for calculations
    ticket_count = int(tickets_str)

    # 3. Process: Define a constant value (uppercase convention)
    TICKET_PRICE = 75

    # 4. Process: Calculate the total cost
    total = ticket_count * TICKET_PRICE
    
    # 5. Output: Display the final result
    print("Total cost:", total)  # Example output: Total cost: 225
    ```

    Explanation:

    - `input()` returns a string, requiring conversion for math.
    - `int()` converts the string to an integer for arithmetic.
    - `TICKET_PRICE` uses uppercase, the naming convention for constants.
    - Multiplication calculates the total cost, and the result is printed.

??? question "3. Short Practice Exercises"

    ### 3.1. Value Prediction

    What is the final value and data type of `total`?

    ```python
    variable2 = 18.4
    variable3 = 2.6
    total = variable2 + variable3
    ```

    ??? note "Show solution"
        `total = 21.0`.

        *Note*: The `total` variable is of data type `float`.

    ### 3.2. Naming Conventions

    Identify which names follow Python best practices:

    - `total_amount`
    - `Value1`
    - `client.id`
    - `CustomerName`

    ??? note "Show solution"
        `total_amount`

    ### 3.3. Input Conversion

    Write one line of code asking for a grade and storing it as a float in `final_grade`.

    ??? note "Show solution"
        ```python
        final_grade = float( input("Enter your grade: ") )
        ```

    ### 3.4. Error Identification

    What error occurs with `"Count" + 7`?

    ??? note "Show solution"
        `TypeError`

        *Explanation*: Python cannot add a string (`"Count"`) and an integer (`7`).

??? tip "4. Google Colab: Try It Yourself"

    Practice variable assignment, manipulation, and naming conventions with this Colab notebook:

    👉 [Open the Variables & Constants Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/04_variables.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"

    ### 5.1. What is the primary function of a variable?

    A) Execute repetitive actions.<br>
    B) Print text.<br>
    C) Store a value in memory.<br>
    D) Convert strings to integers. 

    ??? info "Show answer"
        C) Store a value in memory.

    ### 5.2. What is the data type result of `10 + 4.1`?

    A) Integer<br>
    B) Boolean<br>
    C) String<br>
    D) Float

    ??? info "Show answer"
        D) Float

    ### 5.3. Which function always returns input as a string?

    A) `print()`<br>
    B) `int()`<br>
    C) `input()`<br>
    D) `float`()

    ??? info "Show answer"
        C) `input()`

    ### 5.4. What describes a constant?

    A) Changes many times.<br>
    B) Stays fixed during execution.<br>
    C) Stores only names.<br>
    D) Stores decimals.

    ??? info "Show answer"
        B) Stays fixed during execution.

    ### 5.5. What happens after the second line is executed?

    ```python
    id = "Ana"
    id = 12
    ```
    A) The variable `id` is updated to hold the value 12, and its data type becomes an integer.<br>
    B) The program execution stops because a syntax error is raised at that line of code.<br>
    C) The variable `id` continues to store the string value "Ana" without being changed.<br>
    D) The variable `id` is removed entirely from memory and no longer exists in the program.

    ??? info "Show answer"
        A) The variable `id` is updated to hold the value 12, and its data type becomes an integer.

??? warning "6. Common Mistakes"

    - Starting variable names with numbers or invalid characters.
    - Trying to add strings and numbers directly (`"hello" + 3`).
    - Using ALL_CAPS for regular variables (reserve for constants).
    - Confusing `=` (assignment) with `==` (comparison).

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