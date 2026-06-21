# Day 29 - Group + Aggregate (Category-wise Summaries)

## What I Learned

Grouping organizes records into categories.

Aggregation summarizes records.

When Grouping and Aggregation are combined, we can create summaries for each category separately.

This is one of the most powerful ideas in data analysis.

---

## Learning Journey So Far

```text
Search
│
└── Find Records

Filter
│
└── Select Records

Sort
│
└── Organize Records

Aggregate
│
└── Summarize Records

Group
│
└── Categorize Records

Group + Aggregate
│
└── Summarize Each Category
```

---

## Why Group + Aggregate?

Without grouping:

```text
Average marks of all students
```

Result:

```text
84
```

Only one summary.

---

With grouping:

```text
Average marks of CSE

Average marks of ECE

Average marks of EEE
```

Now we get separate summaries for each category.

---

## Real Life Example: Students

Student Records:

```text
Lakshaga → CSE → 85

Priya → CSE → 91

Ravi → ECE → 72

Kumar → ECE → 80

Arun → EEE → 88
```

---

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

print(groups)
```

#### Output

```text
{
 'CSE': [85, 91],
 'ECE': [72, 80],
 'EEE': [88]
}
```
## Step 1 - Group Students

```text
CSE
│
├── Lakshaga → 85
└── Priya → 91

ECE
│
├── Ravi → 72
└── Kumar → 80

EEE
│
└── Arun → 88
```

---

## Step 2 - Aggregate Each Group

### CSE

```text
85 + 91 = 176

176 ÷ 2 = 88
```

Average:

```text
88
```

---

### ECE

```text
72 + 80 = 152

152 ÷ 2 = 76
```

Average:

```text
76
```

---

### EEE

```text
88
```

Average:

```text
88
```

---

## Final Result

```text
CSE → Average = 88

ECE → Average = 76

EEE → Average = 88
```

This is category-wise summary information.

---
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

    average = (
        sum(groups[dept])
        / len(groups[dept])
    )

    print(
        dept,
        "Average =",
        average
    )
```

#### Output

```text
CSE Average = 88.0
ECE Average = 76.0
EEE Average = 88.0
```

#### Logic

```text
Group Records
      ↓
Aggregate Each Group
      ↓
Return Category Summaries
```
## Library Example

Books:

```text
Python Basics → Programming → ₹500

Advanced Python → Programming → ₹900

Data Science → Data → ₹700

AI Fundamentals → AI → ₹800

Machine Learning → AI → ₹1000
```

---

## Group by Category

```text
Programming
│
├── ₹500
└── ₹900

Data
│
└── ₹700

AI
│
├── ₹800
└── ₹1000
```

---
#### Python Code

```python
books = [
    {"category": "Programming", "price": 500},
    {"category": "Programming", "price": 900},
    {"category": "Data", "price": 700},
    {"category": "AI", "price": 800},
    {"category": "AI", "price": 1000}
]

groups = {}

for book in books:

    category = book["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(
        book["price"]
    )

print(groups)
```

#### Output

```text
{
 'Programming': [500, 900],
 'Data': [700],
 'AI': [800, 1000]
}
```
## Aggregate Each Category

Programming:

```text
(500 + 900) ÷ 2

= 700
```

---

Data:

```text
700
```

---

AI:

```text
(800 + 1000) ÷ 2

= 900
```

---

## Final Result

```text
Programming → Average Price = ₹700

Data → Average Price = ₹700

AI → Average Price = ₹900
```

---
#### Python Code

```python
books = [
    {"category": "Programming", "price": 500},
    {"category": "Programming", "price": 900},
    {"category": "Data", "price": 700},
    {"category": "AI", "price": 800},
    {"category": "AI", "price": 1000}
]

groups = {}

for book in books:

    category = book["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(
        book["price"]
    )

for category in groups:

    average = (
        sum(groups[category])
        / len(groups[category])
    )

    print(
        category,
        "Average Price =",
        average
    )
```

#### Output

```text
Programming Average Price = 700.0
Data Average Price = 700.0
AI Average Price = 900.0
```
## Programming Team Model

### Worker 1

Traverses records.

---
#### Python Code

```python
for student in students:
    print(student)
```
### Worker 2

Reads category and value.

Example:

```text
Department + Marks

Category + Price
```

---

### Gate

Determines category.

---

### Organizer

Places records into groups.

---

### Aggregator

Calculates summary for each group.

---

#### Python Code

```python
for dept in groups:

    average = (
        sum(groups[dept])
        / len(groups[dept])
    )

    print(
        dept,
        average
    )
```
### Worker 3

Repeats for all records.

---

### Return Gate

Returns category-wise summaries.

---

## Group vs Aggregate

### Aggregate Only

Question:

```text
Average marks of all students?
```

Result:

```text
84
```

One summary.

---

### Group + Aggregate

Question:

```text
Average marks by department?
```

Result:

```text
CSE → 88

ECE → 76

EEE → 88
```

Multiple summaries.

---
#### Python Code

```python
groups = {
    "CSE": [85, 91],
    "ECE": [72, 80],
    "EEE": [88]
}

for dept in groups:

    average = (
        sum(groups[dept])
        / len(groups[dept])
    )

    print(
        dept,
        average
    )
```
## Why This Matters

Most real-world reports work this way.

Examples:

### School

```text
Average marks by department
```

---

### Company

```text
Average salary by team
```

---

### Store

```text
Total sales by product category
```

---

### Library

```text
Average book price by category
```

---
#### Python Example

```python
department_marks = {
    "CSE": [85, 91],
    "ECE": [72, 80],
    "EEE": [88]
}

for dept in department_marks:

    average = (
        sum(department_marks[dept])
        / len(department_marks[dept])
    )

    print(
        dept,
        average
    )
```
## Data Analysis Flow

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

Group
 ↓

Categories

Aggregate
 ↓

Category Summaries

Knowledge
 ↓

Insights
```

---

## Key Understanding

Grouping separates records into categories.

Aggregation summarizes records.

Group + Aggregate creates category-wise summaries that reveal patterns and insights.

---

## Simple Memory Rule

```text
Search
│
└── Find

Filter
│
└── Select

Sort
│
└── Organize

Aggregate
│
└── Summarize

Group
│
└── Categorize

Group + Aggregate
│
└── Summarize Categories
```

---

## Complete Mental Model

```text
Data
│
└── Stored Records

Group
│
└── Create Categories

Aggregate
│
└── Summarize Categories

Information
│
└── Category Results

Knowledge
│
└── Insights

Decision Making
│
└── Better Decisions
```

---
---

## Python Understanding

```text
Group
 ↓
Create Categories

Aggregate
 ↓
Create Summary

Group + Aggregate
 ↓
Category-wise Summary
```

### Core Pattern

```python
groups = {}

for record in records:

    category = record["category"]

    if category not in groups:
        groups[category] = []

    groups[category].append(
        record["value"]
    )

for category in groups:

    summary = (
        sum(groups[category])
        / len(groups[category])
    )

    print(
        category,
        summary
    )
```

### Mental Model

```text
Records
   ↓
Read Category
   ↓
Create Groups
   ↓
Add Values
   ↓
Aggregate Group
   ↓
Category Summary
```

## My Thought

Now I understand that grouping organizes records into categories, while aggregation summarizes records. When both are combined, category-wise summaries can be created. Worker 1 traverses records, Worker 2 reads category and value information, the Gate identifies the category, the Organizer places records into groups, the Aggregator summarizes each group, and the Return Gate provides category-wise results. This helps transform raw data into meaningful insights for decision making.
