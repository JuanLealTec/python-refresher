---
hide:
  - toc
---

# 7. Conditionals & Relational Operators

**Conditional statements** are fundamental in programming, enabling a program to make decisions and execute different code based on specific conditions. This allows the program to respond to various situations, ensuring adaptive behavior.

These structures are the primary mechanism used to guide the flow of execution. Mastering them is essential for building dynamic and interactive programs based on **Boolean conditions**.

??? info "1. Basic Syntax and Flow Control"

    ### 1.1. The if-else Syntax

    Conditional structures allow a program to make decisions based on **Boolean conditions** (`True` or `False`). The two main components are the `if` and `else` blocks, which manage the flow of execution.

    Key Elements:

    - The `if` statement checks a condition; if True, its indented code block runs.
    - The `else` block runs when the preceding `if` condition is False. (*Note*: The `else` block is optional.)
    - Syntax Requirement: The basic `if-else` structure requires a Boolean condition and a colon (`:`), followed by an **indented code block**. **Indentation** is mandatory to define which statements belong to each conditional block.

    ```python
    if condition_is_true:
        # Code runs if the condition is True
        statement_1
    else:
        # Code runs if the condition is False
        statement_2
    ```

    ### 1.2. Conditional Flow (if-else)

    The following flowchart illustrates how a condition (the diamond) guides the execution flow. Only one path, the True or the False path, is ever taken before the program flow continues.

    <div style="width: 55%;">
    ```mermaid
    flowchart TD
        A[Start Program] --> B{Condition is True?};
        B -- True --> C[Execute Code in if Block];
        B -- False --> D[Execute Code in else Block];
        C --> E[Continue Program];
        D --> E;
    ```
    </div>

    ### 1.3. Relational Operators

    Relational operators allow Python to compare values and evaluate conditions. The most common ones are:

    | Operator | Description | Example |
    | :--- | :--- | :--- |
    | `==` | Equals | `x == 10` → True if x is 10 |
    | `!=` | Not equal | `x != 5` → True if x is not 5 |
    | `>` | Greater than | `x > 3` → True if x is greater than 3 |
    | `<` | Less than | `x < 7` → True if x is less than 7 |
    | `>=` | Greater than or equal | `x >= 18` → True if x is 18 or older |
    | `<=` | Less than or equal | `x <= 100` → True if x is 100 or less |

    ### 1.4. Conditional Expression (Ternary Operator)

    Python's **Conditional Expression** provides a compact way to assign a value to a variable based on a single condition, all in one line of code.

    The general syntax is:

    `value_if_true if condition else value_if_false`

    It simplifies the common `if-else` structure where the only action is assigning a value.

??? example "2. Commented Examples"

    ### 2.1. Basic `if` Structure (No else)

    ```python
    # 1. Input: Get age from user and convert to integer
    age = int(input("How old are you? "))

    # 2. Decision: Check if the user meets the age requirement
    if age >= 18:
        # 3. Output: Executes ONLY if the condition is True
        print("You can enter the party!") # Example Output: You can enter the party!
    # If the condition is False, the program moves on without action.
    ```

    Explanation:

    - The basic `if` statement checks a single condition.
    - The code inside the `if` block is only executed if the condition evaluates to True.
    - If the condition is False, no action is taken.

    ### 2.2. Using `if-else` for Two Outcomes

    ```python
    # 1. Input: Get age from user and convert to integer
    age = int(input("How old are you? "))

    # 2. Decision: Check the condition
    if age >= 18:
        # 3. Output (True Path): Executes if age is 18 or older
        print("You can enter the party!") # Example Output (True): You can enter the party!
    else:
        # 4. Output (False Path): Executes if the condition is False
        print("Sorry, you cannot enter the party.") # Example Output (False): Sorry, you cannot enter the party.
    ```

    Explanation:

    - The `if-else` structure handles two mutually exclusive paths.
    - The `if` block runs if the condition is True.
    - The `else` block provides the default action and runs if the condition is False.

    ### 2.3. Conditional Expression (Ternary Operator)

    ```python
    # 1. Input: Get age from user and convert to integer
    age = int(input("How old are you? "))

    # 2. Decision and Assignment in One Line (Ternary Operator)
    # Syntax: result_if_true if condition else result_if_false
    status = "Adult" if age >= 18 else "Minor"

    # 3. Output
    print("Your status is:", status) # Example Output (age 20): Your status is: Adult
    ```

    Explanation:

    - The Conditional Expression is a shortcut for simple `if-else` statements where the primary goal is to assign a value to a variable.
    - It is read from the middle: check the `condition` (`age >= 18`).
    - If the condition is True, the expression returns the value before the `if` (`"Adult"`).
    - If the condition is False, the expression returns the value after the `else` (`"Minor"`).

