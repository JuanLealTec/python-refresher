---
hide:
  - toc
---

# 2. Input-Process-Output

The **Input-Process-Output (IPO) cycle** is a foundational model for **algorithms**, serving as the blueprint for any computer program.

This framework defines the three essential stages necessary for any computational logic to function. It underscores a critical principle: a computer does not "think" independently but executes these predefined steps with precision.

??? info "1. The IPO Cycle Components"

    ### 1.1. Input: The Data Received

    **Input** is the **data**, ingredients, or materials needed to follow the algorithm. This can be typing a message or clicking a button.

    Python Example (Input):

    | Python Function | IPO Role | Description |
    | :--- | :--- | :--- |
    | `input("Enter name: ")` | Input | Receives user data |

    ### 1.2. Process: The Transformation

    The Process involves following programmed steps to transform the received data. This is where the algorithm's calculation and logic are applied.

    A typical process can be described as a sequence of precise actions:

    1. Read the input values.
    2. Validate the format of the data.
    3. Apply the required formula or transformation.
    4. Store the result in a variable for later use.

    ### 1.3. Output: The Delivered Result

    Output is the final, useful result produced after the Process step is complete.

    Python Example (Output):

    | Python Function | IPO Role | Description |
    | :--- | :--- | :--- |
    | `print("Hello!")` | Output | Displays information to user |

??? example "2. Commented Examples"

    ### 2.1. Body Mass Index (BMI) Calculation

    | Component | Example Data | Explanation |
    | :--- | :--- | :--- |
    | **Input** | Age: 55 years, Height: 1.72 m, Weight: 88 kg | Required numerical values are fed into the system |
    | **Process** | Apply BMI formula: Weight (kg) / Height (m)² | The system performs the calculation using the formula |
    | **Output** | BMI result: 29.7 → "You are overweight" | The result is displayed to the user |

    ### 2.2. Translation App

    | Component | Example Data | Explanation |
    | :--- | :--- | :--- |
    | **Input** | Sentence typed in Spanish | User provides the text to be translated |
    | **Process** | Algorithm maps words and grammar from Spanish to English | The system applies translation logic |
    | **Output** | Translated sentence in English | The translated text is shown to the user |

??? question "3. Short Practice Exercises"

    ### 3.1. IPO Identification

    When using Spotify, what is the Input, the Process, and the Output?

    ??? note "Show solution"
        - Input: The song title typed or spoken by the user.
        - Process: The computational search and retrieval that occurs before the song starts playing.
        - Output: The song playing.

    ### 3.2. Process Definition

    A program needs to calculate the total cost of movie tickets by multiplying the number of tickets by the unit price. Describe the specific Process step that performs this calculation.

    ??? note "Show solution"
        Process: Multiply the variable holding the number of tickets by the variable holding the unit price, and store the result in a 'total cost' variable.

    ### 3.3. Python Input/Output Functions

    Write the names of the two basic Python functions used to receive data from the user and display information to the console.

    ??? note "Show solution"
        - Input function: `input()`.  
        - Output function: `print()`.

    ### 3.4. Identify the Missing IPO Step

    A program receives a user's temperature in Celsius and converts it to Fahrenheit. The steps below are given, but step 2 is missing. Fill in the missing Process step.

    1. Input: User enters temperature in Celsius
    2. Process:
    3. Output: Display the temperature in Fahrenheit

    ??? note "Show solution"
        Convert Celsius to Fahrenheit using the formula `F = (C * 9/5) + 32`.

??? question "4. Mini-Quiz"

    ### 4.1. What is the role of the Process step in the IPO cycle?

    A) Storing raw data without changes.<br>
    B) Following programmed steps to transform the data.<br>
    C) Delivering the results to the screen.<br>
    D) Receiving initial user data.

    ??? info "Show answer"
        B) Following programmed steps to transform the data.

    ### 4.2. In a navigation application, entering the destination address represents which stage of the IPO cycle?

    A) Output<br>
    B) Process<br>
    C) Input<br>
    D) Storage  

    ??? info "Show answer"
        C) Input

    ### 4.3. Which of the following is an example of an Output delivered by a computer?

    A) Typing a song title in Spotify.<br>
    B) The application displaying the retrieved song.<br>
    C) Clicking a button to send a message.<br>
    D) Entering a delivery address.

    ??? info "Show answer"
        B) The application displaying the retrieved song.

    ### 4.4. What is the main characteristic that distinguishes the Process from the Output?

    A) Process stores the information, Output deletes it.<br>
    B) Process receives the input, Output ignores it.<br>
    C) Process transforms the data, Output delivers the results.<br>
    D) Process delivers the results, Output transforms the data.

    ??? info "Show answer"
        C) Process transforms the data, Output delivers the results.

    ### 4.5. When an application applies a photo filter chosen by the user, this action represents which part of the IPO cycle?

    A) Input<br>
    B) Output<br>
    C) Process<br>
    D) Debugging

    ??? info "Show answer"
        C) Process

??? warning "5. Common Mistakes"

    - Confusing physical actions (clicking, typing) with the actual data used as Input.
    - Leaving out the Process steps, describing only the Input and Output.
    - Showing results without clear labels (e.g., printing just `12.5` instead of `Total cost: 12.5`).
    - Mixing up data used for a calculation (Input) with the information produced after it (Output).

??? note "6. Summary Mindmap"

    ```mermaid
    mindmap
      root((IPO Cycle))
        Input
          Data Received
          Example: Typed text, button click
          Python: input
        Process
          Transformation of Data
          Following programmed steps (Algorithm)
          Example: Formula Calculation, Search Logic
        Output
          Delivered Result
          Example: Displayed text, song playing
          Python: print
    ```

??? tip "7. Optional Extensions"

    - Analyze three apps and identify their Input, Process, and Output.
    - Write an algorithm for an online shopping checkout process using IPO.
    - Research how data types (string vs. integer) affect the Process in Python.