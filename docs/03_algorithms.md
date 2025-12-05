---
hide:
  - toc
---

# 3. Algorithms

An **Algorithm** is a precise, step-by-step set of instructions designed to solve a specific task. This process represents the core planning phase of computational thinking, known as **Algorithmic Design**, which is completed before any code is written.

Think of an **algorithm** as a meticulously organized blueprint: it defines the exact, ordered steps required to transform the initial **Input** into the final **Output** before any programming begins.

??? info "1. Components and Properties"

    ### 1.1. Properties: Essential Characteristics

    A valid and effective algorithm operates on the fundamental **Input-Process-Output (IPO)** model. The **Process** (the algorithm itself) must meet these five essential properties to be valid and effective:

    | Property | Description | Why it matters |
    | :--- | :--- | :--- |
    | **Input** | The initial data or materials required to start the process. | An algorithm cannot run without clearly defined resources. |
    | **Output** | The specific, expected result or product of the algorithm. | If the goal is not defined, the algorithm is useless. |
    | **Precise** | Every step must be clearly specified, unambiguous, and executable. | Computers require exact instructions; vague steps lead to errors. |
    | **Effective** | It must be possible to execute the steps and arrive at the correct output. | The steps must be logically sound and feasible. |
    | **Finite** | The algorithm must stop after a limited number of steps. | It prevents infinite loops or processes that never finish. |

    ### 1.2. Structure: Conditionals and Loops

    Algorithms often involve more than simple sequential steps; they use control structures to manage complexity:

    - **Conditionals** (Selection): Steps that are performed only if a certain condition is true (e.g., "If the oven is hot, then put the cake in").
    - **Loops** (Repetition): Steps that are repeated until a condition is met (e.g., "Keep mixing until the dough is smooth").

??? example "2. Commented Examples"

    ### 2.1. Everyday Life Algorithms

    | Context | Algorithm Description | Explanation |
    | :--- | :--- | :--- |
    | **Baking a Cake** | List ingredients (Input), follow recipe steps (Process), obtain cake (Output). | The recipe acts as an algorithm: a clear plan that transforms raw materials into the final product. |
    | **Finding the Median** | 1. Sort the numbers. 2. Identify the middle element. 3. If two middle elements, average them. | A precise mathematical sequence that always produces the correct median value. |

    ### 2.2. The Phone Call Process

    This algorithm outlines the precise steps for making a phone call, incorporating decision-making (Conditionals) and redialing (Loop).

    - Input: The phone number of the person you want to contact.  
    - Output: Successful connection and communication.
    
    <div></div>

    1. Start: Pick up the phone and prepare to dial.
    2. Condition (Check Validity): Check if the number is valid and properly formatted. IF INVALID, go to step 8. IF VALID, go to step 3.
    3. Process: Dial the number.
    4. Condition (Answer): Is the call answered? IF YES, go to step 6. IF NO, go to step 5.
    5. Process (Wait/Loop): Wait 10 seconds, then RETURN to step 3 (Redial the number).
    6. Process (Communication): Communicate with the other party.
    7. Process: End the call. Go to 9.
    8. Action (Error): Display the message 'Call Failed' or 'Number Error'. Go to 9.
    9. End.

    This flowchart visually represents the logic of the algorithm above, showing how decisions (diamonds) guide the flow and how the loop returns to the 'Dial' step until an answer is received.

    <div style="width: 55%;">
    ```mermaid
    flowchart TD
    Start([1. Start]) --> T1{2. Is the Number Valid?}
    T1 -- No --> T_E[8. Action: Display Error]
    T1 -- Yes --> T2[3. Dial the Number]
    T_E --> End([9. End])
    T2 --> T3{4. Is There an Answer?}
    T3 -- No --> T6[5. Wait 10 Seconds]
    T3 -- Yes --> T4[6. Communicate]
    T4 --> T5[7. End Call]
    T5 --> End
    T6 --> T2 
    
    classDef Loop fill:#ff0,stroke:#333,stroke-width:2px;
    class T6 Loop
    ```
    </div>

??? question "3. Short Practice Exercises"

    ### 3.1. Identifying Components

    You are writing an algorithm to calculate your final grade. What are the necessary Input, Process, and Output?

    ??? note "Show solution"
        - Input: Scores for tests, quizzes, and homework assignments.
        - Process: Applying the grading formula (e.g., weighted average) to the scores.
        - Output: Your final calculated grade (e.g., a percentage or letter grade).

    ### 3.2. Defining Steps

    Write a simple, sequential algorithm to change the light bulb in a desk lamp.

    ??? note "Show solution"
        1. Turn off the lamp switch.
        2. Unplug the lamp from the wall.
        3. Unscrew the old bulb.
        4. Screw in the new bulb.
        5. Plug the lamp back into the wall.
        6. Turn on the lamp switch.

    ### 3.3. Recognizing Conditions

    Identify the loop and its stopping condition in this algorithm: "Walk down the hallway, checking each door until you find the meeting room".

    ??? note "Show solution"
        - The Loop: Checking each door.
        - The Condition: "until you find the meeting room." (This is the stopping condition).

    ### 3.4. Identifying a Missing Step

    The following algorithm is intended to send a message via email, but step 3 is missing in the process. What should be added?

    1. Open email client
    2. Compose new message
    3. 
    4. Send message

    ??? note "Show solution"
        Specify the recipient (e.g., "Enter recipient email address").

??? question "4. Mini-Quiz"

    ### 4.1. Which of the following best defines an algorithm?

    A) A precise, step-by-step set of instructions to solve a problem.<br>
    B) A random set of ideas that may solve a task.<br>
    C) A collection of examples without a clear order.<br>
    D) A computer program written in a specific language.

    ??? info "Show answer"
        A) A precise, step-by-step set of instructions to solve a problem.

    ### 4.2. Which property ensures an algorithm will eventually stop?

    A) Precise<br>
    B) Effective<br>
    C) Finite<br>
    D) Input

    ??? info "Show answer"
        C) Finite

    ### 4.3. What is the difference between an algorithm and a program?

    A) An algorithm is the precise plan written in common language; a program is that plan implemented in code (e.g., Python).<br>
    B) An algorithm is its implementation in code, while a program is only the planning phase.<br>
    C) An algorithm is limited to using loops; a program is limited to using conditionals.<br>
    D) An algorithm is always more complex than a program, regardless of the task.

    ??? info "Show answer"
        A) An algorithm is the precise plan written in common language; a program is that plan implemented in code (e.g., Python).

    ### 4.4. When using an algorithm to solve a complex mathematical calculation, the formula used represents which concept?

    A) The Input<br>
    B) The Output<br>
    C) The Process<br>
    D) The condition

    ??? info "Show answer"
        C) The Process

    ### 4.5. What is the consequence of an algorithm lacking a "Finite" property?

    A) The output will be incorrect.<br>
    B) The algorithm will be too slow.<br>
    C) It could result in an infinite loop when programmed.<br>
    D) It cannot handle loops or conditionals.

    ??? info "Show answer"
        C) It could result in an infinite loop when programmed.

??? warning "5. Common Mistakes"

    - Using vague or imprecise instructions.
    - Confusing an algorithm with a program.
    - Leaving out the required Input or expected Output.
    - Not numbering the steps in a clear, logical order.

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