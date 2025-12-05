---
hide:
  - toc
---

# 9. Compound Conditions

**Compound conditions** allow programs to evaluate multiple criteria at the same time. By combining conditions with Logical Operators, you can write clearer and more powerful decision-making logic.

These structures are essential for handling complex, real-world scenarios. They enable your program's computational logic to manage decisions that depend on several requirements simultaneously, providing flexibility and precision.

??? info "1. Compound Logic and Boolean Evaluation"

    ## 1.1 The `and` Operator

    Use `and` when all conditions must be True for the whole expression to be True.

    ```mermaid
    flowchart LR
        A[Condition 1] --> B{and}
        C[Condition 2] --> B
        B --> D[True only if both are True]
    ```

    Example:
    ```python
    age = 20
    has_ticket = True

    if age >= 18 and has_ticket:
        print("Access granted")
    ```

    ## 1.2 The `or` Operator

    Use `or` when at least one of the conditions must be True for the whole expression to be True.

    ```mermaid
    flowchart LR
        A[Condition 1] --> B{or}
        C[Condition 2] --> B
        B --> D[True if any is True]
    ```

    Example:
    ```python
    country = "Canada"

    if country == "USA" or country == "Canada":
        print("Eligible region")
    ```

    ## 1.3 The `not` Operator

    Use `not` to invert a condition.  

    - `not True` becomes `False`  
    - `not False` becomes `True`

    ```mermaid
    flowchart LR
        A[Condition] --> B{not}
        B --> C[Inverted Result]
    ```

    Example:
    ```python
    has_id = False

    if not has_id:
        print("ID required")
    ```

??? quote "2. Python Shorts (Video)"

    A Python Shorts video demonstrating how to combine conditions using and, or.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe 
            src="https://www.youtube.com/embed/V92IBY3rjVQ"
            title="Python Shorts: Compound Conditions (and, or)"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

    If the video doesn't load, open directly on YouTube: [Watch Python Shorts: Compound Conditions (and, or) ↗](https://www.youtube.com/watch?v=V92IBY3rjVQ){target="_blank" rel="noopener noreferrer"}

??? example "3. Commented Examples"

    ### 3.1. Using `and` for Simultaneous Requirements

    ```python
    # 1. Setup: Define an integer variable (int)
    num = 25

    # 2. Decision: Check if number is between 20 and 30 (both conditions must be True)
    if num >= 20 and num <= 30:
        # 3. Output: Executes only if both conditions are True
        print("Number between 20 and 30")
    ```

    Explanation:

    - Compound conditions combine multiple comparisons using `and` or `or`.
    - The `and` operator executes the block only if both conditions are True.
    - Python evaluates from left to right and stops if one condition is False.
    - This allows multiple requirements to be checked in a single `if` statement.

    ### 3.2. Using `or` for Alternative Requirements

    ```python
    # 1. Setup: Define an integer variable (int)
    stock = 0
    # 2. Setup: Define an boolean variable (bool)
    has_priority_order = True

    # 3 Decision: Check if stock is empty or there is a priority order
    if stock == 0 or has_priority_order:
        # 4. Output: Executes if at least one condition is True
        print("Order can be processed")
    ```

    Explanation:

    - The `or` operator executes the block if at least one condition is True.
    - Python evaluates conditions from left to right and stops if one is True (short-circuit).
    - This allows alternatives to satisfy a single requirement.

    ### 3.3. Using `not` for Logical Inversion

    ```python
    # 1. Setup: Define a boolean variable (bool)
    is_online = False

    # 2. Decision: Check if user is not online
    if not is_online:
        # 3. Output: Executes when the condition is True
        print("User is offline")
    ```

    Explanation:

    - The `not` operator reverses a Boolean value.
    - `not False` becomes True, and `not True` becomes False.
    - This allows checking the opposite of a condition in a single statement.

??? question "4. Short Practice Exercises"

    ### 4.1. Multiple Requirements (`and`)

    What will the following code print if `average = 92` and `absences = 0`?

    ```python
    if average > 90 and absences == 0:
        print("Eligible")
    ```

    ??? note "Show solution"
        `"Eligible"`

        *Explanation*: `and` requires both conditions to be True. Since `92 > 90` is True and `0 == 0` is True, the combined expression is True.

    ### 4.2. Alternative Requirements (`or`)

    Consider the code below. If `senior_citizen = False` and `purchase_total = 1200`, will the message `"Discount Applied"` be printed?
 
    ```python
    if senior_citizen or purchase_total > 1000:
        print("Discount Applied")
    ```

    ??? note "Show solution"
        Yes

        *Explanation*: `or` is True if at least one condition is met; since `1200 > 1000` is True, the entire expression passes.

    ### 4.3. Range Validation (`and`)

    Does the following condition correctly evaluate whether `month` is between 1 and 12?

    ```python
    month >= 1 and month <= 12
    ```

    ??? note "Show solution"
        Yes

        *Explanation*: `and` requires both conditions (`month >= 1` and `month <= 12`) to be True to validate the month is within the inclusive range.

    ### 4.4. Logical Evaluation

    Determine the result of:  
    ```python
    (100 < 50) or (7 == 7)
    ```

    ??? note "Show solution"
        True

        *Explanation*: `or` is True if at least one condition is True; since `7 == 7`, the whole expression is True.

??? tip "5. Google Colab: Try It Yourself"

    Practice compound conditions with this interactive Colab notebook:

    👉 [Open the Compound Conditions Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/09_compound_conditions.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "6. Mini-Quiz"

    ### 6.1. What is a compound condition?

    A) A statement that tests one condition only.<br>
    B) A condition that includes a loop.<br>
    C) A statement combining two or more conditions.<br>
    D) A condition that always returns True.

    ??? info "Show answer"
        C) A statement combining two or more conditions.

    ### 6.2. Which logical operator returns True only if both conditions are True?

    A) `or`<br>
    B) `not`<br>
    C) `and`<br>
    D) `if`

    ??? info "Show answer"
        C) `and`

    ### 6.3. What is the result of the expression `(5 > 3) and (2 < 1)`?

    A) True<br>
    B) False<br>
    C) None<br>
    D) Error

    ??? info "Show answer"
        B) False

    ### 6.4. Which condition checks if `num` is between 10 and 50 (inclusive)?

    A) `num > 10 or num < 50`<br>
    B) `num >= 10 and num <= 50`<br>
    C) `num <= 10 or num >= 50`<br>
    D) `num == 10 and num == 50`

    ??? info "Show answer"
        B) `num >= 10 and num <= 50`

    ### 6.5. Which operator returns True if at least one condition is True?

    A) `and`<br>
    B) `or`<br>
    C) `not`<br>
    D) `elif`

    ??? info "Show answer"
        B) `or`

??? warning "7. Common Mistakes"

    - Mixing up `and` and `or` when checking ranges.
    - Using `or` when checking a value inside a range.
    - Misusing `not` and unintentionally reversing logic.
    - Forgetting relational operators inside compound conditions.

??? note "8. Summary Diagram"

    ```mermaid
    mindmap
      root((Compound Conditions))
        Logical Operators
          and - all conditions True
          or - at least one True
          not - logical inversion
        Common Uses
          Range checks
          Multiple requirements
          Alternative conditions
        Key Points
          Boolean evaluation
          Clear logical structure
    ```

??? tip "9. Optional Extensions"

    - Write a program that asks for age and membership status and determines discount eligibility using `and` and `or`.
    - Extend Example 3.1 so that it also prints `"Out of range"` when the number is below 20 or above 30.
    - Research how Python evaluates compound conditions using short-circuit evaluation and test it with print statements.