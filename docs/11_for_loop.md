---
hide:
  - toc
---

# 11. For Loop

A **for loop** is a primary control flow structure used to repeat a **code block** a defined number of times. It is the preferred loop when the sequence of items to process is known in advance.

By operating over an **iterable sequence**, this structure automatically manages the count. This ensures the **computational logic** is more efficient and streamlined for clearly defined repetition tasks.

??? info "1. Loop Structure and Control Flow"

    ## 1.1. Basic Structure and Iteration

    A **for loop** repeats a block of code for a defined number of times or for each item in a sequence. It handles the iteration automatically, meaning you do not need to manually manage an index variable.

    ```python
    # General Structure
    for variable in iterable_sequence:
        # repeated instructions (code block)
    ```

    The loop's control flow is determined by the `iterable_sequence`. For every item in that sequence, the code block runs once. The loop variable (`variable` in the example) takes on the value of the current item in each turn.

    ## 1.2. The range() Function

    The built-in `range()` function is the primary way to execute a for loop a specific number of times. It generates a sequence of numbers that the loop iterates through.

    | Function Form | Description |
    | :--- | :--- |
    | `range(stop)` | Generates a sequence from 0 up to, but not including, `stop`. |
    | `range(start, stop)` | Generates a sequence from `start` up to, but not including, `stop`. |
    | `range(start, stop, step)` | Generates a sequence from `start` up to, but not including, `stop`, incrementing or decrementing by `step`. |

??? quote "2. Python Shorts (Video)"

    A quick, visual explanation of the `for` loop.

    <div style="position: relative; width: 100%; max-width: 360px; margin: 0 auto; aspect-ratio: 9 / 16;">
        <iframe 
            src="https://www.youtube.com/embed/qiwK7-6_QAg"
            title="Python Shorts: for Loop"
            style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen>
        </iframe>
    </div>

    If the video doesn't load, open directly on YouTube: [Watch Python Shorts: for Loop ↗](https://www.youtube.com/watch?v=qiwK7-6_QAg){target="_blank" rel="noopener noreferrer"}
    
??? example "3. Commented Examples"

    ### 3.1. Iterating a Defined Range

    ```python
    # 1. Loop: Use for to display the numbers from 2 to 5
    for n in range(2, 6):
        # 2. Output: Print the current number
        print(n)
    # Output:
    # 2
    # 3
    # 4
    # 5
    ```

    Explanation:

    - The `range(2, 6)` function generates a sequence starting at 2 and stopping strictly before 6.
    - The for loop runs for a known, defined number of iterations (4 times).
    - The loop variable (`n`) automatically takes the values: 2, 3, 4, and 5.

    ### 3.2. Using the Step Parameter for Countdown

    ```python
    # 1. Loop: Use for a countdown, counting backwards by 5
    for x in range(20, 1, -5):
        # 2. Output: Print the current number
        print(x)
    # Output:
    # 20
    # 15
    # 10
    # 5
    ```

    Explanation:

    - The loop uses a negative step (`-5`) to count backward from the `start` value (20).
    - The loop continues until the value reaches the `stop` boundary (1).
    - This structure is used for sequences where the number is decreasing in a fixed interval.

    ### 3.3. Iterating Over a String

    ```python
    # 1. Setup: Initialize the variable word
    word = "Python"
    # 2. Loop: Iterate over each characters in word
    for char in word:
        #3. Output: Print the current character
        print(char)
    # Output:
    # P
    # y
    # t
    # h
    # o
    # n
    ```

    Explanation:

    - For loops are used to directly iterate through any iterable sequence (like a string).
    - In each turn, the loop variable (`char`) automatically holds the value of the current item (letter).
    - The loop executes once for every item in the sequence.

