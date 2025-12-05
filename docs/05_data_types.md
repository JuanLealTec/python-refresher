---
hide:
  - toc
---

# 5. Data Types

**Data Types** classify the kind of information a **variable** stores. Knowing the **data type** is essential, as it defines which operations (mathematical, logical, or text manipulation) can be performed with that value.

Understanding the difference between the basic types is critical for program's logic and memory management, ensuring operations run accurately and efficiently.

??? info "1. Primitive Categories and Casting"

    ### 1.1. Primitive Categories

    In Python, the most common **primitive data types** are grouped into numbers(**integers** and **floats**), sequences (**strings**), and logical values (**booleans**). These types are the building blocks of any program.
    
    | Data Type | Python Name | Description | Example Assignment |
    | :--- | :--- | :--- | :--- |
    | **Integer** | `int` | Whole numbers, positive or negative, without decimals. | `age = 25` |
    | **Floating-point** | `float` | Numbers that contain a decimal point. | `price = 99.99` |
    | **String** | `str` | Sequences of characters (text). Must be enclosed in single or double quotes. | `name = "Ana"` |
    | **Boolean** | `bool` | Logical values that can only be `True` or `False`. | `is_active = True` |

    Note that Python also includes more complex data structures for organizing collections of data (like lists, tuples, and dictionaries).

    ### 1.2. Type Casting

    When working with different data types, there are strict rules about how they combine and when conversion is necessary (a process called **Type Casting**).

    #### 1.2.1. Input Conversion (`input()`)

    The `input()` function always returns user data as a **string** (`str`). If mathematical calculations are required, conversion using `int()` or `float()` is mandatory:

    ```python
    # User input (always str)
    str_value = input("Enter your age: ")

    # Conversion is necessary to perform mathematical operations
    int_value = int(str_value)

    # Now you can calculate future age:
    future_age = int_value + 10
    print("Your age in 10 years will be:", future_age)
    ```

    #### 1.2.2. Automatic Promotion to `float`

    If an **integer (`int`)** is combined with a **floating-point number (`float`)** in an arithmetic operation, Python automatically converts the result to a **`float`** type to ensure decimal precision is not lost.

    ```python
    integer_value = 10    # int
    float_value = 0.5     # float

    # The result will be a float (10.5)
    result = integer_value + float_value

    print(type(result))
    # Output: <class 'float'>
    ```

??? example "2. Commented Examples"

    ### 2.1. Demonstrating Type Casting

    ```python
    # 1. Input: Prompt user for age (receives str data)
    age_str = input("Please enter your age: ") 

    # 2. Process: Convert the str input to an integer (int) for math
    age_int = int(age_str) 

    # 3. Process: Add 1 to age
    age_next_year = age_int + 1 

    # 4. Process: Convert the integer result back to str for display
    message = "Your age next year will be: " + str(age_next_year)

    # 5. Output: Display the message
    print(message) # Example Output: Your age next year will be: 21
    ```

    Explanation:

    - `input()` always returns a string (`str`).
    - Type Casting (`int()`) is required for arithmetic operations.
    - The `str()` function converts numeric types back to text for display.

    ### 2.2. Mixing Types (Float Promotion)

    ```python
    # 1. Setup: Define an integer variable (int)
    a = 5

    # 2. Setup: Define a floating-point variable (float)
    b = 2.5

    # 3. Process: Perform the operation (Python promotes the result to float)
    result_float = a - b

    # 4. Output: Display the result and verify the resulting data type
    print(result_float)   # Output: 2.5
    print(type(result_float)) # Output: <class 'float'>
    ```

    Explanation:

    - When an operation mixes `int` and `float`, the result is promoted to `float`.
    - This rule ensures that decimal precision is preserved.
    - The `float` type represents non-whole numbers.

??? question "3. Short Practice Exercises"

    ### 3.1. Type Prediction

    What is the final data type of the variable `result` after this calculation?

    ```python
    num_int = 5
    num_float = 2.0
    result = num_int + num_float
    ```

    ??? note "Show solution"
        `float`
    
        *Explanation*: 5 + 2.0 = 7.0

    ### 3.2. Conversion Requirement

    How should the code be corrected so that the final result of the addition is 30?

    ```python
    value_a = "20"
    value_b = 10
    result = value_a + value_b
    ```

    ??? note "Show solution"
        ```python
        value_a = "20"
        value_b = 10
        result = int(value_a) + value_b
        # result is 30 (int)
        ```

        *Explanation*: The string must be converted to an integer:

    ### 3.3. Boolean vs. String

    What is the data type stored in the variable `status`?

    ```python
    status = "False"
    ```

    ??? note "Show solution"
        `str` (String).

        *Explanation*: The quotes around `"False"` make it text data, not a logical boolean value.

    ### 3.4.  Correcting a Type Error

    The following code produces an error. What code line should be added to fix it?

    ```python
    age = input("Enter your age: ")
    future_age = age + 5
    print(future_age)
    ```

    ??? note "Show solution"
        ```python
        age = int(age)
        ```

        *Explanation*: `input()` returns a string, so converting `age` to `int` allows adding 5 without a `TypeError`.

??? tip "4. Google Colab: Try It Yourself"

    Practice recognizing data types and applying type casting with this Colab notebook:

    👉 [Open the Data Types Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/05_data_types.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>


??? question "5. Mini-Quiz"

    ### 5.1. Which Python function always returns the user's input data as a String type?

    A) `print()`<br>
    B) `int()`<br>
    C) `input()`<br>
    D) `float()`

    ??? info "Show answer"
        C) `input()`

    ### 5.2. What data type is stored in the variable `count` after the following line?

    ```python
    count = 12 / 4
    ```

    A) Integer (`int`)<br>
    B) String (`str`)<br>
    C) Boolean (`bool`)<br>
    D) Float (`float`)

    ??? info "Show answer"
        D) Float (`float`)

    ### 5.3. If `user_age` was obtained using `input()`, which conversion is necessary to perform the operation `2 * (user_age)`?

    A) `user_age = str(user_age)`<br>
    B) `user_age = float(user_age)`<br>
    C) `user_age = int(user_age)`<br>
    D) No conversion is required

    ??? info "Show answer"
        C) `user_age = int(user_age)`

    ### 5.4. Which of the following is a boolean data type?

    A) True<br>
    B) 1.23<br>
    C) "True"<br>
    D) 123

    ??? info "Show answer"
        A) True

    ### 5.5. Which data type is used to store a value like "Hello World"?

    A) Integer<br>
    B) Float<br>
    C) Boolean<br>
    D) String

    ??? info "Show answer"
        D) String

??? warning "6. Common Mistakes"

    - Forgetting to convert input values with `int()` or `float()` before using them in calculations.
    - Trying to combine a string and a number with `+` (e.g., `"age: " + 18`).
    - Writing Boolean values as strings (`"True"` / `"False"`) instead of actual booleans.
    - Using lowercase `true` or `false`, which Python treats as undefined variables.

??? note "7. Summary Diagram"

    ```mermaid
    mindmap
      root((Data Types))
        Numeric Types
          Integer (int)
          Float (float)
        Text Type
          String (str)
        Logical Type
          Boolean (bool)
        Conversion (Type Casting)
          int
          float
          str
    ```

??? tip "8. Optional Extensions"

    - Write a short program with `input()` and conversions (`int()` vs. `float()`).
    - Explore the additional data types beyond primitives (`list`, `tuple`, `dict`).
    - Research the difference between mutable and immutable data types.