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

## Data vs Information

Before learning searching, it is important to understand the difference between data and information.

### Data

Data is raw stored facts.

Example:

```text
Book 1
│
├── Title  → Python Basics
├── Author → John Smith
├── Price  → ₹500

Book 2
│
├── Title  → Data Science
├── Author → Mary Jones
├── Price  → ₹700
```

These are simply stored records.

At this stage, they are data.

---

### Information

Information is data that answers a question.

Question:

```text
Which books cost more than ₹600?
```

After searching:

```text
Data Science → ₹700
```

This result is information because it is useful and answers a specific question.

---

## How Data Becomes Information

```text
Data
  +
Processing
  +
Question / Context
  =
Information
```

---

### Example 1

Data:

```text
Price → ₹700
```

Question:

```text
Is it above ₹600?
```

Information:

```text
Yes
```

---

### Example 2

Data:

```text
Title → Python Basics
```

Question:

```text
Do we have a Python book?
```

Information:

```text
Yes, Python Basics
```

---

## Role of Searching

Searching is the process that transforms stored data into useful information.

Without searching:

```text
Library
│
├── Book 1
├── Book 2
└── Book 3
```

Only data exists.

---

With searching:

```text
Question:
Which books are related to Python?

Answer:
Python Basics
```

Now data has become information.

---

## Updated Programming Team Model

### Worker 1

Traverses records.

---

### Worker 2

Reads and processes data.

---

### Gate

Checks whether the data satisfies the condition.

---

### Worker 3

Repeats the process.

---

### Result

Produces useful information.

```text
Data
 ↓
Processing
 ↓
Condition Check
 ↓
Information
```

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

## My Thought

Now I understand that data is raw stored facts, while information is meaningful data that answers a question. Searching is the process that converts data into information. A loop traverses records, Worker 2 processes the data, the Gate checks conditions, and Worker 3 repeats the process until a match is found or all records are checked. Searching combines Lists, Dictionaries, Loops, and Conditions to transform stored data into useful information.
