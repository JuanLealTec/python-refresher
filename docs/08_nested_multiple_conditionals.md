---
hide:
  - toc
---

# 8. Nested & Multiple Conditionals

**Nested and multiple conditional statements** are the core structures for implementing multi-layered logic in a program. They allow the program to manage decisions that depend on several layers of criteria or on a sequence of mutually exclusive choices.

These structures are essential for handling complex and dynamic application development. They enable the computational logic to manage both exclusive sequences and hierarchical dependencies, matching the complexity of real-world scenarios.

??? info "1. Exclusive vs. Hierarchical Logic"

    ### 1.1. Multiple Conditionals

    This structure, using the `if/elif/else` chain, is used to handle multiple mutually exclusive cases (only one can be true). Conditions are evaluated in sequence from top to bottom.
    The first condition that evaluates to `True` executes its corresponding block, and the rest of the entire chain is immediately skipped.

    Exclusive Sequence Example:

    ```python
    score = 85

    if score > 90:
        # Checked first
        print("Grade A") 
    elif score > 80:
        # Only checked if 'score > 90' was False (and it is).
        # This block executes and the program skips the final 'else'.
        print("Grade B") 
    else:
        # Checked last (only if all 'if/elif' conditions were False).
        print("Grade C") 
    ```
    Key Takeaway: Using `elif` prevents subsequent conditions from being checked once a match is found, ensuring only one path runs.

    ### 1.2. Nested Conditionals

    A **nested `if`** statement places one `if` inside another (`if`, `elif`, or `else`) block. This creates a multi-level, hierarchical decision: the inner condition is only evaluated if the outer condition has already been confirmed as `True`.

    Hierarchical Dependence Example:

    ```python
    is_member = True
    has_coupon = True

    if is_member == True:
        # Step 1: Must be True to proceed to the next level (indentation)
        print("Member access confirmed.")
        if has_coupon == True:
            # Step 2: Only evaluated if Step 1 was True.
            print("20% extra discount applied.")
        else:
            # Executes if Step 1 was True, but the inner condition was False.
            print("No coupon, only member discount.")
    else:
        print("Guest access. No discounts.")
    ```

    Key Takeaway: The **indentation** visually enforces the dependency: the code block inside the outer `if` controls access to the inner `if`.

??? quote "2. Python Shorts (Video)"

    ### 2.1. Python Shorts: if/elif/else

    A quick Python Shorts video showing how to use if/elif/else.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe 
            src="https://www.youtube.com/embed/0ZWt_kTnFXs"
            title="Python Shorts: if/elif/else"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

    If the video doesn't load, open directly on YouTube: [Watch Python Shorts: if/elif/else ↗](https://www.youtube.com/watch?v=0ZWt_kTnFXs){target="_blank" rel="noopener noreferrer"}

    ### 2.2. Python Shorts: Nested if

    A short video demonstrating nested if statements in Python.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe 
            src="https://www.youtube.com/embed/ArDFcXjclfE"
            title="Python Shorts: Nested if"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

    If the video doesn't load, open directly on YouTube: [Watch Python Shorts: Nested if ↗](https://www.youtube.com/watch?v=ArDFcXjclfE){target="_blank" rel="noopener noreferrer"}

??? example "3. Commented Examples"

    ### 3.1. Multiple Conditions (`if/elif/else`)

    ```python
    # 1. Input: Get the student's average and convert to integer
    average = int(input("Enter your average: "))

    # 2. Decision Sequence: Check the highest scholarship threshold first
    if average >= 95:
        # 3. Output: Excellence awarded
        print("Excellence Scholarship") # Example Output: Excellence Scholarship
    elif average >= 85:
        # 4. Output: Check the next threshold only if the previous was False
        print("Academic Scholarship") # Example Output: Academic Scholarship
    else:
        # 5. Output: Executes if all preceding conditions were False
        print("No Scholarship") # Example Output: No Scholarship
    ```

    Explanation:

    - `if/elif/else` handles multiple, exclusive conditions.
    - Conditions are evaluated strictly in sequence from top to bottom.
    - Only the code block for the first True condition is executed; the rest are skipped.

    ### 3.2. Nested Conditions (`Nested if`)

    ```python
    # 1. Input: Get age and convert to integer
    age = int(input("How old are you? "))
    # 2. Input: Get ID status (string input)
    has_id = input("Do you have ID? (y/n): ")

    # 3. Decision Hierarchy (Outer): Check the primary requirement (age)
    if age >= 18:
        # 4. Decision Hierarchy (Inner): Check the secondary requirement (ID)
        if has_id.lower() == "y":
            # 5. Output: Requirements met
            print("You can enter.") # Example Output (True/True): You can enter.
        else:
            # 6. Output: Secondary requirement failed
            print("You need ID.") # Example Output (True/False): You need ID.
    else:
        # 7. Output: Primary requirement failed
        print("You must be of age to enter.") # Example Output (False): You must be of age to enter.
    ```

    Explanation:

    - Nested `if` statements are `if` blocks inside another `if`.
    - The inner condition is only checked if the outer condition is True.
    - They are used to establish sequential or hierarchical requirements.

