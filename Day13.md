# Day 13 - if-else (The Inspector Makes Choices)

## What I Learned

A condition helps a program make decisions.

Sometimes there are two possible actions.

The "if-else" statement allows a program to choose between two different actions based on a condition.

---

## Real Life Example: Searching a Book

Suppose I am searching a book for the word "Python".

The book contains multiple pages.

## The Inspector asks:

«Does this page contain the word "Python"?»

There are two possible outcomes.

If YES

- Mark the page.

If NO

- Ignore the page and continue searching.

---

## The Inspector's Decision

Contains "Python"?
        │
    ┌───┴───┐
   Yes      No
    │        │
Mark Page  Ignore Page

---

## Python Idea

contains_python = True

if contains_python:
    print("Mark this page")
else:
    print("Ignore this page")

---

## Understanding if-else

if

Runs when the condition is True.

if contains_python:
    print("Mark this page")

Meaning:

«If the page contains the word "Python", perform the action.»

---

else

Runs when the condition is False.

else:
    print("Ignore this page")

Meaning:

«If the page does not contain the word "Python", perform a different action.»

---

Loop Team + Inspector

Imagine my book-search team.

Worker 1 - Traversal

Visits pages one by one.

Page 1 → Page 2 → Page 3 → Page 4

---

Worker 2 - Processing

Reads the current page and gathers information.

For example:

«Read the page and look for the word "Python".»

---

Inspector - Decision Maker

Checks the condition.

Question:

«Does this page contain the word "Python"?»

If YES:

- Mark the page.

If NO:

- Ignore the page.

---

Worker 3 - Automatic Repetition

Repeats the same process for all pages until no pages remain.

Traverse
↓
Process
↓
Decide
↓
Repeat

---

## Cheap Checks and Expensive Checks

I learned that not all conditions are the same.

Cheap Checks

Quick to evaluate.

Examples:

- Is the page blank?
- Does the page contain any text?

Page
 ↓
Quick Check
 ↓
Decision

---

## Expensive Checks

Require processing before a decision can be made.

Example:

«Does the page contain the word "Python"?»

To answer this question, the page must first be read.

Page
 ↓
Read Content
 ↓
Check for Python
 ↓
Decision

Here, processing and condition checking work together.

---

## Important Concept

- List = Book
- Items = Pages
- Worker 1 = Traversal
- Worker 2 = Processing
- Inspector = Condition / Decision Maker
- Worker 3 = Automatic Repetition
- if = Action when condition is True
- else = Action when condition is False

---

## Key Understanding

A loop automates repetitive work.

Inside the loop:

1. Worker 1 traverses pages.
2. Worker 2 performs processing.
3. The Inspector checks conditions.
4. A decision is made.
5. Worker 3 repeats the process automatically.

The Inspector can choose between two actions:

Condition True  → Action A
Condition False → Action B

This makes programs intelligent because they can respond differently to different situations.

---

## My Thought

Now I understand that "if-else" allows a program to make decisions. I imagine an Inspector working with the loop team. The Inspector evaluates a condition and chooses between two possible actions. Sometimes the Inspector can make a quick decision, while other times processing is needed before the decision can be made. Together, traversal, processing, decision-making, and repetition help a program solve problems automatically.
