# Day 28 - Grouping (Organizing Data into Categories)

## What I Learned

Until now, I treated all records as one large collection.

Sometimes I need to organize records into categories.

Grouping means placing similar records together based on a common property.

Grouping helps me understand data category by category instead of viewing everything as one large collection.

---

## Learning Journey So Far

```text
Variable
│
└── Store One Value

List
│
└── Store Many Items

Dictionary
│
└── Store Properties of One Item

List of Dictionaries
│
└── Store Many Items with Properties

Loop
│
└── Traverse Data

Condition
│
└── Make Decisions

Function
│
└── Reusable Processing Machine

Return
│
└── Send Results Back

Search
│
└── Find Information

Filter
│
└── Select Relevant Information

Sort
│
└── Organize Information

Aggregate
│
└── Summarize Information

Group
│
└── Organize Information into Categories
```

---

## Big Picture

```text
Store
  ↓

Traverse
  ↓

Process
  ↓

Decide
  ↓

Find
  ↓

Select
  ↓

Organize
  ↓

Summarize
  ↓

Group
  ↓

Understand
```

This is similar to how real-world systems, databases, dashboards, analytics tools, and AI systems process information.

---

## Memory Rule

```text
Search
│
└── Which record?

Filter
│
└── Which records satisfy a condition?

Sort
│
└── In what order?

Aggregate
│
└── What summary?

Group
│
└── Which category?
```

---

## What is Grouping?

Grouping means:

```text
Many Records
      ↓
Separate by Category
      ↓
Category-wise Collections
```

Instead of treating everything as one large collection, we organize records into smaller groups.

---

## Real Life Example: Library

Library Data:

```text
Python Basics       → Programming

Data Science        → Data

AI Fundamentals     → AI

Advanced Python     → Programming

Machine Learning    → AI
```

---

## Without Grouping

All books appear together:

```text
Python Basics

Data Science

AI Fundamentals

Advanced Python

Machine Learning
```

Everything is mixed.

---

## With Grouping

```text
Programming
│
├── Python Basics
└── Advanced Python

Data
│
└── Data Science

AI
│
├── AI Fundamentals
└── Machine Learning

#### Python Code

```python
books = [
    {"name": "Python Basics", "category": "Programming"},
    {"name": "Data Science", "category": "Data"},
    {"name": "AI Fundamentals", "category": "AI"},
    {"name": "Advanced Python", "category": "Programming"},
    {"name": "Machine Learning", "category": "AI"}
]

groups = {}

