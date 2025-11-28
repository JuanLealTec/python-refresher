---
hide:
  - toc
---

# 2. Algorithms

An Algorithm is a precise, step-by-step set of instructions designed to solve a specific task. Algorithms represent the core planning phase of computational thinking, known as Algorithmic Design, and are developed before a program is ever written in code.  
An algorithm is like a meticulously organized building blueprint: it describes the exact, ordered steps required to turn raw materials (Input) into the final structure (Output) before any actual construction (Programming) begins.

??? info "1. Components and Properties"

    A valid and effective algorithm operates on the fundamental **Input-Process-Output (IPO)** model. The **Process** is the algorithm itself—the sequence of detailed steps that transforms the raw **Input** into the desired **Output**. This Process must meet the five essential properties listed below.

    ## 1.1 Properties: Essential Characteristics

    | Property | Description | Why it matters |
    | :--- | :--- | :--- |
    | **Input** | The initial data or materials required to start the process. | An algorithm cannot run without clearly defined resources. |
    | **Output** | The specific, expected result or product of the algorithm. | If the goal is not defined, the algorithm is useless. |
    | **Precise** | Every step must be clearly specified, unambiguous, and executable. | Computers require exact instructions; vague steps lead to errors. |
    | **Effective** | It must be possible to execute the steps and arrive at the correct output. | The steps must be logically sound and feasible. |
    | **Finite** | The algorithm must stop after a limited number of steps. | It prevents infinite loops or processes that never finish. |

    ## 1.2 Structure: Loops and Conditionals

    Algorithms often involve more than simple sequential steps; they use control structures to manage complexity:

    - **Loops (Repetition):** Steps that are repeated until a condition is met (e.g., "Keep mixing until the dough is smooth").
    - **Conditionals (Selection):** Steps that are performed only if a certain condition is true (e.g., "If the oven is hot, then put the cake in").

??? example "2. Real-World Applications"

    Algorithms are everywhere, even in non-computer processes.

    ### 2.1: Conceptual Algorithm (Everyday Life)

    | Context | Algorithm Description | Explanation |
    | :--- | :--- | :--- |
    | **Baking a Cake** | The algorithm is the **recipe**. It lists ingredients (Input), specifies steps (Process), and results in the cake (Output). | This shows an algorithm is a logical plan for solving a task. |
    | **Finding the Median** | 1. Sort the numbers. 2. Find the middle element. 3. If two middle elements, average them. | A clear, mathematical sequence that always yields the correct result. |

    ### 2.2: The Phone Call Process (Illustrating Conditionals & Loops)

    This algorithm outlines the precise steps for making a phone call, incorporating decision-making (**Conditionals**) and redialing (**Loop**).

    **Input:** The phone number of the person you want to contact.  
    **Output:** Successful connection and communication.

    1.  Start: Pick up the phone and prepare to dial.
    2.  Condition (Check Validity): Check if the number is valid and properly formatted. **IF INVALID, go to step 9.** **IF VALID, go to step 3.**
    3.  Action: Dial the number.
    4.  Condition (Answer): Is the call answered? **IF YES, go to step 6.** **IF NO, go to step 5.**
    5.  Action (Wait/Loop): Wait 10 seconds, then **RETURN to step 3** (Redial the number).
    6.  Action (Communication): Communicate with the other party.
    7.  Action: End the call.
    8.  Stop.
    9.  Action (Error): Display the message 'Call Failed' or 'Number Error' and **Stop.**

    This flowchart visually represents the logic of the algorithm above, showing how decisions (diamonds) guide the flow and how the loop returns to the 'Dial' step until an answer is received.

    ```mermaid
    flowchart TD
        Start([Start]) --> T1{Is the Number Valid?}
        T1 --> T2[Dial the Number]
        T1 --> T_E[Display Error]
        T_E --> End([End])
        T2 --> T3{Is There an Answer?}
        T3 --> T4[Communicate]
        T3 --> T6[Wait 10 Seconds]
        T4 --> T5[End Call]
        T5 --> End
        T6 --> T2
    ```