??? question "3. Short Practice Exercises"

    ### 3.1. Prediction of Output

    What is the final output of the following code block?

    ```python
    x = 10
    if x > 5:
        print("A")
    else:
        print("B")
    ```

    ??? note "Show solution"
        `"A"`

        *Explanation*: The `if` condition (`x > 5`) is True, so the `else` block is skipped.

    ### 3.2. Error Correction

    How should the code be corrected to check if `current_state` is equal to `"running"`?

    ```python
    current_state = "running"
    # if current_state = "running":
    #     print("System active")
    ```

    ??? note "Show solution"
        ```python
        current_state = "running"
        if current_state == "running":
            print("System active")
        ```

        *Explanation*: The comparison operator `==` must be used instead of the assignment operator `=`:

    ### 3.3. Indentation Error

    Identify the error in the following conditional structure:

    ```python
    user_status = True
    if user_status:
    print("Welcome")
    ```

    ??? note "Show solution"
        `IndentationError`

        *Explanation*: The statement inside the `if` block (`print("Welcome")`) must be indented (usually 4 spaces).

    ### 3.4. Conditional Expression Output

    What value is assigned to the variable `message` in the following line of code?

    ```python
    score = 95
    message = "Passed" if score >= 60 else "Failed"
    ```

    ??? note "Show solution"
        `"Passed"`

        *Explanation*: The condition (`score >= 60`) is True (95 is greater than 60), so the value before the `if` (`"Passed"`) is assigned to the variable `message`.

??? tip "4. Google Colab: Try It Yourself"

    Practice basic conditional statements (`if` and `else`) and relational operators with this Colab notebook:

    👉 [Open the Conditionals & Relational Operators Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/07_conditionals.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "5. Mini-Quiz"

    ### 5.1. What happens when an `if` condition evaluates to True?  

    A) The program stops immediately.<br>
    B) The `else` block is executed anyway.<br>
    C) Only the `if` block runs.<br>
    D) Both blocks run.

    ??? info "Show answer"
        C) Only the `if` block runs.

    ### 5.2. Which operator would you use to check if a number of absences is greater than or equal to 6?

    A) `=`<br>
    B) `==`<br>
    C) `!=`<br>
    D) `>=`

    ??? info "Show answer"
        D) `>=`

    ### 5.3. What is the primary role of the `else` block in a conditional structure?

    A) Executes when the `if` condition is True.<br>
    B) Executes when the `if` condition is False.<br>
    C) Handles syntax errors.<br>
    D) Always executes.

    ??? info "Show answer"
        B) Executes when the `if` condition is False.

    ### 5.4. Which operator checks for equality in Python?

    A) `=`<br>
    B) `==`<br>
    C) `!=`<br>
    D) `>=`

    ??? info "Show answer"
        B) `==`

    ### 5.5. What happens if the `if` block is not indented correctly?

    A) Python ignores it.<br>
    B) Python raises an `IndentationError`.<br>
    C) It runs anyway.<br>
    D) The `else` block runs instead.

    ??? info "Show answer"
        B) Python raises an `IndentationError`.

??? warning "6. Common Mistakes"

    - Using `=` instead of `==` for comparisons.
    - Forgetting the colon `:` after `if` or `else` statements.
    - Incorrect indentation of conditional blocks.
    - Not converting input to `int`/`float` before comparing.

??? note "7. Summary Diagram"

    ```mermaid
    mindmap
      root((Conditional Structures))
        Flow Structures
          Block Structure
            if / else
          Single-Line Assignment
            Ternary Operator: A if C else B
        Building Blocks
          Relational Operators
            ==, <, >, >=, etc.
          Boolean Conditions
            True / False
        Key Rules
          Proper Indentation
          Only One Block Runs
    ```

??? tip "8. Optional Extensions"

    - Write a program that asks the user for a number and prints whether it is positive or negative using `if` and `else`.  
    - Modify the age example above (Commented Example 2.2) to include a category for children (e.g., below 12) and print `"Child"` or `"Adult"`.  
    - Research nested `if` statements and create a program that evaluates two conditions at once (e.g., age and temperature) and prints different messages accordingly.  