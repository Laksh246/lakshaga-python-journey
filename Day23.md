# Day 23 - Functions + Search (Reusable Search Machines)

## What I Learned

Searching is useful.

But writing the same search code again and again is repetitive.

A function allows me to create a reusable search machine.

Instead of rewriting the search logic, I can create it once and use it many times.

---

## Learning Journey So Far

```text
Data
  ↓
Information
  ↓
Knowledge
```

And:

```text
Function
│
└── Reusable Machine

Loop
│
└── Traversal

Condition
│
└── Decision Making

Return
│
└── Sends Result Back

Search
│
└── Finds Matching Data
```

---

## Why Combine Functions and Search?

Suppose I have a library.

```text
Library
│
├── Python Basics
├── Data Science
└── AI Fundamentals
```

Today I search for:

```text
Python Basics
```

Tomorrow I search for:

```text
Data Science
```

The search process is the same.

Only the search value changes.

A function helps reuse the search process.

---

## Real Life Example: Librarian

Imagine a librarian.

People ask different questions.

```text
Find Python Basics

Find Data Science

Find AI Fundamentals
```

The librarian uses the same search process every time.

Only the requested title changes.

The librarian behaves like a reusable function.

---

## Python Idea

```python
def find_book(title):

    for book in library:

        if book["title"] == title:
            return book

    return "Book Not Found"
```

---

## Understanding the Function

### Parameter

```python
title
```

This is an empty slot.

The function does not know the title in advance.

---

### Argument

```python
find_book("Python Basics")
```

```text
Python Basics
```

is the actual value supplied.

---

### Return

If found:

```python
return book
```

The result is sent back.

---

## Complete Example

```python
library = [
    {"title": "Python Basics"},
    {"title": "Data Science"},
    {"title": "AI Fundamentals"}
]

def find_book(title):

    for book in library:

        if book["title"] == title:
            return book

    return "Book Not Found"

result = find_book("Data Science")

print(result)
```

---

## What Happens Internally?

### Input Supplier

Provides:

```text
Data Science
```

---

### Function Machine

Starts searching.

---

### Worker 1 - Traversal

Visits books.

```text
Book 1
 ↓
Book 2
 ↓
Book 3
```

---

### Worker 2 - Processing

Reads title.

---

### Gate

Checks:

```text
Title = Data Science ?
```

---

### Worker 3

Repeats search.

---

### Return Gate

Returns matching result.

---

## Search Flow

### Book 1

```text
Python Basics
```

Condition:

```text
Match?
```

Result:

```text
No
```

Continue.

---

### Book 2

```text
Data Science
```

Condition:

```text
Match?
```

Result:

```text
Yes
```

Return result.

Stop searching.

---

## Why Return is Useful

Without return:

```python
print("Book Found")
```

Only displays information.

---

With return:

```python
return book
```

The result can be:

```text
Stored

Reused

Processed Further
```

---

## Data → Information → Knowledge

### Data

```text
Library Records
```

---

### Information

Question:

```text
Find Data Science
```

Answer:

```text
Data Science Found
```

---

### Knowledge

Decision:

```text
Borrow Data Science
```

---

## Reusable Search Machine

The same function can answer many questions.

```python
find_book("Python Basics")

find_book("Data Science")

find_book("AI Fundamentals")
```

Only the argument changes.

The machine remains the same.

---

## Key Understanding

A search function combines:

```text
Function
 +
Loop
 +
Condition
 +
Return
 =
Reusable Search Machine
```

---

## Complete Mental Model

```text
Library Data
        │
        ▼

Function Machine
        │
        ▼

Worker 1
(Traversal)

        │
        ▼

Worker 2
(Processing)

        │
        ▼

Gate
(Condition Check)

        │
        ▼

Worker 3
(Automatic Repetition)

        │
        ▼

Return
(Result)

        │
        ▼

Information

        │
        ▼

Knowledge
```

---

## 💭 My Thought

Now I understand that a function can be used as a reusable search machine. The function accepts a search value as input, Worker 1 traverses the records, Worker 2 processes the data, the Gate checks for a match, Worker 3 repeats the search automatically, and the Return sends the result back. This transforms stored data into information and helps create knowledge for decision making.
