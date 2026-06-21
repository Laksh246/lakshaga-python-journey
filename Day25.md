# Day 25 - Sorting Results (Organizing Information)

## What I Learned

Searching helps find information.

Sometimes the results are not organized.

Sorting arranges information in a meaningful order.

Sorting makes information easier to understand and compare.

---

## Learning Journey So Far

Data
  ↓

Information
  ↓

Knowledge

And:

Search
│
└── Finds Matching Records

Sort
│
└── Organizes Matching Records

---

## Why Sorting is Needed

Suppose a search returns:

Python Basics      → ₹500

Advanced Python    → ₹900

Python Beginner    → ₹300

The information is correct.

But it is not organized.

Question:

Which is the cheapest?

Not immediately obvious.

After sorting:

Python Beginner    → ₹300

Python Basics      → ₹500

Advanced Python    → ₹900

Now comparison becomes easier.

---

## Real Life Example: Library

Imagine a library search.

Result:

Book A → ₹700

Book B → ₹300

Book C → ₹500

Unsorted Results

Book A → ₹700

Book B → ₹300

Book C → ₹500

Information exists.

But it is harder to compare.

Sorted Results

Book B → ₹300

Book C → ₹500

Book A → ₹700

Now the cheapest book appears first.

---

## Real Life Example: Student Marks

Marks:

Lakshaga → 85

Ravi → 72

Priya → 91

Arun → 88

Question:

Who scored highest?

Unsorted data makes comparison harder.

After sorting:

Priya → 91

Arun → 88

Lakshaga → 85

Ravi → 72

Now ranking becomes obvious.

---

## What Sorting Actually Does

Sorting does not create new data.

Sorting does not remove data.

Sorting only changes the order.

Before:

B
A
C

After:

A
B
C

Same data.

Different arrangement.

---

Programming Team Model

Worker 1

Traverses records.

Worker 2

Reads values used for comparison.

Example:

Price

Marks

Name

Comparator

Compares two values.

Example:

300 < 500 ?

Organizer

Places records in the correct order.

Worker 3

Repeats until all records are arranged.

---

## Library Example

Books:

Python Basics      → ₹500

Advanced Python    → ₹900

Python Beginner    → ₹300

Sorting by price:

300
 ↓
500
 ↓
900

Result:

Python Beginner

Python Basics

Advanced Python

---

## Student Example

Marks:

85

72

91

88

## Sorting highest first:

91
 ↓
88
 ↓
85
 ↓
72

Result:

Priya

Arun

Lakshaga

Ravi

---

Search vs Sort

Search

Answers:

What matches?

Example:

Find books related to Python.

Sort

Answers:

In what order should the results be arranged?

Example:

Arrange Python books from cheapest to most expensive.

---

## Information vs Organized Information

Search Result

Book A → ₹700

Book B → ₹300

Book C → ₹500

Information found.

Sorted Result

Book B → ₹300

Book C → ₹500

Book A → ₹700

Information organized.

---

Data → Information → Organized Information → Knowledge

Data
 ↓

Search
 ↓

Information
 ↓

Sort
 ↓

Organized Information
 ↓

Understanding
 ↓

Knowledge

---

## Python Examples

Example 1: Sort Numbers

numbers = [700, 300, 500]

sorted_numbers = sorted(numbers)

print(sorted_numbers)

Output:

[300, 500, 700]

---

Example 2: Sort Books by Price

books = [
    {"name": "Python Basics", "price": 500},
    {"name": "Advanced Python", "price": 900},
    {"name": "Python Beginner", "price": 300}
]

sorted_books = sorted(
    books,
    key=lambda book: book["price"]
)

for book in sorted_books:
    print(book["name"], "→ ₹" + str(book["price"]))

Output:

Python Beginner → ₹300
Python Basics → ₹500
Advanced Python → ₹900

---

Example 3: Sort Students by Marks

students = [
    {"name": "Lakshaga", "marks": 85},
    {"name": "Ravi", "marks": 72},
    {"name": "Priya", "marks": 91},
    {"name": "Arun", "marks": 88}
]

sorted_students = sorted(
    students,
    key=lambda student: student["marks"],
    reverse=True
)

for student in sorted_students:
    print(student["name"], "→", student["marks"])

Output:

Priya → 91
Arun → 88
Lakshaga → 85
Ravi → 72

---

Example 4: Search and Sort Together

books = [
    {"name": "Python Basics", "price": 500},
    {"name": "Advanced Python", "price": 900},
    {"name": "Python Beginner", "price": 300},
    {"name": "Machine Learning", "price": 800}
]

python_books = []

for book in books:
    if "Python" in book["name"]:
        python_books.append(book)

sorted_books = sorted(
    python_books,
    key=lambda book: book["price"]
)

for book in sorted_books:
    print(book["name"], "→ ₹" + str(book["price"]))

Output:

Python Beginner → ₹300
Python Basics → ₹500
Advanced Python → ₹900

---

## Key Understanding

Searching finds records.

Sorting arranges records.

Searching and sorting are often used together.

---

Complete Mental Model

Data
│
└── Stored Records

Search
│
└── Finds Matches

Information
│
└── Matching Records

Sort
│
└── Organizes Records

Organized Information
│
└── Easier Comparison

Knowledge
│
└── Better Decisions

---

## My Thought

Now I understand that searching helps find information, while sorting helps organize information. Searching answers "What matches my requirement?" and sorting answers "In what order should the results be arranged?" Sorting does not change the data itself; it only changes the arrangement. Organized information makes comparison easier and supports better knowledge and decision making.

I also learned that Python provides the "sorted()" function, which can organize numbers, text, and complex records based on specific rules. In real-world applications, searching and sorting are often used together to transform raw data into organized information that is easier to understand and use.
