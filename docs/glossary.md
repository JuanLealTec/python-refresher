title: Glossary
---

# Glossary

This reference resource is organized thematically to facilitate the review of core concepts covered in **Computational Thinking I** and the **Python Refresher** site.

??? info "Alphabetical Index"

    | A - C | D - N | O - W |
    | :--- | :--- | :--- |
    | **A** | **D** | **O** |
    | [Abstraction](#abstraction) | [Data](#data) | [Operator Precedence](#operator-precedence) |
    | [Algorithmic Design](#algorithmic-design) | [Data Types](#data-types) | [Output](#output) |
    | [Algorithm](#algorithm) | [Decomposition](#decomposition) | **P** |
    | [ALL_CAPS](#all_caps) | **F** | [Pattern Recognition](#pattern-recognition) |
    | [Arithmetic Operators](#arithmetic-operators) | [For Loop](#for-loop) | [Primitive data types](#primitive-data-types) |
    | [Assignment Operator](#assignment-operator) | [Floating-point (float)](#floating-point-float) | [Process](#process) |
    | **B** | **I** | **R** |
    | [Boolean (bool)](#boolean-bool) | [Indentation](#indentation) | [Relational Operators](#relational-operators) |
    | **C** | [Infinite Loop](#infinite-loop) | **S** |
    | [Camel Case](#camel-case) | [Input](#input) | [Snake Case](#snake-case) |
    | [Case-sensitive](#case-sensitive) | [Input-Process-Output (IPO) cycle](#input-process-output-ipo-cycle) | [String (str)](#string-str) |
    | [Code Block](#code-block) | [Integer (int)](#integer-int) | **T** |
    | [Comparison Operator](#comparison-operator) | [Iterable Sequence](#iterable-sequence) | [Type Casting](#type-casting) |
    | [Conditional Expression](#conditional-expression) | **L** | [Type Promotion](#type-promotion) |
    | [Conditional Statements](#conditional-statements) | [Loop](#loop) | [TypeError](#typeerror) |
    | [Condition](#condition) | **M** | **V** |
    | [Constant](#constant) | [Multiple Conditional Statements](#multiple-conditional-statements) | [Validating User Input](#validating-user-input) |
    | [Computational Thinking](#computational-thinking) | **N** | [Variable](#variable) |
    | | [Nested Conditional Statements](#nested-conditional-statements) | **W** |
    | | | [While Loop](#while-loop) |

## 1. Computational Thinking and Algorithms

### Computational Thinking
A systematic and disciplined approach to solving problems using methods that can be executed by a computer.

It relies on four main pillars: Decomposition, Pattern Recognition, Abstraction, and Algorithmic Design.

### Decomposition
The process of breaking a complex problem or system into smaller, more manageable sub-problems.

This is the essential first step to manage complexity. A good decomposition should result in sub-problems that can be analyzed and solved independently.

### Pattern Recognition
Identifying similarities, trends, or repetitions among small, decomposed parts of a problem.

Recognizing these common patterns is key to generalization. This allows the programmer to reuse solutions or predict behaviors within the problem set.

### Abstraction
Filtering out irrelevant details and focusing only on the essential information needed to solve a problem.

Abstraction reduces complexity by simplifying the model. It allows us to work with high-level concepts without needing to understand all the underlying low-level details.

### Algorithmic Design
Developing a precise, step-by-step procedure or plan to solve a problem or a sub-problem.

The resulting plan must be unambiguous (no room for interpretation) and finite (guaranteed to stop). This design phase precedes the writing of the actual program.

### Algorithm
A precise, step-by-step procedure designed to solve a specific problem.

All algorithms follow the Input-Process-Output (IPO) cycle. It is often confused with a program (the implementation of the algorithm).

### Input-Process-Output (IPO) cycle
The fundamental model for all algorithms, defining that a system must receive data, transform it, and deliver a result.

The blueprint for program structure.

### Data
A single piece of raw value, fact, or observation that has not been interpreted or processed within a given context.

It is the fundamental element (e.g., a number, a character, a boolean value) that serves as Input to an algorithm.

### Input
The data, raw materials, or signals that a system receives before beginning a process.

Examples: User-typed text, a sensor reading, or clicking a button.

### Process
The stage where the algorithm's calculation and logic are applied to transform the received Input.

This is where the work is done (e.g., applying a formula or running a search).

### Output
The final, useful result or information delivered by the system after the Process is complete.

Examples: Displayed text, a computed number, or a song playing.

---

## 2. Data, Variables, and Naming Conventions

### Variable
A named storage location in the computer's memory that holds a value and can change during program execution.

Created by assigning a value using the `=` operator (assignment).

### Constant
A named identifier for a value that is intended to remain unchanged throughout the program's execution.

Conventionally written in ALL\_CAPS in Python to indicate its fixed nature.

### Data Types
The classification used by programming languages to define the kind of value a variable stores.

Dictates which operations (math, logic, text) can be performed.

### Primitive data types
The basic, built-in types that serve as the fundamental building blocks of any program.

Includes Integer, Float, String, and Boolean.

### Integer (int)
Whole numbers (positive, negative, or zero) without a fractional part.

Used for counting, indices, and discrete values.

### Floating-point (float)
Numbers that contain a decimal point, allowing for fractional values.

Used for prices, measurements, and scientific calculations.

### String (str)
A sequence of characters used to store text.

Must be enclosed in single (`'`) or double (`"`) quotes.

### Boolean (bool)
A logical data type that can only hold one of two values: True or False.

Used for decision-making and flow control (Conditionals and Loops).

### Snake Case
A naming convention where words are separated by underscores (`_`) and usually written in lowercase (e.g., `total_cost`).

The recommended style for variable names in Python (PEP 8 standard).

### ALL\_CAPS
A naming convention where all letters are uppercase, and words are separated by underscores (e.g., `TAX_RATE`).

The universal convention used in Python to indicate a Constant (a value that should not change).

### Camel Case
A naming convention where the first letter of each word (except the first one) is capitalized (e.g., `totalCost`).

Common in other languages (e.g., JavaScript) but less common for Python variables.

### Case-sensitive
A property of a programming language where uppercase and lowercase letters are treated as distinct characters.

`Name`, `name`, and `NAME` are recognized as three different identifiers.

---

## 3. Operators and Expressions

### Arithmetic Operators
Symbols used to perform mathematical calculations with numeric values (integers and floats).

The foundation of most Process steps in an algorithm.

### Operator Precedence
The set of rules that dictates the order in which operators must be evaluated within a complex mathematical expression.

Parentheses have the highest precedence, followed by Exponentiation.

### Assignment Operator (=)
The symbol (`=`) used to store a value on the right into a Variable name on the left in the computer's memory.

It is crucial to distinguish it from the Comparison Operator (`==`), a common source of bugs for beginners.

### Comparison Operator (==)
The double-equals operator used specifically to check if two values are equal.

It is a common mistake to confuse it with the Assignment Operator (`=`), which is used to assign a value to a variable.

### Relational Operators
Special symbols that allow Python to compare values. The result of this comparison is always a Boolean value (True or False).

They are used within the conditions of conditional structures. Common examples include: `==` (equality), `!=` (inequality), `>` (greater than), and `<` (less than).

### Type Promotion
The automatic conversion of the result of an arithmetic expression to the wider data type to prevent loss of precision.

The fundamental rule is: If an `int` and a `float` are mixed in an operation, the result is always a `float`.

### Type Casting
The explicit process of converting a value from one data type to another.

Essential for performing math on string-based input (like `input()`).

### TypeError
An error raised when an operation is performed on incompatible data types.

Common example: Trying to combine a string and an `int` using the addition operator (`+`).

---

## 4. Control Structures: Conditionals (Selection)

### Conditional Statements
Control structures used in algorithms that perform steps only if a specific condition is true (also known as Selection). In Python, these structures (`if`, `else`, `elif`) enable a program to execute different blocks of code based on the evaluation of a condition.

They are essential for controlling the flow of execution by allowing the program to make decisions (e.g., "IF the input is X, THEN do Y").

### Indentation
The whitespace (typically 4 spaces) used to set apart blocks of code belonging to a structure, such as the code under an `if` or `else` statement.

It is a mandatory syntax requirement in Python. Incorrect indentation will cause the program to raise an `IndentationError`.

### Code Block
A sequence of one or more logical lines of code that are grouped together to be executed as a single unit.

In Python, Indentation (typically 4 spaces) es mandatory to define the code block of structures like `if`, `else`, or `while` loops.

### Nested Conditional Statements
Structures where one conditional statement (`if`, `elif`, or `else`) is placed entirely within the code block of another.

They create a hierarchy or dependency: the inner condition is only evaluated if the outer condition is True.

### Multiple Conditional Statements
Chained structures using `if`, one or more `elif`, and optionally `else` to handle multiple mutually exclusive cases (only one can be true).

Conditions are checked in sequence. As soon as the first True condition is found, its code block executes, and the rest of the chain is skipped.

### Conditional Expression
A compact syntax used to assign a value to a variable in a single line, based on a single condition. It is also known as the Ternary Operator.

Its syntax is: `value_if_true if condition else value_if_false`. It is used to simplify basic `if-else` structures whose only purpose is value assignment.

---

## 5. Control Structures: Loops (Repetition)

### Loop
Control structures used in algorithms where steps are repeated until a stopping condition is met (also known as Repetition).

Essential for tasks that involve repetition, such as iterating over a collection of data.

### Condition
A boolean expression (evaluating to True or False) that determines if the loop body should execute in the current iteration.

It is the decision-making expression that governs the control flow in loops and conditional statements, determining whether a specific block of code is executed or skipped.

### While Loop
A control flow statement that repeatedly executes a block of code as long as a given condition evaluates to True.

The core feature is its use when the number of iterations is unknown in advance.

### Infinite Loop
A loop that runs indefinitely because the condition that controls its execution never becomes False.

Must be actively prevented by ensuring a mechanism exists to change the loop condition.

### Validating User Input
The process of checking data provided by a user to ensure it meets the program's requirements (e.g., format, range, type).

Example: Repeating a prompt until the user enters a number within a specified range (e.g., age between 0 and 120).

### For Loop
A control flow statement that repeats a block of code for a defined number of times or for each item in a sequence.

The key feature is that the number of iterations is typically known in advance or determined by the length of an iterable sequence.

### Iterable Sequence
Any sequence of objects (such as a string, a list, or the output of the `range()` function) that the For Loop can process item by item.

The loop executes exactly once for every element present in this sequence.