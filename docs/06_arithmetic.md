---
hide:
  - toc
---

# 6. Arithmetic Operators

Arithmetic operations are the foundation of most computational tasks. They allow a program to perform calculations, combine values, and transform **data** into meaningful results.

Mastering these operations and their rules, particularly **operator precedence**, is essential for writing correct and efficient code that executes computational logic exactly as intended.

??? info "1. Operator Categories and Precedence"

    ### 1.1. Operator Categories

    Arithmetic operators are the symbols used to perform calculations with numbers in Python. They are grouped into basic operations (like addition and multiplication) and specialized operations (like floor division and modulo).

    | Operator | Python Symbol | Description | Example |
    | :--- | :--- | :--- | :--- |
    | Addition | `+` | Sum of two numbers | `3 + 2` → `5` |
    | Subtraction | `-` | Difference between two numbers | `5 - 2` → `3` |
    | Multiplication | `*` | Product of two numbers | `4 * 2` → `8` |
    | Division | `/` | Divides and always returns a float result | `5 / 2` → `2.5` |
    | Floor Division | `//` | Divides and returns the whole number part (floor) of the result | `5 // 2` → `2` |
    | Modulo | `%` | Returns the remainder of a division | `5 % 2` → `1` |
    | Exponentiation | `**` | Raises the first number to the power of the second | `2 ** 3` → `8` |

    ### 1.2. Operator Precedence (Order of Operations)

    Expressions follow standard mathematical **operator precedence**, where parentheses `()` have the highest priority.

    1. Parentheses `()`
    2. Exponentiation `**`
    3. Multiplication/Division/Modulo `*`, `/`, `//`, `%` (from left to right)
    4. Addition/Subtraction `+`, `-` (from left to right)

    Type Promotion Rule: When a calculation mixes **integers** and **floats**, Python automatically converts the result to a **float** (`int + float = float`).

??? example "2. Commented Examples"

    ### 2.1. Arithmetic Operators

    ```python
    # 1. Process: Calculate Modulo (remainder of 10 divided by 3)
    mod_result = 10 % 3
    # 2. Output: Display the calculated result
    print(mod_result) # 1

    # 3. Process: Calculate Floor Division (quotient without remainder)
    floor_result = 10 // 3
    # 4. Output: Display the calculated result
    print(floor_result) # 3

    # 5. Process: Calculate Exponentiation (3 raised to the power of 4)
    exp_result = 3 ** 4
    # 6. Output: Display the calculated result
    print(exp_result) # 81
    ```

    Explanation:

    - Modulo (`%`) returns the remainder of a division.
    - Floor Division (`//`) returns the floor of the quotient; with integer operands the result is an integer.
    - Exponentiation (`**`) calculates powers.

    ### 2.2. Operator Precedence

    ```python
    # 1. Process: Evaluate parentheses first
    result1 = (5 + 4) + (3 * 2)
    # 2. Output: Show result
    print(result1) # 15

    # 3. Process: Apply multiplication before addition/subtraction
    result2 = 8 + 3 * 11 - 2
    # 4. Output: Show result
    print(result2) # 39

    # 5. Process: Apply modulo before addition/subtraction
    result3 = 8 % 3 + 1
    # 6. Output: Show result
    print(result3) # 3
    ```
    Explanation:

    - Parentheses force an explicit evaluation order.
    - Python follows the mathematical order of operations (PEMDAS/BODMAS).
    - Operators `*`, `/`, `//`, and `%` are executed before `+` and `-`.

??? question "3. Short Practice Exercises"

    ### 3.1. Operator Identification

    Write the Python arithmetic operator symbol used for:  
    a) calculating the remainder of a division  
    b) raising a number to a power  

    ??? note "Show solution"
        a) `%`  
        b) `**`

    ### 3.2. Precedence Calculation

    Determine the numerical result of the following arithmetic expression:  

    ```python
    20 - 4 * 2 + (10 / 2)
    ```
    
    ??? note "Show solution"
        20 - 8 + 5 → 17.0

    ### 3.3. Input Preparation

    Write two lines of Python code: one line that prompts the user for the sample quantity (`t`) and one line that converts this input to a numerical value.

    ??? note "Show solution"
        ```python
        t = input("Enter sample quantity: ")  # str
        t = int(t)  # or float(t)
        ```

    ### 3.4. Data Type Rule

    Predict the output of the expression:  

    ```python
    10 + "5"
    ```

    ??? note "Show solution"
        `TypeError`

        *Explanation*: Python cannot add `int` and `str`.

??? tip "4. Google Colab: Try It Yourself"

    Practice arithmetic operations, precedence, and input conversion for calculations with this Colab notebook:

    👉 [Open the Arithmetic Operators Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/06_arithmetic.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"

    ### 5.1. What is the highest priority operator in a mathematical expression?

    A) Subtraction (`-`)<br>
    B) Multiplication (`*`)<br>
    C) Exponentiation (`**`)<br>
    D) Parentheses (`()`)

    ??? info "Show answer"
        D) Parentheses (`()`)

    ### 5.2. Which operator returns the integer part of the division, discarding any remainder?

    A) Modulo (`%`)<br>
    B) Division (`/`)<br>
    C) Floor Division (`//`)<br>
    D) Exponentiation (`**`)

    ??? info "Show answer"
        C) Floor Division (`//`)

    ### 5.3. If x = 10 and y = 3, what is the result of x % y?

    A) 3.333...<br>
    B) 3<br>
    C) 1<br>
    D) 0

    ??? info "Show answer"
        C) 1

    ### 5.4. What is the data type of the result of the expression 10 + 4.1?

    A) Integer<br>
    B) String<br>
    C) Boolean<br>
    D) Float  

    ??? info "Show answer"
        D) Float

    ### 5.5. In Python, what is the correct operator for raising a number to a power?

    A) `^`<br>
    B) `*`<br>
    C) `**`<br>
    D) `exp`

    ??? info "Show answer"
        C) `**`

??? warning "6. Common Mistakes"

    - Ignore operator precedence (assuming left-to-right instead of Python's rules).
    - Forget to convert input() strings to integer or float before calculation.
    - Combine strings and numbers with `+`, causing a TypeError (e.g., `"Age: " + 20`).
    - Confuse `/` (float division) with `//` (integer division).

??? note "7. Summary Diagram"

    ### 7.1. Arithmetic Operators

    ```mermaid
    mindmap
      root((Arithmetic Operators))
        Basic Operators
          Addition +
          Subtraction -
          Multiplication *
          Division /
        Specialized Operators
          Floor Division //
          Modulo %
          Exponentiation **
        Rules
          🟦 Operator Precedence
          Type Promotion
            int + float = float
    ```

    ### 7.2. 🟦 Operator Precedence

    ```mermaid
    flowchart TD
    A[1. Parentheses] --> B[2. Exponentiation];
    B --> C[3. Multiplication / Division / Modulo];
    C --> D[4. Addition / Subtraction];
    ```

??? tip "8. Optional Extensions"

    - Write a program that prompts the user for two numbers and prints all arithmetic operations between them.  
    - Explore complex arithmetic expressions with nested parentheses and predict the result.  
    - Research how Python handles arithmetic with very large integers and floating-point precision.