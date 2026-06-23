# Day 6 - Loops (Repetition and Automation)

## What Did I Learn Today?

On Day 5, I learned that programs can make decisions using conditions.

Today I learned that programs can repeat actions automatically.

Many real-world activities involve repetition.

Instead of writing the same instruction again and again, programmers use **loops**.

A loop tells the computer:

> Repeat this task multiple times.

---

## What Is a Loop?

A loop is a way to repeat a set of instructions.

Instead of writing the same code many times, we write it once and let the computer repeat it.

---

## Real-Life Example: Brushing Teeth

We do not brush our teeth only once.

We repeat it every day.

### Thinking Like a Loop

```text
Day 1 → Brush Teeth
Day 2 → Brush Teeth
Day 3 → Brush Teeth
Day 4 → Brush Teeth
...
```

This repetitive action can be viewed as a loop.

---

## Real-Life Example: Walking

Walking is also repetitive.

```text
Take a step
Take a step
Take a step
Take a step
...
```

The same action is repeated until we reach our destination.

---

## Real-Life Example: Daily Routine

Many daily activities follow a repeating pattern.

```text
Wake Up
Brush Teeth
Eat Breakfast
Go to Work
Sleep

Repeat Next Day
```

This cycle continues repeatedly.

---

## Why Do We Need Loops?

Without loops:

```python
print("Brush Teeth")
print("Brush Teeth")
print("Brush Teeth")
print("Brush Teeth")
print("Brush Teeth")
```

This works, but it is repetitive.

With loops:

```python
for day in range(5):
    print("Brush Teeth")
```

The computer repeats the instruction automatically.

---

## Loops in Python

Python uses loops to repeat actions.

Example:

```python
for day in range(7):
    print("Brush Teeth")
```

### Output

```text
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
```

The instruction runs seven times.

---

## Understanding range()

```python
range(7)
```

Means:

```text
0, 1, 2, 3, 4, 5, 6
```

A total of seven repetitions.

The loop repeats once for each value.

---

## Tea Shop Example

Suppose a tea shop receives five tea orders.

Without a loop:

```python
print("Prepare Tea")
print("Prepare Tea")
print("Prepare Tea")
print("Prepare Tea")
print("Prepare Tea")
```

With a loop:

```python
for order in range(5):
    print("Prepare Tea")
```

The output remains the same, but the code becomes shorter and easier to manage.

---

## Combining Loops and Variables

Loops can work with variables.

Example:

```python
for number in range(5):
    print(number)
```

Output:

```text
0
1
2
3
4
```

The variable `number` changes automatically during each repetition.

---

## Combining Loops and Decision Making

Loops can also work with conditions.

Example:

```python
for number in range(5):

    if number == 3:
        print("Special Number")

    else:
        print(number)
```

Output:

```text
0
1
2
Special Number
4
```

Now the program is repeating actions and making decisions.

---

## Repetition Flow

A common programming pattern is:

```text
Start
  ↓
Repeat Action
  ↓
Repeat Again
  ↓
Repeat Again
  ↓
Stop When Finished
```

This is the basic idea behind loops.

---

## Why Is This Important?

Computers are very good at repetitive tasks.

Humans become tired of repeating the same work.

Computers can repeat tasks thousands or millions of times without getting tired.

Examples:

- Sending notifications
- Processing student records
- Printing reports
- Checking passwords
- Analyzing data

Loops make these tasks possible.

---

## Connecting Day 1 to Day 6

### Day 1

Instructions tell the computer what to do.

```text
Follow steps
```

### Day 2

Variables store information.

```python
name = "Lakshaga"
```

### Day 3

Variables process information.

```python
total = a + b
```

### Day 4

Programs interact with users.

```python
name = input("Enter your name: ")
```

### Day 5

Programs make decisions.

```python
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

### Day 6

Programs repeat actions automatically.

```python
for day in range(7):
    print("Brush Teeth")
```

Now programming is not only storing, processing, communicating, and deciding.

It is also automating repetitive work.

---

## My Thought

Today I learned that loops help computers perform repetitive tasks automatically.

Instead of writing the same instruction many times, we can write it once and let the computer repeat it.

This makes programs shorter, cleaner, and more efficient.

Computers can repeat tasks without getting tired, making automation possible.

---

## What I Learned Today

- Loops help repeat actions automatically.
- Repetition is common in real life.
- Python uses loops to automate repetitive tasks.
- `for` loops repeat actions a specific number of times.
- Loops reduce repetitive code.
- Loops can work together with variables and conditions.

### Programming Rule #6

**Repeat → Automate → Save Effort**

Loops allow computers to perform repetitive tasks efficiently and automatically.
