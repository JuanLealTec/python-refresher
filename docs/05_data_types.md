---
hide:
  - toc
---

# 5. Data Types

Data Types are the classification Python and other programming languages use to understand the kind of information a variable stores. Knowing the data type is essential, as it defines which operations (mathematical, logical, or text manipulation) can be performed with that value.

??? info "1. Brief Explanation"
    ## 1.1 Data Types: Primitive Categories
    In Python, the most common primitive data types are grouped into numbers, sequences (strings), and logical values (booleans).

    | Data Type | Python Name | Description | Example Assignment |
    | :--- | :--- | :--- | :--- |
    | **Integer** | `int` | Whole numbers, positive or negative, without decimals. | `age = 25` |
    | **Floating-point** | `float` | Numbers that contain a decimal point. | `price = 99.99` |
    | **String** | `str` | Sequences of characters (text). Must be enclosed in single or double quotes. | `name = "Ana"` |
    | **Boolean** | `bool` | Logical values that can only be `True` or `False`. | `is_active = True` |

    ## 1.2 Data Types: Operation Rules and Casting
    When working with different data types, there are strict rules about how they combine and when conversion is necessary (a process called *Type Casting*).

    ### 1.2.1 Input Conversion (`input()`)
    The `input()` function always returns user data as a **string (`str`)**. If mathematical calculations are required, conversion using `int()` or `float()` is mandatory:

    ```python
    # User input (always str)
    str_value = input("Enter your age: ")

    # Conversion is necessary to perform mathematical operations
    int_value = int(str_value)

    # Now you can calculate future age:
    future_age = int_value + 10
    print("Your age in 10 years will be:", future_age)
    ```

    ### 1.2.2 Automatic Promotion to `float`
    If an integer (`int`) is combined with a floating-point number (`float`) in an arithmetic operation, Python automatically converts the result to a `float` type to ensure decimal precision is not lost.

    ```python
    integer_value = 10    # int
    float_value = 0.5     # float

    # The result will be a float (10.5)
    result = integer_value + float_value

    print(type(result))
    # Output: <class 'float'>
    ```

??? example "2. Commented Examples"
    ### 2.1: Demonstrating Type Casting
    This shows how to handle user input (which is always a `str`) and convert it to an `int` to perform arithmetic, then convert the result back to a `str` for printing.

    ```python
    # 1. Input: str data is received
    age_str = input("Please enter your age: ") # age_str stores "20" (type str)

    # 2. Process (Type Casting): Convert str to int
    age_int = int(age_str) # age_int stores 20 (type int)

    # 3. Process (Arithmetic): Operation works on int
    age_next_year = age_int + 1 # age_next_year stores 21 (type int)

    # 4. Output: Convert the result back to str for a descriptive print message
    message = "Your age next year will be: " + str(age_next_year)
    print(message)
    # Output: Your age next year will be: 21
    ```

    ### 2.2: Mixing Types (Float Promotion)
    If a calculation involves both `int` and `float`, Python promotes the result to `float`.

    ```python
    # Define an integer and a float
    a = 5         # type int
    b = 2.5       # type float

    # Subtraction involves a float, so the result is a float
    result_float = a - b

    print(result_float)  # Output: 2.5
    print(type(result_float)) # Output: <class 'float'>
    ```

??? question "3. Short Practice Exercises"
    ### 3.1: Type Prediction
    What is the final data type of the variable `result` after this calculation?

    ```python
    num_int = 5
    num_float = 2.0
    result = num_int + num_float
    ```

    ??? note "Show solution"
        **Data Type:** `float` (5.0 + 2.0 = 7.0)

    ### 3.2: Conversion Requirement
    How should the code be corrected so that the final result of the addition is 30?

    ```python
    value_a = "20"
    value_b = 10
    # result = value_a + value_b
    ```

    ??? note "Show solution"
        The string must be converted to an integer:
        ```python
        value_a = "20"
        value_b = 10
        result = int(value_a) + value_b
        # result is 30 (int)
        ```

    ### 3.3: Boolean vs. String
    What is the data type stored in the variable `status`?

    ```python
    status = "False"
    ```

    ??? note "Show solution"
        **Data Type:** `str` (String). The quotes around `False` make it text data, not a logical boolean value.

??? tip "4. Google Colab: Try It Yourself"
    The best way to solidify your understanding of data types and casting is through hands-on practice. Use the following Colab notebook to practice:

    👉 [Open the Data Types Colab notebook ↗](https://colab.research.google.com/drive/1XQpGEIHEgWnxlcP2bts_bf2u9uyu9PQh?usp=sharing){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;">**First time using Google Colab?**</span> <a href="/colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"
    ### Q1. Which Python function always returns the user’s input data as a String type?
    A) `print()`  
    B) `int()`  
    C) `input()`  
    D) `float()`

    ??? info "Show answer"
        **C) `input()`**

    ### Q2. What data type is stored in the variable `count` after the following line?
    ```python
    count = 12 / 4
    ```
    A) Integer (`int`)  
    B) String (`str`)  
    C) Boolean (`bool`)  
    D) Float (`float`)

    ??? info "Show answer"
        **D) Float (`float`)**

    ### Q3. Which conversion is necessary to perform the operation `2 * (user_age)`?
    A) `user_age = str(user_age)`  
    B) `user_age = float(user_age)`  
    C) `user_age = int(user_age)`  
    D) No conversion is required

    ??? info "Show answer"
        **C) `user_age = int(user_age)`**

    ### Q4. Which of the following is a boolean data type?
    A) True  
    B) 1.23  
    C) "True"  
    D) 123

    ??? info "Show answer"
        **A) True**

    ### Q5. Which data type is used to store a value like "Hello World"?
    A) Integer  
    B) Float  
    C) Boolean  
    D) String

    ??? info "Show answer"
        **D) String**

??? warning "6. Common Mistakes"

    - Forgetting to convert input values with `int()` or `float()` before using them in calculations  
    - Trying to combine a string and a number with `+` (e.g., `"age: " + 18`)  
    - Writing Boolean values as strings (`"True"` / `"False"`) instead of actual booleans  
    - Expecting an integer when one operand is a float (Python returns a float)  
    - Using lowercase `true` or `false`, which Python treats as undefined variables

??? note "7. Summary Diagram"

    ```mermaid
    mindmap
      root((Data Types))
        Numeric Types
          Integer (int)
            Whole numbers
            Ex: 10, -5
          Float (float)
            Numbers with decimals
            Automatic promotion in calculations
            Ex: 3.14, 0.0
        Text Type
          String (str)
            Sequence of characters
            Must be in quotes
            Input is always str
        Logical Type
          Boolean (bool)
            Only True / False
        Conversion (Type Casting)
          Functions
            int
            float
            str
          Key Rule     
            Conversion is mandatory for math operations
    ```

??? tip "8. Optional Extensions"

    - Write a short program with `input()` and conversions (`int()` vs. `float()`).
    - Explore the additional data types beyond primitives (`list`, `tuple`, `dict`).
    - Research the difference between mutable and immutable data types.
