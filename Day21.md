# Day 21 - Searching in a List of Dictionaries (Finding Information)

## What I Learned

Storing data is useful.

But in real applications, we often need to find specific information from stored data.

Searching means looking through data and finding items that match a condition.

This is where Lists, Dictionaries, Loops, and Conditions work together.

---

## Learning Journey So Far

```text
Variable
│
└── One Value

List
│
└── Many Items

Dictionary
│
└── One Item with Many Properties

List of Dictionaries
│
└── Many Items
      │
      └── Each Item Has Many Properties
```

---

## Programming Team Model

```text
Worker 1
│
└── Traversal

Worker 2
│
└── Processing

Gate
│
└── Decision Making

Worker 3
│
└── Automatic Repetition

Function
│
└── Reusable Machine

Return
│
└── Sends Result Back
```

---

## Why Searching is Needed

Real systems do not just store data.

They answer questions.

Examples:

```text
Find student named Lakshaga

Find book titled Python Basics

Find products cheaper than ₹500

Find employees in Computer Science department
```

Searching helps us find useful information from stored data.

---

## Real Life Example: Library Search

Imagine a library.

```text
Library
│
├── Book 1
│     ├── Title  → Python Basics
│     ├── Author → John Smith
│
├── Book 2
│     ├── Title  → Data Science
│     ├── Author → Mary Jones
│
└── Book 3
      ├── Title  → AI Fundamentals
      ├── Author → David Lee
```

Suppose I want to find:

```text
Python Basics
```

I do not know where it is.

I must search through the books.

---

## Manual Search

Without a loop:

```text
Check Book 1

If found → Stop

Otherwise check Book 2

If found → Stop

Otherwise check Book 3
```

This becomes difficult for hundreds of books.

---

## Smart Search Using a Loop

Give one instruction:

```text
Check every book
until the required title is found
```

---

## Python Idea

```python
library = [
    {"title": "Python Basics"},
    {"title": "Data Science"},
    {"title": "AI Fundamentals"}
]

for book in library:

    if book["title"] == "Python Basics":
        print("Book Found")
```

---

## What Happens Internally?

### Worker 1 - Traversal

Visits books one by one.

```text
Book 1
 ↓
Book 2
 ↓
Book 3
```

---

### Worker 2 - Processing

Reads the title.

Example:

```text
Python Basics
```

---

### Gate - Decision

Checks:

```text
Title = Python Basics ?
```

---

### Worker 3 - Automatic Repetition

Repeats the search for every remaining book.

---

## Detailed Search Flow

### Book 1

Worker 1:

```text
Visit Book 1
```

Worker 2:

```text
Read Title
```

Gate:

```text
Python Basics == Python Basics
```

Result:

```text
TRUE
```

Book found.

---

### If Not Found

Suppose searching for:

```text
Machine Learning
```

Book 1:

```text
FALSE
```

Worker 3 repeats.

Book 2:

```text
FALSE
```

Worker 3 repeats.

Book 3:

```text
FALSE
```

Search completed.

No match found.

---

## Understanding Search Time

Even checking takes time.

To decide whether a book matches:

```text
Visit Book
 ↓
Read Title
 ↓
Compare Title
 ↓
Decision
```

This processing happens for every book until a match is found or the search ends.

---

## Real Life Search Example

Finding a word in a book.

```text
Page 1
 ↓
Read Page
 ↓
Check for word

Page 2
 ↓
Read Page
 ↓
Check for word

Page 3
 ↓
Read Page
 ↓
Check for word
```

Even if the word does not exist, the pages still need to be checked.

The same idea applies to searching in programming.

---

## Search = Loop + Condition

```text
Loop
 ↓
Traverse Data

Condition
 ↓
Check Match

Repeat
 ↓
Until Finished
```

---

## Searching with More Details

```python
library = [
    {
        "title": "Python Basics",
        "author": "John Smith",
        "price": 500
    },
    {
        "title": "Data Science",
        "author": "Mary Jones",
        "price": 700
    }
]

for book in library:

    if book["price"] > 600:
        print(book["title"])
```

Output:

```text
Data Science
```

---

## Key Understanding

Storage answers:

```text
What data do I have?
```

Searching answers:

```text
Which data matches my requirement?
```

---

## Complete Mental Model

```text
List
│
└── Stores Many Records

Dictionary
│
└── Stores Details of One Record

Loop
│
└── Traverses Records

Worker 2
│
└── Reads Data

Gate
│
└── Checks Condition

Worker 3
│
└── Repeats Search

Search
│
└── Finds Matching Records
```

---

## 💭 My Thought

Now I understand that searching is the process of finding specific information from stored data. A loop traverses records one by one, Worker 2 reads the details, the Gate checks whether the data matches the requirement, and Worker 3 repeats the process until a match is found or all records have been checked. Searching combines Lists, Dictionaries, Loops, and Conditions to answer useful questions from data.
