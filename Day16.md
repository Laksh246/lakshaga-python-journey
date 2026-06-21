# Day 16 - Functions Revisited (Reusable Machines)

## What I Learned

A function is a reusable block of code that performs a specific task.

Instead of writing the same instructions repeatedly, I can place them inside a function and call the function whenever needed.

A function is like a machine that accepts inputs, performs processing, and produces an output.

---

## Real Life Example: Coffee Machine

Imagine a coffee machine.

To make coffee, I do not manually control every internal step.

I simply provide inputs:

- Water
- Coffee powder
- Sugar

and press a button.

The machine automatically performs all the work and produces coffee.

---

## Understanding the Coffee Machine

### Inputs

Things given to the machine.

```text
Water
Coffee Powder
Sugar
```

---

### Processing

Work performed inside the machine.

```text
Mix
Heat
Filter
```

---

### Output

Final result produced.

```text
Coffee
```

---

## Function as a Machine

```text
Input
  ↓
Function
  ↓
Processing
  ↓
Output
```

---

## Python Idea

```python
def make_coffee():
    print("Coffee Ready")

make_coffee()
```

---

## What Happens Here?

Step 1:

Create a machine.

```python
def make_coffee():
```

Step 2:

Define what the machine should do.

```python
print("Coffee Ready")
```

Step 3:

Use the machine.

```python
make_coffee()
```

Output:

```text
Coffee Ready
```

---

## Function with Inputs

A machine becomes more useful when it accepts inputs.

Example:

```python
def make_coffee(name):
    print("Coffee for", name)

make_coffee("Lakshaga")
```

Output:

```text
Coffee for Lakshaga
```

---

## Understanding Parameters and Arguments

### Parameter

A placeholder inside the machine.

```python
def make_coffee(name):
```

Here:

```text
name
```

is a parameter.

It is an empty slot waiting for a value.

---

### Argument

The actual value supplied.

```python
make_coffee("Lakshaga")
```

Here:

```text
"Lakshaga"
```

is an argument.

---

## Coffee Machine Example

```text
Parameter = Cup Label

Argument = Lakshaga
```

The machine places the supplied value into the empty slot.

---

## Function + Loop + Condition

Functions can contain everything learned so far.

```python
def check_marks(mark):
    if mark >= 50:
        print("Pass")
    else:
        print("Fail")
```

This function contains:

- Processing
- Condition
- Decision Making

---

## Programming Team Model

### Input Supplier

Provides information.

---

### Worker 1 - Traversal

Visits items if needed.

---

### Worker 2 - Processing

Performs work.

---

### Gate(s)

Make decisions.

---

### Worker 3 - Automatic Repetition

Repeats work when loops are used.

---

### Function

Acts like a reusable machine that coordinates everything.

---

## Important Concept

Functions do not create new ideas.

They organize existing ideas.

Inside a function we can use:

- Variables
- Lists
- Loops
- Conditions
- Nested Conditions

Functions help package all these concepts into reusable blocks.

---

## Key Understanding

Before functions:

```text
Write instructions repeatedly
```

After functions:

```text
Create once
Reuse many times
```

---

## My Thought

Now I understand that a function is like a reusable machine. Inputs are supplied to the machine, processing happens inside, and an output is produced. Functions help organize code and avoid repeating the same instructions. They can contain variables, lists, loops, conditions, and decision gates, making them one of the most powerful tools in programming.
