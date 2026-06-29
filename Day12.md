# Day 12 - Conditions (The Inspector)

## What I Learned

A condition helps a program make decisions.

Without conditions, a program treats every item the same way.

With conditions, a program can decide whether to process an item, skip it, or perform a different action.

---

## Real Life Example: Searching a Book

Imagine I am searching a book for the word **"Python"**.

The book contains many pages:

- Page 1
- Page 2
- Page 3
- Page 4

My goal is not to process every page equally.

I only care about pages that contain the word **"Python"**.

---

## The Inspector

In my mental model, I add an **Inspector** to the loop team.

The Inspector's job is to make decisions.

The Inspector asks:

**"Does this page contain the word Python?"**

---

## How the Team Works

### Worker 1 – Traversal

Visits pages one by one.

```text
Page 1 → Page 2 → Page 3 → Page 4
```

---

### Worker 2 – Processing

Reads the current page.

---

### Inspector – Condition

Checks:

**"Does this page contain the word Python?"**

If YES:

- Mark the page.
- Continue processing.

If NO:

- Skip the page.

---

### Worker 3 – Automatic Repetition

Repeats the process for all remaining pages.

---

## Python Idea

```python
page_contains_python = True

if page_contains_python:
    print("Mark this page")
```

---

## Understanding `if`

The word **if** means:

> **"Only do this action when the condition is True."**

Example:

```python
if page_contains_python:
    print("Mark this page")
```

Meaning:

- If the page contains "Python" → Mark it.
- Otherwise → Do nothing.

---

## Boolean Values (The Inspector's Language)

Every condition eventually becomes one of two values:

- `True`
- `False`

Example:

```python
page_contains_python = True

if page_contains_python:
    print("Mark this page")
```

Thinking:

```text
Condition
    ↓
True or False
```

The Inspector understands only these two answers.

```text
YES → True

NO → False
```

Every decision in programming is based on True or False.

---

## Cheap Checks

Some conditions are quick to evaluate.

Examples:

- Is the page blank?
- Does the page contain any text?

Thinking:

```text
Page
 ↓
Quick Check
 ↓
Decision
```

---

## Expensive Checks

Some conditions require processing before making a decision.

Example:

"Does the page contain the word Python?"

The page must first be read.

```text
Page
 ↓
Read Content
 ↓
Check for Python
 ↓
Decision
```

Sometimes processing comes before the decision.

---

## Comparison Operators

The Inspector compares values using comparison operators.

```python
==
!=
>
<
>=
<=
```

Examples:

```python
age == 18
age != 18
age > 18
age < 18
age >= 18
age <= 18
```

Thinking:

```text
Compare
   ↓
True or False
```

---

## Assignment (`=`) vs Comparison (`==`)

Many beginners confuse these.

### Assignment (`=`)

```python
age = 18
```

Meaning:

```text
Store 18 inside age.
```

### Comparison (`==`)

```python
age == 18
```

Meaning:

```text
Check whether age equals 18.
```

Remember:

```text
=   → Store

==  → Compare
```

---

## IF / ELSE

Sometimes the Inspector must choose between two actions.

```python
marks = 80

if marks >= 50:
    print("Pass")
else:
    print("Fail")
```

Thinking:

```text
Marks >= 50?
      ↓
 YES      NO
 ↓         ↓
Pass     Fail
```

---

## IF / ELIF / ELSE

Sometimes there are multiple possibilities.

```python
marks = 85

if marks >= 90:
    print("Grade A")

elif marks >= 75:
    print("Grade B")

else:
    print("Grade C")
```

The Inspector checks each condition until one becomes True.

---

## Multiple Conditions (AND)

Sometimes one condition is not enough.

```python
age = 25
has_ticket = True

if age >= 18 and has_ticket:
    print("Allow Entry")
```

Thinking:

```text
Age Check
    AND
Ticket Check
```

Both must be True.

---

## OR Condition

```python
is_admin = False
is_manager = True

if is_admin or is_manager:
    print("Access Granted")
```

Only one condition needs to be True.

---

## NOT Condition

```python
logged_in = False

if not logged_in:
    print("Login Required")
```

NOT reverses the result.

```text
True → False

False → True
```

---

## Conditions Inside Loops

Conditions become even more useful inside loops.

```python
marks = [35, 80, 45, 90]

for mark in marks:

    if mark >= 50:
        print(mark)
```

