---
hide:
  - toc
---

# 1. Computational Thinking

Computational Thinking is a disciplined way of approaching problems so they can be solved efficiently, systematically, and with clarity. It relies on four essential principles or pillars:

- **Decomposition**
- **Pattern Recognition**
- **Abstraction**
- **Algorithmic Design**

These skills support problem-solving in programming, mathematics, engineering, and everyday situations.

??? info "1. The Four Pillars"
    ## 1.1 Decomposition
    Breaking a complex problem into smaller, more manageable parts.

    ```mermaid
    flowchart TD
        A[Complex Problem] --> B[Part 1]
        A --> C[Part 2]
        A --> D[Part 3]
        A --> E[Part 4]
    ```

    ## 1.2 Pattern Recognition
    Finding similarities, repetitions, or trends among the smaller parts.

    ```mermaid
    flowchart LR
        A((Input 1)) --> X[Pattern]
        B((Input 2)) --> X
        C((Input 3)) --> X
        X --> D((General Rule))
    ```

    ## 1.3 Abstraction
    Removing unnecessary details to focus only on what matters.

    ```mermaid
    flowchart LR
        A[All Details] -->|Remove Clutter| B[Essential Ideas]
    ```

    ## 1.4 Algorithmic Design  
    Creating a precise, step-by-step process to solve a problem.

    ```mermaid
    flowchart TD
        Start([Start]) --> S1[Step 1]
        S1 --> S2[Step 2]
        S2 --> S3[Step 3]
        S3 --> End([End])
    ```

??? example "2. Commented Examples"
    ## 2.1: Decomposition + Pattern Recognition

    **Problem:** Find the sum of all numbers from 1 to 200.

    **Decomposition:** Pair numbers from opposite ends:  
    1 + 200  
    2 + 199  
    3 + 198  
    …

    **Pattern Recognition:** Each pair sums to **201**.

    **Algorithmic Design:**
    1. Create number pairs.  
    2. Count the number of pairs (200 ÷ 2 = 100).  
    3. Multiply: **201 × 100 = 20,100**

    ## 2.2: Abstraction

    A bus route planner ignores irrelevant details such as:

    - building colors  
    - parked cars  
    - tiny alleyways  

    Planners keep only:

    - main streets  
    - stops  
    - distances  
    - times  

??? question "3. Short Practice Exercises"
    ### 3.1: Decomposition  
    List four smaller tasks needed to organize a school Science Fair.

    ??? note "Show solution"
        - Reserve the venue  
        - Assign booths  
        - Prepare schedule and logistics  
        - Create judges’ materials  

    ### 3.2: Pattern Recognition  
    Identify the pattern in: 10, 20, 30, 40, 50…

    ??? note "Show solution"
        This is an arithmetic sequence increasing by **10**.  

    ### 3.3: Abstraction  
    A programmer builds a BMI calculator.  
    Which details matter? Which do not?

    ??? note "Show solution"
        **Essential:** weight, height  
        **Not essential:** hair color, music preference, phone number  

    ### 3.4: Algorithmic Design  
    Write an algorithm for checking out a book from a library.

    ??? note "Show solution"
        1. Start  
        2. Pick a book  
        3. Go to librarian  
        4. Scan book  
        5. Scan library card  
        6. Confirm checkout  
        7. End  

??? question "4. Mini-Quiz"
    ### Q1. Which of the following best defines computational thinking?

    A) A method for memorizing programming syntax  
    B) A technique for translating code into natural language  
    C) A set of methods for expressing problems and their solutions  
    D) A way to optimize hardware performance  

    ??? info "Show answer"
        **C) A set of methods for expressing problems and their solutions**


    ### Q2. Breaking a complex challenge into smaller parts refers to:

    A) Abstraction  
    B) Decomposition  
    C) Pattern Recognition  
    D) Algorithmic Design  

    ??? info "Show answer"
        **B) Decomposition**

    ### Q3. Showing only the Sun and planets to explain orbits is an example of:

    A) Decomposition  
    B) Debugging  
    C) Algorithmic Design  
    D) Abstraction  

    ??? info "Show answer"
        **D) Abstraction**

    ### Q4. An algorithm is:

    A) A list of random examples  
    B) A precise, step-by-step procedure  
    C) A collection of ideas  
    D) Code written in Python  

    ??? info "Show answer"
        **B) A precise, step-by-step procedure**

    ### Q5. Finding similarities among sub-problems refers to:

    A) Decomposition  
    B) Abstraction  
    C) Pattern Recognition  
    D) Debugging  

    ??? info "Show answer"
        **C) Pattern Recognition**

??? warning "5. Common Mistakes"
    - Confusing **algorithm** with **program**  
    - Using vague steps (“do it”, “fix it”)  
    - Mixing **Decomposition** (break apart) with **Abstraction** (filter out details)  
    - Keeping irrelevant details  

??? note "6. Summary Mindmap"
    ```mermaid
    mindmap
      root((Computational Thinking))
        Decomposition
          Break into parts
          Manage complexity
        Pattern Recognition
          Identify similarities
          Predict behavior
        Abstraction
          Remove noise
          Focus on essentials
        Algorithmic Design
          Step-by-step plan
          Precise instructions
    ```

??? tip "7. Optional Extensions"
    - Decompose a daily-life problem.  
    - Identify patterns in a sequence you choose (e.g., even numbers, repeating schedules).
    - Write an algorithm for a simple routine.  
    