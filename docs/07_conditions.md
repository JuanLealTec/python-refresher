---
hide:
  - toc
---

# 7. Conditions: IF, ELIF, ELSE

Conditional statements are fundamental in programming because they allow a program to **make decisions** and execute different code based on specific conditions. Using `if`, `elif`, and `else`, a program can respond to different situations, compare values, and guide the flow of execution. Understanding these statements is essential for building dynamic and interactive Python programs.

??? info "1. Brief Explanation"
    Conditional structures allow a program to make decisions based on **Boolean conditions**.  

    - The **`if`** statement checks the first condition; if True, its indented code block runs.  
    - The **`elif`** (short for *else if*) checks additional conditions **only if all preceding if/elif conditions were False**.  
    - The **`else`** block runs only if none of the previous conditions were True.  

    **Important points:**
    - Only the **first True condition executes**, and the rest of the chain is skipped.  
    - Use **relational operators** (`==`, `!=`, `<`, `>`, `<=`, `>=`) to compare values.  
    - **Indentation** is mandatory to define which statements belong to each conditional block.

    ## 1.1 Relational Operators
    Relational operators allow Python to compare values and evaluate conditions. The most common ones are:
    | Operator | Description | Example |
    | :--- | :--- | :--- |
    | `==` | Equals | `x == 10` → True if x is 10 |
    | `!=` | Not equal | `x != 5` → True if x is not 5 |
    | `>` | Greater than | `x > 3` → True if x is greater than 3 |
    | `<` | Less than | `x < 7` → True if x is less than 7 |
    | `>=` | Greater than or equal | `x >= 18` → True if x is 18 or older |
    | `<=` | Less than or equal | `x <= 100` → True if x is 100 or less |

??? quote "2. Python Shorts (Video)"
    A quick Python Shorts video showing how to use if…elif…else.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe 
            src="https://www.youtube.com/embed/7FILd3kvs70"
            title="Python Shorts: if…elif…else"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

??? example "3. Commented Examples"
    ### 3.1 Basic `if...else` Structure
    **Note:** These examples assume the user enters numeric input.  
    If a non-numeric value is entered, Python will raise an error.

    ```python
    # Ask for age and convert to integer
    age = int(input("How old are you? "))

    if age >= 18:
        # Executes if age is 18 or older
        print("You can enter the party!")
    else:
        # Executes if the above condition is False
        print("Sorry, you cannot enter the party.")
    ```

    ### 3.2 Using `elif` for Multiple Conditions
    ```python
    # Ask for student's average grade
    average = int(input("Enter your average grade: "))

    if average >= 95:
        # First condition checked
        print("Excellence Scholarship")
    elif average >= 85:
        # Checked only if the first condition was False
        print("Academic Scholarship")
    else:
        # Executes if neither of the above conditions is True
        print("No Scholarship")
    ```

??? question "4. Short Practice Exercises"
    ### 4.1: Operator Selection
    Which relational operator checks if the variable `inventory` is **strictly less than** 100?

    A) `<= 100`  
    B) `< 100`  
    C) `!= 100`

    ??? note "Show solution"
        **B) `< 100`**

    ### 4.2: Prediction of Output
    What is the final output of the following code block?

    ```python
    x = 10
    if x > 5:
        print("A")
    elif x == 10:
        print("B")
    else:
        print("C")
    ```
    
    ??? note "Show solution"
        **Output:** `"A"`  
        *Explanation: The first condition (`x > 5`) is True, so the rest of the `elif`/`else` chain is skipped.*

    ### 4.3: Error Correction
    How should the code be corrected to check if `current_state` is equal to `"running"`?

    ```python
    current_state = "running"
    # if current_state = "running":
    #     print("System active")
    ```

    ??? note "Show solution"
        The comparison operator `==` must be used instead of the assignment operator `=`:
        ```python
        current_state = "running"
        if current_state == "running":
            print("System active")
        ```

    ### 4.4: Indentation Error
    Identify the error in the following conditional structure:

    ```python
    user_status = True
    if user_status:
    print("Welcome")
    ```

    ??? note "Show solution"
        **Indentation Error.** The statement inside the `if` block (`print("Welcome")`) must be indented (usually 4 spaces).

??? tip "5. Google Colab: Try It Yourself"
    Practice conditional statements, if...elif...else chains, and input conversion with this Colab notebook:

    👉 [Open the Conditions Colab notebook ↗](https://colab.research.google.com/drive/1QIbINLkf4zGFNGPqJ2j2iaRtuL1Zmg6d?usp=sharing){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;">**First time using Google Colab?**</span> <a href="/colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "6. Mini-Quiz"
    ### Q1. What happens when a condition in an if...elif...else chain evaluates to True?
    A) The program stops immediately  
    B) All remaining conditions are evaluated  
    C) The rest of the chain is skipped  
    D) Only the else part runs  

    ??? info "Show correct answer"
        **C) The rest of the chain is skipped**

    ### Q2. Which operator would you use to check if a number of absences is greater than or equal to 6?
    A) =  
    B) ==  
    C) !=  
    D) >=  

    ??? info "Show correct answer"
        **D) >=**

    ### Q3. What is the primary role of the else block in a conditional structure?
    A) Executes when the if or elif condition is True  
    B) Executes when the preceding if and elif conditions are False  
    C) Handles syntax errors  
    D) Always executes regardless of conditions  

    ??? info "Show correct answer"
        **B) Executes when the preceding if and elif conditions are False**

    ### Q4. What does the keyword elif stand for in Python conditional logic?
    A) else function  
    B) else if  
    C) else loop  
    D) if else  

    ??? info "Show correct answer"
        **B) else if**

    ### Q5. In Python, when an if statement is used inside another if statement, what is this structure called?
    A) Compound conditional  
    B) if...elif...else  
    C) Nested if  
    D) Loop  

    ??? info "Show correct answer"
        **C) Nested if**

??? warning "7. Common Mistakes"
    - Using `=` instead of `==` for comparisons  
    - Forgetting the colon `:` after if, elif, or else statements  
    - Incorrect indentation of conditional blocks  
    - Not converting input to int/float before comparing  

??? note "8. Summary Diagram"
    ```mermaid
    mindmap
      root((Conditional Structures))
        Basic Conditional
          If Statement
        Multiple Conditions
          Elif Statement
        Default Option
          Else Statement
        Key Rules
          First True Condition Executes
          Only One Block Runs
          Proper Indentation
    ```

??? tip "9. Optional Extensions"
    - Write a program that asks the user for a number and prints whether it is positive, negative, or zero using if...elif...else  
    - Modify the scholarship example to include an additional category for students with average 75–84 and print `"Merit Scholarship"`  
    - Research nested if statements and create a program that determines grade and scholarship eligibility simultaneously