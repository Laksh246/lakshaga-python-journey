# Day 24 - Functions + Search + Multiple Results (Finding All Matches)

## What I Learned

In Day 23, the search stopped when the first match was found.

Sometimes one match is not enough.

I may want to find all matching records.

For this, the function must continue searching through all records and collect every match.

---

## Day 23 vs Day 24

### Day 23

```text
Find first matching book
        ↓
Return immediately
        ↓
Stop searching
```

---

### Day 24

```text
Find matching book
        ↓
Store result
        ↓
Continue searching
        ↓
Find another match
        ↓
Store result
        ↓
Search entire collection
        ↓
Return all matches
```

---

## Real Life Example: Library

Imagine a library.

```text
Book 1 → Python Basics

Book 2 → Data Science

Book 3 → Python for Beginners

Book 4 → AI Fundamentals

Book 5 → Advanced Python
```

Suppose I ask:

```text
Find all Python books
```

I do not want only the first Python book.

I want every Python-related book.

---

## Why Day 23 Is Not Enough

If we stop at the first match:

```text
Python Basics
```

we miss:

```text
Python for Beginners

Advanced Python
```

Therefore we must continue searching.

---

## Python Idea

```python
library = [
    {"title": "Python Basics"},
    {"title": "Data Science"},
    {"title": "Python for Beginners"},
    {"title": "AI Fundamentals"},
    {"title": "Advanced Python"}
]

def find_python_books():

    results = []

    for book in library:

        if "Python" in book["title"]:
            results.append(book)

    return results
```

---

## New Concept: Results List

Before searching:

```python
results = []
```

This is an empty list.

Think of it as a basket.

```text
Results Basket
│
└── Empty
```

---

## Collecting Matches

When a match is found:

```python
results.append(book)
```

The matching book is placed into the basket.

---

Example:

```text
Python Basics
```

Basket becomes:

```text
Results Basket
│
└── Python Basics
```

---

Another match:

```text
Python for Beginners
```

Basket becomes:

```text
Results Basket
│
├── Python Basics
└── Python for Beginners
```

---

## Programming Team Model

### Worker 1

Traverses all books.

---

### Worker 2

Reads title.

---

### Gate

Checks:

```text
Contains "Python" ?
```

---

### Collector

Stores matching books.

---

### Worker 3

Repeats search for all remaining books.

---

### Return Gate

Returns the entire collection of matches.

---

## Search Flow

### Book 1

```text
Python Basics
```

Gate:

```text
Contains Python?
```

Result:

```text
YES
```

Store in basket.

---

### Book 2

```text
Data Science
```

Gate:

```text
Contains Python?
```

Result:

```text
NO
```

Skip.

---

### Book 3

```text
Python for Beginners
```

Result:

```text
YES
```

Store in basket.

---

### Book 4

```text
AI Fundamentals
```

Result:

```text
NO
```

Skip.

---

### Book 5

```text
Advanced Python
```

Result:

```text
YES
```

Store in basket.

---

## Final Return

```python
return results
```

Returns:

```text
Python Basics

Python for Beginners

Advanced Python
```

---

## Information vs Knowledge

### Information

Question:

```text
Which books contain Python?
```

Answer:

```text
Python Basics

Python for Beginners

Advanced Python
```

Information found.

---

### Knowledge

Decision:

```text
Choose a beginner-friendly Python book.
```

Knowledge helps decision making.

---

## Another Example: Student Marks

Data:

```text
Lakshaga → 85

Ravi → 72

Priya → 91

Arun → 88
```

Question:

```text
Find all students scoring above 80
```

Result:

```text
Lakshaga

Priya

Arun
```

Multiple matches found.

---

## Day 23 vs Day 24 Mental Model

### Day 23

```text
First Match
      ↓
Return
      ↓
Stop
```

---

### Day 24

```text
Match
 ↓
Collect

Match
 ↓
Collect

Match
 ↓
Collect

Search Complete
 ↓
Return All Matches
```

---

## Key Understanding

A reusable search function can:

### Return One Match

```text
Day 23
```

or

### Return Multiple Matches

```text
Day 24
```

To return multiple matches, a collection basket (list) is needed.

---

## Complete Mental Model

```text
Data
│
└── Library Records

Function
│
└── Reusable Search Machine

Worker 1
│
└── Traversal

Worker 2
│
└── Processing

Gate
│
└── Match Check

Collector
│
└── Stores Matches

Worker 3
│
└── Repetition

Return
│
└── All Matching Results

Information
│
└── Matching Records

Knowledge
│
└── Better Decisions
```

---

## My Thought

Now I understand that some searches require only the first match, while others require all matches. In a multiple-result search, Worker 1 traverses all records, Worker 2 processes each record, the Gate checks for matches, the Collector stores matching records in a results list, Worker 3 repeats the process until all records are checked, and the Return sends back all matching results. This allows one search function to answer broader questions and provide richer information for decision making.