??? question "4. Short Practice Exercises"

    ### 4.1. Predict the Output (`if/else`)

    What will be printed by the following code?

    ```python
    age = 16
    if age >= 18:
        print("Adult")
    else:
        print("Minor")
    ```

    ??? note "Show solution"
        `"Minor"`.

        *Explanation*: The condition `age >= 18` is False, so the `else` block executes.

    ### 4.2. Nested `if`

    Predict the output of the following nested if structure:

    ```python
    age = 20
    has_id = "n"
    if age >= 18:
        if has_id.lower() == "y":
            print("Can enter")
        else:
            print("Need ID")
    else:
        print("Too young")
    ```

    ??? note "Show solution"
        `"Need ID"`

        *Explanation*: The outer condition `age >= 18` is True, so the inner `if` is evaluated. `has_id.lower() == "y"` is False, so the inner `else` executes.

    ### 4.3. Correct the Code

    The following code is intended to print `"Eligible"` if `score >= 50` and `"Not eligible"` otherwise. Correct it:

    ```python
    score = 45
    if score >= 50
        print("Eligible")
    else:
    print("Not eligible")
    ```

    ??? note "Show solution"
        ```python
        score = 45
        if score >= 50:
            print("Eligible")
        else:
            print("Not eligible")
        ```

        *Explanation*: The `if` line needs a colon, and both blocks must be properly indented.

    ### 4.4. Logical Sequence Check

    Read the code and indicate what will be printed:

    ```python
    balance = 100
    pin_entered = False
    if balance > 0:
        if pin_entered:
            print("Withdrawal allowed")
        else:
            print("Enter PIN")
    else:
        print("Insufficient funds")
    ```

    ??? note "Show solution"
        `"Enter PIN"`

        *Explanation*: Balance is positive, so the outer `if` passes. PIN was not entered, so the inner `else` executes.

??? tip "5. Google Colab: Try It Yourself"

    Practice nested and multiple conditional structures (`if-elif-else`) with this Colab notebook:

    👉 [Open the Nested & Multiple Conditionals Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/08_nested_multiple_conditionals.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "6. Mini-Quiz"

    ### 6.1. What happens when a condition in an `if/elif/else` chain evaluates to True?

    A) All remaining conditions are evaluated.<br>
    B) The program stops immediately.<br>
    C) The rest of the chain is skipped.<br>
    D) Only the else part runs.

    ??? info "Show answer"
        C) The rest of the chain is skipped.

    ### 6.2. Which structure allows a second decision only after a primary condition is True?

    A) Compound conditional<br>
    B) `if/elif/else`<br>
    C) Nested if<br>
    D) `or` operator

    ??? info "Show answer"
        C) Nested if

    ### 6.3. What will the following code print?  

    ```python
    x = 5
    y = 10
    if x > 3:
        if y > 8:
            print("A")
        else:
            print("B")
    else:
        print("C")
    ```

    A) A<br>
    B) B<br>
    C) C<br>
    D) ABC

    ??? info "Show answer"
        A) A

    ### 6.4. What does `elif` stand for in Python?

    A) else loop<br>
    B) else if<br>
    C) else function<br>
    D) if else

    ??? info "Show answer"
        B) else if

    ### 6.5. When is it better to use an `if/elif/else` structure instead of a nested `if`?

    A) When you want all conditions to be checked even after one is true.<br>
    B) When the conditions are not mutually exclusive.<br>
    C) When you need only a single level of decision-making.<br>
    D) When only one condition should be true and trigger an action.

    ??? info "Show answer"
        D) When only one condition should be true and trigger an action.

??? warning "7. Common Mistakes"

    - Using multiple independent `if` statements instead of an `if/elif/else` chain when only one path should execute.
    - Incorrect indentation in nested if blocks.
    - Skipping type conversion when using `input()` for numerical comparisons.
    - Assuming inner `if` runs without the outer condition being True.

??? note "8. Summary Diagram"

    ```mermaid
    mindmap
      root((Nested & Multiple Conditionals))
        Multiple Conditions if/elif/else
          Sequence of checks
          First True condition runs and rest skipped
        Nested Conditions
          Hierarchical evaluation
          Inner if executes only if outer is True
        Key Points
          Correct evaluation order
          Proper indentation
    ```

??? tip "9. Optional Extensions"

    - Write a program that asks for a number and prints whether it is positive, negative, or zero using nested `if` statements.
    - Modify Commented Example 3.1 to include a "Merit Scholarship" category for averages between 90 and 94 and print the corresponding scholarship.
    - Create a program that evaluates multiple conditions with a combination of nested `if` statements and logical operators, e.g., age, membership status and score to decide eligibility for a program.