Thinking:

```text
Traversal
    ↓
Inspector
    ↓
Pass?
    ↓
Process
```

Without the Inspector:

```text
All marks are processed.
```

With the Inspector:

```text
Only matching marks are processed.
```

---

## Filtering

Example:

```python
numbers = [1,2,3,4,5,6]

for number in numbers:

    if number % 2 == 0:
        print(number)
```

Output:

```text
2
4
6
```

Thinking:

```text
Traverse
    ↓
Inspect
    ↓
Keep?
    ↓
Process
```

Filtering means selecting only the required items.

---

## Searching

Example:

```python
books = ["Java", "Python", "C++"]

for book in books:

    if book == "Python":
        print("Found")
```

Thinking:

```text
Traverse
    ↓
Inspect
    ↓
Match?
    ↓
Found
```

---

## Nested Conditions

Sometimes one decision depends on another.

```python
marks = 85

if marks >= 50:

    if marks >= 75:
        print("Distinction")

    else:
        print("Pass")
```

Thinking:

```text
Pass?
 ↓
Yes
 ↓
Distinction?
 ↓
Yes
```

This is called a nested condition.

---

## Controlling the Loop

The Inspector can also control the loop itself.

### continue — Skip Current Item

```python
numbers = [1, 2, -1, 4]

for num in numbers:

    if num < 0:
        continue

    print(num)
```

Output:

```text
1
2
4
```

What happened?

- 1 → Condition False → Print
- 2 → Condition False → Print
- -1 → Condition True → Skip this item
- 4 → Continue processing

`continue` skips only the current item.

---

### break — Stop the Loop

```python
numbers = [1, 2, -1, 4]

for num in numbers:

    if num < 0:
        break

    print(num)
```

Output:

```text
1
2
```

What happened?

- 1 → Print
- 2 → Print
- -1 → Stop loop
- 4 is never visited.

`break` stops the entire loop immediately.

---

## When Should I Use Them?

### Use `if`

When you only need to make a decision.

Examples:

- Pass or Fail
- Even or Odd
- Allow or Deny

---

### Use `continue`

When you want to skip the current item but continue processing the remaining items.

Examples:

- Skip blank pages.
- Ignore invalid records.
- Skip negative numbers.

---

### Use `break`

When the task is complete and continuing is unnecessary.

Examples:

- Search completed.
- Correct password found.
- Product found.
- Three wrong login attempts.

---

## Enhanced Worker Model

```text
Worker 1 = Traversal

Worker 2 = Processing

Worker 3 = Repetition

Inspector = Decision Maker
```

The Inspector can:

- Allow
- Deny
- Skip
- Search
- Filter
- Select
- Classify
- Route
- Stop
- Continue

---

## Real-World Examples

### ATM

Correct PIN?

↓

Allow Access

---

### Phone Unlock

Fingerprint Match?

↓

Unlock Phone

---

### Shopping Website

Price < Budget?

↓

Show Product

---

### Search Engine

Keyword Match?

↓

Display Result

---

### University

Marks ≥ Pass Mark?

↓

Pass Student

---

## Day 12 Insight

Conditions make programs intelligent.

Without conditions, every item is treated the same.

With conditions, programs can:

- Allow
- Reject
- Search
- Filter
- Select
- Skip
- Classify

The Inspector does not perform the work.

The Inspector decides whether the work should happen.

---

## My Thought

Today I learned that conditions are like an Inspector inside a program.

The Inspector decides what should happen next based on True or False.

Sometimes it allows processing.

Sometimes it skips processing.

Sometimes it stops processing completely.

By combining conditions with loops, programs become capable of making intelligent decisions instead of performing the same action for every item.

---

## Day 12 Completion Checklist

✅ if

✅ if-else

✅ if-elif-else

✅ Comparison Operators

✅ Assignment (`=`) vs Comparison (`==`)

✅ Boolean Values (True / False)

✅ AND

✅ OR

✅ NOT

✅ Conditions Inside Loops

✅ Searching

✅ Filtering

✅ Nested Conditions

✅ continue

✅ break

✅ Real-World Decision Systems

---

### Programming Rule #12

```text
Traverse → Inspect → Decide → Process → Repeat
```

The Inspector is the decision-making system of a program. It decides **what should happen next** before the program performs its work.