??? question "3. Short Practice Exercises"

    ### 3.1: Identifying Components

    You are writing an algorithm to calculate a student's final grade.
    What are the necessary **Input**, **Process**, and **Output**?

    ??? note "Show solution"
        - **Input:** Scores for tests, quizzes, and homework assignments.
        - **Process:** Applying the grading formula (e.g., weighted average) to the scores.
        - **Output:** The student's final calculated grade (e.g., a percentage or letter grade).

    ### 3.2: Defining Steps

    Write a simple, sequential algorithm to change the light bulb in a desk lamp.

    ??? note "Show solution"
        1. Turn off the lamp switch.
        2. Unplug the lamp from the wall.
        3. Unscrew the old bulb.
        4. Screw in the new bulb.
        5. Plug the lamp back into the wall.
        6. Turn on the lamp switch.

    ### 3.3: Recognizing Conditions

    Identify the loop condition in this algorithm: *Walk down the hallway, checking each door until you find the meeting room.*

    ??? note "Show solution"
        - **The Loop:** Checking each door.
        - **The Condition:** "until you find the meeting room." (This is the stopping condition).

??? question "4. Mini-Quiz"

    ### Q1. Which of the following best defines an algorithm?

    A) A precise, step-by-step set of instructions to solve a problem  
    B) A random set of ideas that may solve a task  
    C) A collection of examples without a clear order  
    D) A computer program written in a specific language  

    ??? info "Show answer"
        **A) A precise, step-by-step set of instructions to solve a problem**

    ### Q2. Which property ensures an algorithm will eventually stop?

    A) Precise  
    B) Effective  
    C) Finite  
    D) Input  

    ??? info "Show answer"
        **C) Finite**

    ### Q3. What is the difference between an algorithm and a program?

    A) An algorithm is the precise plan written in common language; a program is that plan implemented in code (e.g., Python)  
    B) An algorithm is its implementation in code, while a program is only the planning phase  
    C) An algorithm is limited to using loops; a program is limited to using conditionals  
    D) An algorithm is always more complex than a program, regardless of the task  

    ??? info "Show answer"
        **A) An algorithm is the precise plan written in common language; a program is that plan implemented in code (e.g., Python).**

    ### Q4. When using an algorithm to solve a complex mathematical calculation, the formula used represents which concept?

    A) The Input  
    B) The Output  
    C) The Process  
    D) The condition  

    ??? info "Show answer"
        **C) The Process**

    ### Q5. What is the consequence of an algorithm lacking a "Finite" property?

    A) The output will be incorrect.  
    B) The algorithm will be too slow.  
    C) It could result in an infinite loop when programmed.  
    D) It cannot handle loops or conditionals.  

    ??? info "Show answer"
        **C) It could result in an infinite loop when programmed.**

??? warning "5. Common Mistakes"

    - Lack of precision: using vague language (like "mix ingredients well") instead of detailed, unambiguous steps that a computer can follow.  
    - Confusing algorithm with program: mistaking the high-level, language-independent planning phase (algorithm) with the language-specific implementation phase (program code).  
    - Missing input/output: failing to clearly define what data is needed (Input) and what the intended result should be (Output).  
    - Non-finite algorithms: creating a set of steps that lacks a clear stopping condition, potentially leading to an infinite loop in code.  
    - Skipping order: not numbering the instructions clearly, which makes it hard to identify the flow or refer back to steps for repetition or conditionals.  

??? note "6. Summary Mindmap"

    ```mermaid
    mindmap
      root((Algorithm))
        Input
          Data
          Resources
        Process
          Sequence of Steps
          Transforms Input to Output
          Must be:
            Precise
            Effective
            Finite
        Output
          Expected Result
          Goal
    ```

??? tip "7. Optional Extensions"

    - Design a flowchart for a daily task (e.g., brewing coffee).
    - Write an algorithm for checking if a number is prime.
    - Research and document the differences between flowcharts and pseudocode.