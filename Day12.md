# Day 12 - Conditions (The Inspector)

## What I Learned

A condition helps a program make decisions.

Without conditions, a program treats every item the same way.

With conditions, a program can decide whether to process an item, skip it, or perform a different action.

---

## Real Life Example: Searching a Book

Imagine I am searching a book for the word "Python".

The book contains many pages:

- Page 1
- Page 2
- Page 3
- Page 4

My goal is not to process every page equally.

I only care about pages that contain the word "Python".

---

## The Inspector

In my mental model, I add an Inspector to the loop team.

The Inspector's job is to make decisions.

The Inspector asks:

«Does this page contain the word "Python"?»

---

## How the Team Works

Worker 1 - Traversal

Visits pages one by one.

Page 1 → Page 2 → Page 3 → Page 4

---

Worker 2 - Processing

Reads the current page.

---

Inspector - Condition

Checks:

«Does this page contain the word "Python"?»

If YES:

- Mark the page.
- Continue processing.

If NO:

- Skip the page.

---

Worker 3 - Automatic Repetition

Repeats the process for all remaining pages.

---

## Python Idea

```python
page_contains_python = True

if page_contains_python:
    print("Mark this page")
```
---

## Understanding if

The word "if" means:

«"Only do this action when the condition is true."»

Example:
```python
if page_contains_python:
    print("Mark this page")
```
Meaning:

- If the page contains "Python" → Mark it.
- Otherwise → Do nothing.

---

Cheap Checks

Some conditions are quick to evaluate.

Examples:

- Is the page blank?
- Does the page contain text?

These checks require very little work.

Page
 ↓
Quick Check
 ↓
Decision

---

Expensive Checks

Some conditions require processing before a decision can be made.

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

Here, processing helps the Inspector make a decision.

---

## Important Concept

- List = Book
- Items = Pages
- Worker 1 = Traversal
- Worker 2 = Processing
- Inspector = Condition / Decision Maker
- Worker 3 = Automatic Repetition

---

## Key Understanding

Conditions help programs make decisions.

The Inspector does not perform the work.

The Inspector decides whether the work should happen.

Sometimes the Inspector can decide immediately.

Sometimes the Inspector needs information from processing before making a decision.

---

## My Thought

Now I understand that conditions are like an Inspector inside a program. The Inspector checks whether a requirement is satisfied and decides what should happen next. Some decisions are quick, while others require information gathered during processing. Conditions help programs become intelligent instead of treating every item the same way.
