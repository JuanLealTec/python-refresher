---
hide:
  - toc
---

# 10. While Loop

A **while loop** is a primary control flow structure that repeats a **code block** as long as a specific condition remains True. This structure is particularly useful when the exact number of repetitions required is unknown in advance.

Understanding its termination is critical: a **while loop** must always be written so that the condition eventually becomes False. This essential update mechanism prevents the code from running forever in an **infinite loop**.

??? info "1. Loop Structure and Control Flow"

    ## 1.1. Basic Structure of a While Loop

    A while loop follows this general pattern:

    ```python
    while condition_is_true:
        # repeated instructions
    ```

    A loop continues to run as long as its condition evaluates to True, and it stops once the condition becomes False; the key idea is that something inside the **loop** must eventually change the **condition** so the cycle can end.

    ## 1.2. Updating the Control Variable

    To ensure the loop stops correctly, the value used in the condition must be updated:

    ```python
    count = 3
    while count > 0:
        print(count)
        count = count - 1   # update step
    ```

    If the update step is missing, the loop runs forever, creating an **infinite loop**.

    ## 1.3. Input Validation Using While

    A while loop can be used to validate user input, repeating a prompt until the data meets a required condition. This technique is useful when the program cannot assume the user will enter valid information on the first attempt.

    While loops can validate:  

    - numbers (ranges, positivity, limits)  
    - strings (allowed responses, formats)
    - booleans (True or False flags)

    #### 1.3.1. Validating Numerical Input

    When validating numbers, the loop continues as long as the value is outside the acceptable range. This prevents invalid data from entering the rest of the program.
    
    ```python
    age = int(input("Enter your age: "))
    while age < 0 or age > 120:     # invalid input
        print("Please enter a valid age.")
        age = int(input("Enter your age: "))
    ```

    #### 1.3.2. Validating String Input

    When validating strings, the loop ensures the user enters only one of the accepted options. This is useful for commands, menus, or categorical choices.
    
    ```python
    answer = input("Continue (yes/no): ")
    while answer != "yes" and answer != "no":     # invalid string
        print("Please type yes or no.")
        answer = input(""Continue (yes/no): ")
    ```

??? quote "2. Python Shorts (Video)"

    A short visual introduction to the while loop structure.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe
            src="https://www.youtube.com/embed/P9Sn8mDrgnc"
            title="Python Shorts: while Loop"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

    If the video doesn't load, open directly on YouTube: [Watch Python Shorts: while Loop ↗](https://www.youtube.com/watch?v=P9Sn8mDrgnc){target="_blank" rel="noopener noreferrer"}

??? example "3. Commented Examples"

    ### 3.1. Counting Down

    ```python
    # 1. Setup: Initialize the counter variable
    i = 5

    # 2. Loop: Continue while the condition is True
    while i > 0:  # Loop continues while i is positive
        # 3. Output: Print the current value of i
        print(i)
        # 4. Process: Decrease i to eventually stop the loop
        i = i - 1  # Update step prevents infinite loop
    ```

    Explanation:

    - While loops repeat a block of code as long as the condition is True.
    - The loop prints numbers from 5 down to 1.
    - Updating the counter prevents an infinite loop.
    - Once the condition becomes False (`i <= 0`), the loop stops.

    ### 3.2. Repeating Until Valid Input

    ```python
    # 1. Input: Prompt the user for a response
    answer = input("Do you want to continue (y/n)? ")

    # 2. Loop: Repeat while the input is invalid
    while answer != "y" and answer != "n":
        # 3. Output: Notify the user about invalid input
        print("Please, type y or n.")
        # 4. Process: Ask for input again
        answer = input("Do you want to continue (y/n)? ")
    ```

    Explanation:

    - This loop repeats only when the input fails validation (`answer` not "y" or "n").
    - The user is prompted until a valid response is given.
    - This pattern is useful for input validation in programs.

    ### 3.3. Sum Until Limit

    ```python
    # 1. Setup: Initialize total and counter variables
    total = 0
    number = 1

    # 2. Loop: Continue while total is less than 20
    while total < 20:
        # 3. Process: Add the current number to the total
        total = total + number
        # 4. Process: Increase the number for the next iteration
        number = number + 1
    ```

    Explanation:

    - The loop keeps adding numbers until `total` reaches or exceeds 20.
    - Each iteration increases the counter to eventually stop the loop.

