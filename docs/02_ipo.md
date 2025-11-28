---
hide:
  - toc
---

# 2. Input-Process-Output (IPO) Cycle

The core function of a computer program, or even computational logic, is summarized by the **Input-Process-Output (IPO)** cycle. This cycle is the fundamental model for how all algorithms operate, providing a structure for planning and execution.

* **Input**: The data or instructions the computer receives.
* **Process**: The computer follows programmed steps (algorithms) to transform the input data into something useful.
* **Output**: The delivered result or useful information.

A computer does not "think"; it strictly follows these defined processes.

??? info "1. The IPO Cycle Components"
    ## 1.1 Input: The Data Received
    Input is the data, ingredients, or materials needed to follow the algorithm. This can be typing a message or clicking a button.

    ### 1.1.1 Python Example (Input)
    | Python Function | Role in IPO | Explanation |
    | :--- | :--- | :--- |
    | `input("Enter name: ")` | **Input** | The `input()` function allows the user to enter data. |

    ## 1.2 Process: The Transformation
    The Process involves following programmed steps to transform the received data. This is where the algorithm's calculation and logic are applied.

    ### 1.2.1 Example Process Steps
    A typical process can be described as a sequence of precise actions:
    1. Read the input values.
    2. Validate the format of the data.
    3. Apply the required formula or transformation.
    4. Store the result in a variable for later use.

    ## 1.3 Output: The Delivered Result
    Output delivers the final result or product to the user. This can be showing corrected text, displaying a filtered photo, or calculating a total.

    ### 1.3.1 Python Example (Output)
    | Python Function | Role in IPO | Explanation |
    | :--- | :--- | :--- |
    | `print("Total:", total)` | **Output** | The `print()` function displays the result or text content to the console. |

??? example "2. Commented Examples"

    ### 2.1: Conceptual IPO Flow (BMI Calculation)

    | Component | Description | Example Data |
    | :--- | :--- | :--- |
    | **Input (Data)** | Required numerical values are fed into the system. | Age (55 years), Height (1.72 m), Weight (88 kg). |
    | **Process** | The system applies the BMI formula: Weight (kg) / Height (m)². | Core calculation and logic. |
    | **Output (Information)** | The BMI result is calculated and shown to the user. | Example: 29.7 → "You are overweight". |

    ### 2.2: Translation App (Google Translate)

    When you use a translation application:  
    
    * **Input**: The sentence you type in Spanish.  
    * **Process**: The system applies algorithms to map words and grammatical structures from Spanish to English.  
    * **Output**: The translated sentence received in English.  

??? question "3. Short Practice Exercises"

    ### 3.1: IPO Identification (Music App)

    When using Spotify, what is the **Input**, the **Process**, and the **Output**?

    ??? note "Show solution"
        - **Input**: The song title typed or spoken by the user.
        - **Process**: The computational search and retrieval that occurs before the song starts playing.
        - **Output**: The song playing.

    ### 3.2: Process Definition

    A program needs to calculate the total cost of movie tickets by multiplying the number of tickets by the unit price. Describe the specific **Process** step that performs this calculation.

    ??? note "Show solution"
        **Process**: Multiply the variable holding the number of tickets by the variable holding the unit price, and store the result in a 'total cost' variable.

    ### 3.3: Python Input/Output Functions

    Write the names of the two basic Python functions used to receive data from the user and display information to the console.

    ??? note "Show solution"
        **Input Function**: `input()`  
        **Output Function**: `print()`

??? question "4. Mini-Quiz"

    ### Q1. What is the role of the Process step in the IPO cycle?

    A) Storing raw data without changes  
    B) Following programmed steps to transform the data  
    C) Delivering the results to the screen  
    D) Receiving initial user data  

    ??? info "Show answer"
        **B) Following programmed steps to transform the data**

    ### Q2. In a navigation application, entering the destination address represents which stage of the IPO cycle?

    A) Output  
    B) Process  
    C) Input  
    D) Storage  

    ??? info "Show answer"
        **C) Input**

    ### Q3. Which of the following is an example of an Output delivered by a computer?

    A) Typing a song title in Spotify  
    B) The application displaying the retrieved song  
    C) Clicking a button to send a message  
    D) Entering a delivery address  

    ??? info "Show answer"
        **B) The application displaying the retrieved song**

    ### Q4. What is the main characteristic that distinguishes the Process from the Output?

    A) Process stores the information, Output deletes it  
    B) Process receives the input, Output ignores it  
    C) Process transforms the data, Output delivers the results  
    D) Process delivers the results, Output transforms the data  

    ??? info "Show answer"
        **C) Process transforms the data, Output delivers the results**

    ### Q5. When an application applies a photo filter chosen by the user, this action represents which part of the IPO cycle?

    A) Input  
    B) Output  
    C) Process  
    D) Debugging  

    ??? info "Show answer"
        **C) Process**

??? warning "5. Common Mistakes"

    - Confusing **physical actions** (clicking, typing) with the actual **data** used as Input  
    - Leaving out the **Process steps**, describing only the Input and Output  
    - Showing results without **clear labels** (e.g., printing just `12.5` instead of `Total cost: 12.5`)  
    - Mixing up **data used for a calculation** (Input) with the **information produced after** it (Output)

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