---
hide:
  - toc
---

# 6. Arithmetic & Basic Expressions

Arithmetic operations are the foundation of most computational tasks. They allow a program to **perform calculations**, combine values, and transform data into meaningful results. Understanding how Python handles basic and specialized arithmetic operations, as well as operator precedence, is essential for writing correct and efficient code.

??? info "1. Brief Explanation"
    Arithmetic operators in Python are symbols that perform calculations with numbers (integers or floats). The basic operators are: addition (`+`), subtraction (`-`), multiplication (`*`), and division (`/`).  

    Python also provides specialized operators:  
    - **Floor Division (`//`)** – divides and returns the integer part, discarding any remainder.  
    - **Modulo (`%`)** – returns the remainder of a division.  
    - **Exponentiation (`**`)** – raises a number to a power.  

    When an expression combines an integer and a float, Python automatically converts the result to a float. Expressions follow standard mathematical **operator precedence**, with parentheses `()` having the highest priority to ensure specific operations are evaluated first.

    ## 1.1 Arithmetic Operators
    | Operator | Python Symbol | Description | Example |
    | :--- | :--- | :--- | :--- |
    | Addition | `+` | Sum of two numbers | `3 + 2` → `5` |
    | Subtraction | `-` | Difference between numbers | `5 - 2` → `3` |
    | Multiplication | `*` | Product of numbers | `4 * 3` → `12` |
    | Division | `/` | Real division | `10 / 4` → `2.5` |
    | Floor Division | `//` | Integer division discarding remainder | `10 // 3` → `3` |
    | Modulo | `%` | Remainder of a division | `10 % 3` → `1` |
    | Exponentiation | `**` | Power of a number | `3 ** 4` → `81` |

    ## 1.2 Operator Precedence
    Python follows standard mathematical precedence:
    1. Parentheses `()`  
    2. Exponentiation `**`  
    3. Multiplication `*`, Division `/`, Floor Division `//`, Modulo `%`  
    4. Addition `+`, Subtraction `-`

??? example "2. Commented Examples"
    ### 2.1: Arithmetic Operators
    ```python
    # Modulo: remainder of 10 divided by 3
    mod_result = 10 % 3
    print(mod_result)  # Output: 1

    # Floor Division: quotient without remainder
    floor_result = 10 // 3
    print(floor_result)  # Output: 3

    # Exponentiation: 3 raised to the power of 4
    exp_result = 3 ** 4
    print(exp_result)  # Output: 81
    ```

    ### 2.2: Operator Precedence
    ```python
    # Parentheses evaluated first
    result1 = (5 + 4) + (3 * 2)  # 9 + 6
    print(result1)  # Output: 15

    # Multiplication before addition/subtraction
    result2 = 8 + 3 * 11 - 2  # 8 + 33 - 2
    print(result2)  # Output: 39

    # Modulo before addition
    result3 = 8 % 3 + 1  # 2 + 1
    print(result3)  # Output: 3
    ```

??? question "3. Short Practice Exercises"
    ### 3.1: Operator Identification
    Write the Python arithmetic operator symbol used for:  
    a) calculating the remainder of a division  
    b) raising a number to a power  

    ??? note "Show solution"
        a) `%`  
        b) `**`

    ### 3.2: Precedence Calculation
    Determine the numerical result of the following arithmetic expression:  
    ```python
    20 - 4 * 2 + (10 / 2)
    ```
    
    ??? note "Show solution"
        20 - 8 + 5 → 17.0

    ### 3.3: Input Preparation
    Write two lines of Python code: one line that prompts the user for the sample quantity (`t`) and one line that converts this input to a numerical value.

    ??? note "Show solution"
    ```python
    t = input("Enter sample quantity: ")  # str
    t = int(t)  # or float(t)
    ```

    ### 3.4: Data Type Rule
    Predict the output of the expression:  
    ```python
    10 + "5"
    ```

    ??? note "Show solution"
        ERROR → Cannot add `int` and `str`

??? tip "4. Google Colab: Try It Yourself"
    Practice arithmetic operations, operator precedence, and input conversion with this Colab notebook:

    👉 [Open the Arithmetic Expressions Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/06_arithmetic.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;">**First time using Google Colab?**</span> <a href="/colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"
    ### Q1. What is the highest priority operator in a mathematical expression?
    A) Subtraction (-)  
    B) Multiplication (*)  
    C) Exponentiation (**)  
    D) Parentheses ()  

    ??? info "Show correct answer"
        **D) Parentheses ()**

    ### Q2. Which operator returns the integer part of the division, discarding any remainder?
    A) Modulo (%)  
    B) Division (/)  
    C) Floor Division (//)  
    D) Exponentiation (**)  

    ??? info "Show correct answer"
        **C) Floor Division (//)**

    ### Q3. If x = 10 and y = 3, what is the result of x % y?
    A) 3.333...  
    B) 3  
    C) 1  
    D) 0  

    ??? info "Show correct answer"
        **C) 1**

    ### Q4. What is the data type of 10 + 4.1?
    A) Integer  
    B) String  
    C) Boolean  
    D) Float  

    ??? info "Show correct answer"
        **D) Float**

    ### Q5. In Python, what is the correct operator for raising a number to a power?
    A) `^`  
    B) `*`  
    C) `**`  
    D) `exp`  

    ??? info "Show correct answer"
        **C) `**`**

??? warning "6. Common Mistakes"
    - Ignore operator precedence (assuming left-to-right instead of Python’s rules)  
    - Forget to convert input() strings to numbers before calculation  
    - Combine strings and numbers with `+` causing runtime ERROR  
    - Confuse `/` (float division) with `//` (integer division)  
    - Misinterpret `%` as quotient instead of remainder

??? note "7. Summary Diagram"

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
            Quotient only
          Modulo %
            Remainder
          Exponentiation **
            Power
        Rules
          Operator Precedence
            Parentheses
            Exponentiation
            Multiplication/Division/Modulo
            Addition/Subtraction
          Type Promotion
            int + float = float
    ```

??? tip "8. Optional Extensions"
    - Write a program that prompts the user for two numbers and prints all arithmetic operations between them.  
    - Explore complex arithmetic expressions with nested parentheses and predict the result.  
    - Research how Python handles arithmetic with very large integers and floating-point precision.