??? question "4. Short Practice Exercises"

    ### 4.1. Predict the Output

    What will the following code print?

    ```python
    i = 3
    while i > 0:
        print(i)
        i = i - 1
    ```

    ??? note "Show solution"
        ```
        3
        2
        1
        ```

        *Explanation*: The loop repeats while `i > 0`. Each iteration decreases `i` by 1, stopping when `i` reaches 0.

    ### 4.2. Identify the Error

    What is wrong with the following code?

    ```python
    count = 1
    while count < 5
        print(count)
        count = count + 1
    ```

    ??? note "Show solution"
        The `while` statement is missing a colon at the end.

        *Correct version*: `while count < 5:`

    ### 4.3. Condition Check

    Which condition keeps a while loop running as long as the user has not typed "stop"?

    ??? note "Show solution"
        `while user_input != "stop":`

    ### 4.4. Loop Behavior

    What will the following code print?

    ```python
    n = 0
    while n < 3:
        print("Hello")
        n = n + 1
    ```

    ??? note "Show solution"
        ```
        Hello
        Hello
        Hello
        ```

        *Explanation*: The loop runs 3 times, incrementing `n` each iteration.

??? tip "5. Google Colab: Try It Yourself"

    Practice `while` loops with this interactive Colab notebook:

    👉 [Open the While Loop Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/10_while_loop.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "6. Mini-Quiz"

    ### 6.1.  Which line of code should be added to prevent an infinite loop?

    ```python
    x = 5
    while x > 0:
        print(x)
        # What should go here?
    ```

    A) `x = x + 1`<br>
    B) `x = x - 1`<br>
    C) `print(x)`<br>
    D) Nothing

    ??? info "Show answer"
        B) `x = x - 1`

    ### 6.2. What prevents an infinite loop?

    A) print() inside the loop.<br>
    B) Using `range()`.<br>
    C) Updating something so the condition can become False.<br>
    D) Adding another while loop.<br>

    ??? info "Show answer"
        C) Updating something so the condition can become False.

    ### 6.3. When does `while i < 6:` stop?

    A) When i becomes 1.<br>
    B) It still runs when i is 6.<br>
    C) It runs while i is less than 6.<br>
    D) It never stops.

    ??? info "Show answer"
        C) It runs while i is less than 6.

    ### 6.4. When is a while loop preferred over a for loop?

    A) When repeating over a known list.<br>
    B) When iterating a string.<br>
    C) When repetitions depend on user input.<br>
    D) When summing numbers from 1 to 10.

    ??? info "Show answer"
        C) When repetitions depend on user input.

    ### 6.5. What type of validation is this used for?

    `while age < 18 or age > 99:`

    A) Length verification.<br>
    B) Data type verification.<br>
    C) Range verification.<br>
    D) Form verification.

    ??? info "Show answer"
        C) Range verification.

??? warning "7. Common Mistakes"

    - Forgetting the update step → infinite loop.
    - Not initializing the variable used in the condition.
    - Using while when a for loop is more appropriate.
    - Incorrect validation logic (`and` vs. `or`).

??? note "8. Summary Diagram"

    ```mermaid
    mindmap
      root((While Loop))
        Concept
          Repeats as long as condition is True
          Useful when repetitions unknown in advance
        Stop Condition
          Update variables so loop ends
        Common Uses
          Counting
          Accumulation
          Input validation
        Key Points
          Prevent infinite loops
    ```

??? tip "9. Optional Extensions"

    - Modify Example 3.2 to accept "y/Y/n/N".  
    - Test what happens in a loop when you remove the update step (but stop execution manually!).  
    - Create a loop that counts how many invalid attempts the user makes before entering correct data.