# Day 20 - List of Dictionaries (Many Items with Many Properties)

## What I Learned

A list can store many items.

A dictionary can store many properties of one item.

A List of Dictionaries combines both ideas.

This allows us to store:

> Many items, where each item has many properties.

This is one of the most common ways real-world data is stored.

---

## Before Day 20

### Variable

Stores one value.

```text
name → Lakshaga
```

---

### List

Stores many items.

```text
Library
│
├── Book 1
├── Book 2
├── Book 3
└── Book 4
```

Question answered:

```text
How many books do I have?
```

---

### Dictionary

Stores one item with many properties.

```text
Book
│
├── Title  → Python Basics
├── Author → John Smith
├── Pages  → 250
└── Price  → ₹500
```

Question answered:

```text
What details does this book have?
```

---

### List of Dictionaries

Stores many items where each item has many properties.

```text
Library
│
├── Book 1
│     ├── Title
│     ├── Author
│     └── Price
│
├── Book 2
│     ├── Title
│     ├── Author
│     └── Price
│
└── Book 3
      ├── Title
      ├── Author
      └── Price
```

Question answered:

```text
How many books do I have?

What details does each book have?
```

---

## Real Life Example: Library

Imagine a library.

The library contains many books.

Each book has its own details.

```text
Library
│
├── Book 1
│     ├── Title  → Python Basics
│     ├── Author → John Smith
│     └── Price  → ₹500
│
├── Book 2
│     ├── Title  → Data Science
│     ├── Author → Mary Jones
│     └── Price  → ₹700
│
└── Book 3
      ├── Title  → AI Fundamentals
      ├── Author → David Lee
      └── Price  → ₹900
```

---

## Python Idea

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
    },
    {
        "title": "AI Fundamentals",
        "author": "David Lee",
        "price": 900
    }
]
```

---

## Understanding the Structure

### Outer Container

```text
Library
```

This is a List.

---

### Each Book

```text
Book
│
├── Title
├── Author
└── Price
```

This is a Dictionary.

---

## Accessing a Book

Suppose I want the first book.

```python
library[0]
```

Result:

```text
Book 1 Dictionary
```

---

## Accessing a Property

Suppose I want the title of the first book.

```python
library[0]["title"]
```

Output:

```text
Python Basics
```

---

## Programming Team Model

### Library

List of books.

---

### Book

Dictionary containing details.

---

### Worker 1 - Traversal

Visits each book one by one.

```text
Book 1
 ↓
Book 2
 ↓
Book 3
```

---

### Worker 2 - Processing

Reads book details.

Example:

```text
Title  → Python Basics
Author → John Smith
Price  → ₹500
```

---

### Gate (Condition)

Can make decisions.

Example:

```text
Price > ₹600 ?
```

---

### Worker 3 - Automatic Repetition

Repeats the same process for every book.

---

## Loop Through All Books

```python
for book in library:
    print(book["title"])
```

Output:

```text
Python Basics
Data Science
AI Fundamentals
```

---

## Loop + Condition

Suppose I want books costing more than ₹600.

```python
for book in library:

    if book["price"] > 600:
        print(book["title"])
```

Output:

```text
Data Science
AI Fundamentals
```

---

## What Happens Internally?

For each book:

### Worker 1

Traverses to the next book.

---

### Worker 2

Reads the price.

---

### Gate

Checks:

```text
Price > ₹600 ?
```

---

### Worker 3

Repeats for the next book.

---

## Why This Structure Is Powerful

Almost every real-world system uses this idea.

### Classroom

```text
Students List
│
├── Student Dictionary
├── Student Dictionary
└── Student Dictionary
```

---

### Employee Database

```text
Employees List
│
├── Employee Dictionary
├── Employee Dictionary
└── Employee Dictionary
```

---

### Product Catalog

```text
Products List
│
├── Product Dictionary
├── Product Dictionary
└── Product Dictionary
```

---

### Library

```text
Books List
│
├── Book Dictionary
├── Book Dictionary
└── Book Dictionary
```

---

## Key Understanding

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

This is the first data structure that closely resembles a real database.

---

## My Thought

Now I understand that a List of Dictionaries combines the strengths of both structures. The list stores many items, while each dictionary stores the properties of one item. Worker 1 traverses through the items, Worker 2 processes their details, the Gate can make decisions based on conditions, and Worker 3 automatically repeats the process. This structure is commonly used to represent real-world data such as students, books, employees, and products.