??? question "4. Short Practice Exercises"

    ### 4.1. Predict the Output (Iterating a String)

    What will be printed by the following code?

    ```python
    word = "LOOP"
    for letter in word:
        print(letter)
    ```

    ??? note "Show solution"
        ```
        L
        O
        O
        P
        ```

        *Explanation*: The for loop iterates through the string, printing each character on a new line.

    ### 4.2. Predict the Output (Counting with Step)

    What numbers will be printed by the following loop?

    ```python
    # Prints multiples of 3
    for num in range(3, 16, 3):
        print(num)
    ```

    ??? note "Show solution"
        ```
        3
        6
        9
        12
        15  
        ```

        *Explanation*: The sequence starts at 3, increases by a step of 3, and stops before the number 16 (exclusive), resulting in multiples up to 15.

    ### 4.3. Predict Final Value

    What is the final value of the `total` variable after the following code snippet executes?

    ```python
    total = 0
    for i in range(1, 8):
        total = total + i
    ```

    ??? note "Show solution"
        28

        *Explanation*: The loop calculates the sum of numbers from 1 up to and including 7 (`range(1, 8)`), which is 1 + 2 + 3 + 4 + 5 + 6 + 7 = 28.

    ### 4.4. Correct the Code (Reverse Count)

    The following code is intended to count down by ones from 8 to 3 (inclusive). Correct the `range()` function so that it prints 8, 7, 6, 5, 4, 3.

    ```python
    # Incorrect countdown:
    for i in range(8, 3, 1):
        print(i)
    ```

    ??? note "Show solution"
        ```python
        # Correct countdown:
        for i in range(8, 2, -1):
            print(i)
        ```

        *Explanation*: For a countdown, the step must be negative (`-1`), and the stop value must be 1 less than the last desired number (stopping at 2 is necessary to include 3).

??? tip "5. Google Colab: Try It Yourself"

    Practice `for` loops with this interactive Colab notebook:

    👉 [Open the For Loope Colab notebook ↗](https://colab.research.google.com/github/JuanLealTec/python-refresher/blob/main/docs/assets/notebooks/11_for_loop.ipynb){target="_blank" rel="noopener"}

    <span style="color:#1a73e8;"><strong>First time using Google Colab?</strong></span> <a href="../colab_instructions/" target="_blank" rel="noopener">Read the quick beginner guide ↗</a>

??? question "6. Mini Quiz"

    ### 6.1. What is the main characteristic that distinguishes a for loop from a while loop?

    A) The for loop runs as long as a condition is true.<br>
    B) The for loop repeats a known, defined number of times.<br>
    C) The for loop is only used for comparisons.<br>
    D) The for loop cannot contain if statements.

    ??? info "Show answer"
        B) The for loop repeats a known, defined number of times.

    ### 6.2. If you use `range(1, 10, 2)`, what does the number '10' represent?

    A) The starting number of the sequence.<br>
    B) The step size between numbers.<br>
    C) The number that the sequence will stop immediately before (exclusive).<br>
    D) The number of times the loop will run.

    ??? info "Show answer"
        C) The number that the sequence will stop immediately before (exclusive).

    ### 6.3. What is the output of the Python code `for n in range(4): print(n)`?

    A) 1 2 3 4<br>
    B) 0 1 2 3<br>
    C) 0 1 2 3 4<br>
    D) 4

    ??? info "Show answer"
        B) 0 1 2 3

    ### 6.4. How do you create a sequence that counts backward (e.g., from 10 down to 1) using the `range()` function?

    A) By making the start parameter negative.<br>
    B) By omitting the stop parameter.<br>
    C) By using a negative value for the step parameter.<br>
    D) By using the while loop instead.

    ??? info "Show answer"
        C) By using a negative value for the step parameter.

    ### 6.5. In the structure `for variable in iterable:`, what defines the instructions that will be repeated in each iteration?

    A) The use of the `range()` function.<br>
    B) The statements placed outside the loop structure.<br>
    C) The statements that are correctly indented below the `for` statement.<br>
    D) The variable name used in the loop.

    ??? info "Show answer"
        C) The statements that are correctly indented below the `for` statement.

??? warning "7. Common Mistakes"

    - Confusing for loop with while loop when iterations are unknown.
    - Assuming the stop value in `range()` is inclusive (it is always exclusive).
    - Forgetting the Colon (`:`) at the end of the `for` statement line.
    - Trying to manually modify the for loop variable (`n = n + 1`), which is automatic.

??? note "8. Summary Diagram"

    ```mermaid
    mindmap
      root((For Loop))
        Concept
          Repeats a known number of times
          Iterates over a sequence
        range Function
          Defines start, stop, and step
          Used for counting
        Iteration
          Automatically manages the loop variable
          Used on strings, lists, or sequences
        Key Points
          Don't manually change the loop variable
          Stop value is exclusive
    ```

??? tip "9. Optional Extensions"

    - Research and demonstrate how to use a for loop inside another for loop to print a multiplication table (e.g., 1x1 to 10x10).
    - Explore the `break` and `continue` keywords and write a program using them to exit or skip iterations within a `for` loop.
    - Write a Python program that initializes a variable to calculate the factorial of a number (e.g., 5! = 5 * 4 * 3 * 2 * 1) using a for loop.