for book in books:
    category = book["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(book["name"])

print(groups)
```

#### Output

```text
{
 'Programming': ['Python Basics', 'Advanced Python'],
 'Data': ['Data Science'],
 'AI': ['AI Fundamentals', 'Machine Learning']
}
```

#### Logic

```text
Read Book
    ↓
Read Category
    ↓
Create Group If Needed
    ↓
Add Book To Group
```
```

Now similar books are together.

---

## Another Example: Students

Students:

```text
Lakshaga → CSE

Ravi → ECE

Priya → CSE

Arun → EEE

Kumar → ECE
```

---

### Grouped Result

```text
CSE
│
├── Lakshaga
└── Priya

ECE
│
├── Ravi
└── Kumar

EEE
│
└── Arun
```


Now students are organized department-wise.

#### Python Code

```python
students = [
    {"name": "Lakshaga", "dept": "CSE"},
    {"name": "Ravi", "dept": "ECE"},
    {"name": "Priya", "dept": "CSE"},
    {"name": "Arun", "dept": "EEE"},
    {"name": "Kumar", "dept": "ECE"}
]

departments = {}

for student in students:
    dept = student["dept"]

    if dept not in departments:
        departments[dept] = []

    departments[dept].append(student["name"])

print(departments)
```

#### Output

```text
{
 'CSE': ['Lakshaga', 'Priya'],
 'ECE': ['Ravi', 'Kumar'],
 'EEE': ['Arun']
}
```

---

## Why Grouping is Useful

Without grouping:

```text
Average marks of all students
```

Only one summary.

---

With grouping:

```text
Average marks of CSE

Average marks of ECE

Average marks of EEE
```

Now we can compare categories.

#### Python Code

```python
students = [
    {"name": "Lakshaga", "dept": "CSE", "mark": 85},
    {"name": "Priya", "dept": "CSE", "mark": 91},
    {"name": "Ravi", "dept": "ECE", "mark": 72},
    {"name": "Kumar", "dept": "ECE", "mark": 80},
    {"name": "Arun", "dept": "EEE", "mark": 88}
]

groups = {}

for student in students:
    dept = student["dept"]

    if dept not in groups:
        groups[dept] = []

    groups[dept].append(student["mark"])

for dept in groups:
    average = sum(groups[dept]) / len(groups[dept])

    print(dept, "Average =", average)
```

#### Output

```text
CSE Average = 88.0
ECE Average = 76.0
EEE Average = 88.0
```

---

## Programming Team Model

### Worker 1

Traverses records.

---

#### Python Code

```python
books = [
    {"name": "Python Basics", "category": "Programming"},
    {"name": "Data Science", "category": "Data"}
]

for book in books:
    print(book)
```
### Worker 2

Reads category information.

Example:

```text
Department

Category

Brand

Team
```

---

### Gate

Determines which category the record belongs to.

---

### Organizer

Places records into the correct group.

---

### Worker 3

Repeats for all records.

---

### Return Gate

Returns grouped collections.

---

## Grouping Process

Example:

```text
Python Basics → Programming
```

Worker 1:

```text
Visit Record
```

Worker 2:

```text
Read Category
```

Gate:

```text
Programming?
```

Organizer:

```text
Place into Programming Group
```

Worker 3:

```text
Repeat for remaining records
```

---

#### Python Code

```python
books = [
    {"name": "Python Basics", "category": "Programming"},
    {"name": "Data Science", "category": "Data"},
    {"name": "AI Fundamentals", "category": "AI"}
]

groups = {}

for book in books:

    category = book["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(book["name"])

print(groups)
```

#### Logic

```text
Visit Record
     ↓
Read Category
     ↓
Find Group
     ↓
Add Record
     ↓
Repeat
```
## Search vs Filter vs Sort vs Aggregate vs Group

### Search

```text
Find Python Basics
```

Result:

```text
One Record
```

---

### Filter

```text
Find books below ₹800
```

Result:

```text
Matching Records
```

---

### Sort

```text
Arrange books by price
```

Result:

```text
Ordered Records
```

---

### Aggregate

```text
Average book price
```

Result:

```text
One Summary
```

---

### Group

```text
Books by category
```

Result:

```text
Category-wise Collections
```

---

#### Python Comparison

```python
books = [
    {"name": "Python Basics", "category": "Programming"},
    {"name": "Advanced Python", "category": "Programming"},
    {"name": "AI Fundamentals", "category": "AI"}
]

groups = {}

for book in books:

    category = book["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(book["name"])

print(groups)
```

#### Output

```text
{
 'Programming': [
     'Python Basics',
     'Advanced Python'
 ],
 'AI': [
     'AI Fundamentals'
 ]
}
```

## Library Question Examples

Books Data:

```text
Python Basics
Data Science
AI Fundamentals
Advanced Python
Machine Learning
```

Questions:

```text
Search:
Find Python Basics

Filter:
Find books below ₹800

Sort:
Arrange by price

Aggregate:
Average book price

Group:
Books by category
```

Each operation answers a different type of question.

---

## Data → Information → Knowledge

```text
Data
 ↓

Search
 ↓

Information

Filter
 ↓

Relevant Information

Sort
 ↓

Organized Information

Aggregate
 ↓

Summary Information

Group
 ↓

Category-wise Information

Knowledge
 ↓

Better Decisions
```

---

## Knowledge by Category

Before Grouping:

```text
Average marks of all students
```

One overall summary.

---

After Grouping:

```text
Average marks of CSE

Average marks of ECE

Average marks of EEE
```

Knowledge becomes more detailed and meaningful.

---

## Key Understanding

Grouping organizes records based on a shared property.

Instead of treating everything as one collection, grouping creates category-wise collections that are easier to analyze and compare.

---

## Complete Mental Model

```text
Data
│
└── Stored Records

Search
│
└── Finds Records

Filter
│
└── Selects Records

Sort
│
└── Organizes Records

Aggregate
│
└── Summarizes Records

Group
│
└── Categorizes Records

Information
│
└── Useful Results

Knowledge
│
└── Category-wise Understanding

Decision Making
│
└── Better Actions
```

---

---

## Python Understanding

```text
Search
 ↓
Comparison

Filter
 ↓
Condition

Sort
 ↓
Ordering

Aggregate
 ↓
Summary

Group
 ↓
Categorization
```

### Grouping Formula

```python
groups = {}

for record in records:

    category = record["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(record)
```

### Mental Model

```text
Records
   ↓
Read Category
   ↓
Create Group
   ↓
Add Record
   ↓
Repeat
   ↓
Grouped Collections
```

## My Thought

Now I understand that grouping means organizing records into categories based on a common property. Worker 1 traverses records, Worker 2 reads the category information, the Gate determines which category the record belongs to, the Organizer places the record into the correct group, and Worker 3 repeats the process for all records. Grouping helps transform information into category-wise knowledge, making analysis and decision making more powerful.
