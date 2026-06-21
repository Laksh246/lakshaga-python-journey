# Day 27 - Aggregation (Summarizing Data)

##  What I Learned

Sometimes I do not need individual records.

Instead, I need a summary of many records.

Aggregation means combining multiple records to produce a single meaningful result.

Aggregation helps transform information into insights.

---

##  Learning Journey So Far

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

Aggregation
 ↓

Summary Information

Knowledge
 ↓

Better Decisions
```

---

##  What is Aggregation?

Aggregation means:

```text
Many Records
      ↓
Combine
      ↓
One Summary Result
```

---

##  Real Life Example: Library

Library:

```text
Python Basics      → ₹500

Data Science       → ₹700

AI Fundamentals    → ₹900

Python Beginner    → ₹300
```

Instead of asking:

```text
What is the price of each book?
```

I ask:

```text
What is the total value
of all books?
```

This requires aggregation.

---

## 📊 Common Aggregations

### Count

#### Question

```text
How many books exist?
```

#### Result

```text
4 Books
```

#### Python Code

```python
books = [
    "Python Basics",
    "Data Science",
    "AI Fundamentals",
    "Python Beginner"
]

count = len(books)

print("Total Books:", count)
```

#### Output

```text
Total Books: 4
```

#### Logic

```text
Books
  ↓
Count Records
  ↓
Return Count
```

#### Key Takeaway

```text
Count tells us how many records exist.
```

---

### Sum

#### Question

```text
What is the total value
of all books?
```

#### Calculation

```text
500 + 700 + 900 + 300
```

#### Result

```text
₹2400
```

#### Python Code

```python
prices = [500, 700, 900, 300]

total_price = sum(prices)

print("Total Value:", total_price)
```

#### Output

```text
Total Value: 2400
```

#### Logic

```text
Read Prices
     ↓
Add Values
     ↓
Return Total
```

#### Key Takeaway

```text
Sum combines many values
into one total result.
```

---

### Average

#### Question

```text
What is the average price?
```

#### Calculation

```text
2400 ÷ 4
```

#### Result

```text
₹600
```

#### Python Code

```python
prices = [500, 700, 900, 300]

average_price = sum(prices) / len(prices)

print("Average Price:", average_price)
```

#### Output

```text
Average Price: 600.0
```

#### Logic

```text
Add Values
     ↓
Get Total
     ↓
Divide By Count
     ↓
Return Average
```

#### Key Takeaway

```text
Average shows the typical
value in a dataset.
```

---
### Maximum

#### Question

```text
Which book is most expensive?
```

#### Result

```text
AI Fundamentals → ₹900
```

#### Python Code

```python
books = {
    "Python Basics": 500,
    "Data Science": 700,
    "AI Fundamentals": 900,
    "Python Beginner": 300
}

most_expensive = max(
    books,
    key=books.get
)

print(
    most_expensive,
    "→ ₹" + str(books[most_expensive])
)
```

#### Output

```text
AI Fundamentals → ₹900
```

#### Logic

```text
Read Prices
     ↓
Compare Values
     ↓
Keep Highest Value
     ↓
Return Maximum
```

#### Key Takeaway

```text
Maximum finds the
largest value.
```

---

### Minimum

#### Question

```text
Which book is cheapest?
```

#### Result

```text
Python Beginner → ₹300
```

#### Python Code

```python
books = {
    "Python Basics": 500,
    "Data Science": 700,
    "AI Fundamentals": 900,
    "Python Beginner": 300
}

cheapest = min(
    books,
    key=books.get
)

print(
    cheapest,
    "→ ₹" + str(books[cheapest])
)
```

#### Output

```text
Python Beginner → ₹300
```

#### Logic

```text
Read Prices
     ↓
Compare Values
     ↓
Keep Lowest Value
     ↓
Return Minimum
```

#### Key Takeaway

```text
Minimum finds the
smallest value.
```

---

## Another Example: Student Marks

Marks:

```text
Lakshaga → 85

Ravi → 72

Priya → 91

Arun → 88
```

---

### Count

```text
4 Students
```

#### Python Code

```python
marks = [85, 72, 91, 88]

print(
    "Students:",
    len(marks)
)
```

#### Output

```text
Students: 4
```

#### Logic

```text
Marks
  ↓
Count Records
  ↓
Return Total Students
```

---

### Total Marks

```text
85 + 72 + 91 + 88

= 336
```

#### Python Code

```python
marks = [85, 72, 91, 88]

print(
    "Total Marks:",
    sum(marks)
)
```

#### Output

```text
Total Marks: 336
```

#### Logic

```text
Read Marks
     ↓
Add Marks
     ↓
Return Total
```

---

### Average Marks

```text
336 ÷ 4

= 84
```

#### Python Code

```python
marks = [85, 72, 91, 88]

average = (
    sum(marks)
    / len(marks)
)

print(
    "Average:",
    average
)
```

#### Output

```text
Average: 84.0
```

#### Logic

```text
Add Marks
     ↓
Get Total
     ↓
Divide By Count
     ↓
Return Average
```

---

### Highest Marks

```text
Priya → 91
```

#### Python Code

```python
marks = {
    "Lakshaga": 85,
    "Ravi": 72,
    "Priya": 91,
    "Arun": 88
}

highest = max(
    marks,
    key=marks.get
)

print(
    highest,
    "→",
    marks[highest]
)
```

#### Output

```text
Priya → 91
```

#### Logic

```text
Compare Marks
      ↓
Keep Highest
      ↓
Return Student
```

---

### Lowest Marks

```text
Ravi → 72
```

#### Python Code

```python
marks = {
    "Lakshaga": 85,
    "Ravi": 72,
    "Priya": 91,
    "Arun": 88
}

lowest = min(
    marks,
    key=marks.get
)

print(
    lowest,
    "→",
    marks[lowest]
)
```

#### Output

```text
Ravi → 72
```

#### Logic

```text
Compare Marks
      ↓
Keep Lowest
      ↓
Return Student
```

---

### Student Summary Example

#### Python Code

```python
marks = {
    "Lakshaga": 85,
    "Ravi": 72,
    "Priya": 91,
    "Arun": 88
}

count = len(marks)

total = sum(
    marks.values()
)

average = (
    total / count
)

highest = max(
    marks,
    key=marks.get
)

lowest = min(
    marks,
    key=marks.get
)

print("Students:", count)
print("Total:", total)
print("Average:", average)
print(
    "Highest:",
    highest,
    "→",
    marks[highest]
)
print(
    "Lowest:",
    lowest,
    "→",
    marks[lowest]
)
```

#### Output

```text
Students: 4
Total: 336
Average: 84.0
Highest: Priya → 91
Lowest: Ravi → 72
```

---
## ⚙️ Programming Team Model

### Worker 1

Traverses records.

#### Python Code

```python
prices = [500, 700, 900, 300]

for price in prices:
    print(price)
```

#### Output

```text
500
700
900
300
```

#### Logic

```text
Record 1
   ↓
Record 2
   ↓
Record 3
   ↓
Record 4
```

---

### Worker 2

Reads values.

Example:

```text
Price

Marks

Quantity
```

#### Python Code

```python
books = [
    {"name": "Python Basics", "price": 500},
    {"name": "Data Science", "price": 700}
]

for book in books:
    print(book["price"])
```

#### Output

```text
500
700
```

#### Logic

```text
Read Record
      ↓
Extract Value
      ↓
Pass To Aggregator
```

---

### Aggregator

Collects and combines values.

#### Python Code

```python
prices = [500, 700, 900, 300]

total = 0

for price in prices:
    total += price

print(total)
```

#### Output

```text
2400
```

#### Logic

```text
500
 ↓
1200
 ↓
2100
 ↓
2400
```

---

### Worker 3

Repeats for all records.

#### Python Code

```python
prices = [500, 700, 900, 300]

total = 0

for price in prices:
    total += price

print(total)
```

#### Logic

```text
Read Value
    ↓
Aggregate
    ↓
Repeat
    ↓
Aggregate
    ↓
Repeat
```

---

### Return Gate

Returns the final summary.

#### Python Code

```python
prices = [500, 700, 900, 300]

print(sum(prices))
```

#### Output

```text
2400
```

#### Logic

```text
Aggregate Complete
        ↓
Return Result
```

---

## 🔍 Understanding Aggregation

Suppose we want the total book price.

Books:

```text
500

700

900

300
```

---

Traversal:

```text
500
 ↓
700
 ↓
900
 ↓
300
```

#### Python Code

```python
prices = [500, 700, 900, 300]

for price in prices:
    print(price)
```

#### Output

```text
500
700
900
300
```

---

Aggregation:

```text
500 + 700 + 900 + 300
```

#### Python Code

```python
prices = [500, 700, 900, 300]

total = sum(prices)

print(total)
```

#### Output

```text
2400
```

---

Result:

```text
2400
```

#### Logic

```text
Read Values
     ↓
Combine Values
     ↓
Generate Summary
```

---

## 🔄 Aggregation vs Search

### Search

Question:

```text
Which book matches?
```

Result:

```text
Specific Record
```

#### Python Code

```python
books = [
    "Python Basics",
    "Data Science",
    "AI Fundamentals"
]

search_book = "Python Basics"

for book in books:
    if book == search_book:
        print(book)
        break
```

#### Output

```text
Python Basics
```

#### Logic

```text
Traverse Records
      ↓
Find Match
      ↓
Return Record
```

---

### Aggregation

Question:

```text
What summary can be created?
```

Result:

```text
Count

Total

Average

Maximum

Minimum
```

#### Python Code

```python
prices = [500, 700, 900, 300]

print("Count:", len(prices))
print("Total:", sum(prices))
print("Average:", sum(prices) / len(prices))
print("Maximum:", max(prices))
print("Minimum:", min(prices))
```

#### Output

```text
Count: 4
Total: 2400
Average: 600.0
Maximum: 900
Minimum: 300
```

#### Logic

```text
Many Records
      ↓
Create Summary
      ↓
Return Insight
```

---

## 🔄 Aggregation vs Filter

### Filter

Returns:

```text
Matching Records
```

Example:

```text
Books below ₹800
```

#### Python Code

```python
prices = [500, 700, 900, 300]

filtered_prices = []

for price in prices:
    if price < 800:
        filtered_prices.append(price)

print(filtered_prices)
```

#### Output

```text
[500, 700, 300]
```

#### Logic

```text
Apply Condition
      ↓
Keep Matches
      ↓
Return Records
```

---

### Aggregation

Returns:

```text
One Summary Result
```

Example:

```text
Average Price
```

#### Python Code

```python
prices = [500, 700, 900, 300]

average = sum(prices) / len(prices)

print(average)
```

#### Output

```text
600.0
```

#### Logic

```text
Read Values
      ↓
Combine Values
      ↓
Return Summary
```

---

##  Real World Examples

### School

```text
Average Marks

Highest Marks

Number of Students
```

#### Python Code

```python
marks = [85, 72, 91, 88]

print("Students:", len(marks))
print("Average:", sum(marks) / len(marks))
print("Highest:", max(marks))
```

---

### Library

```text
Total Books

Average Price

Most Expensive Book
```

#### Python Code

```python
prices = [500, 700, 900, 300]

print("Books:", len(prices))
print("Average:", sum(prices) / len(prices))
print("Highest:", max(prices))
```

---

### Store

```text
Total Sales

Average Product Price

Best Selling Product
```

#### Python Code

```python
sales = [1200, 1500, 1000, 2000]

print("Total Sales:", sum(sales))
print("Average Sale:", sum(sales) / len(sales))
print("Highest Sale:", max(sales))
```

---
##  Data → Information → Knowledge

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

Aggregation
 ↓

Summary Information

Knowledge
 ↓

Better Decisions
```

---

### Complete Flow Example

Books:

```text
Python Basics      → ₹500

Data Science       → ₹700

AI Fundamentals    → ₹900

Python Beginner    → ₹300
```

#### Step 1: Search

```text
Find Python Books
```

#### Python Code

```python
books = [
    {"name": "Python Basics", "price": 500},
    {"name": "Data Science", "price": 700},
    {"name": "AI Fundamentals", "price": 900},
    {"name": "Python Beginner", "price": 300}
]

python_books = []

for book in books:
    if "Python" in book["name"]:
        python_books.append(book)

print(python_books)
```

#### Output

```text
[
 {'name': 'Python Basics', 'price': 500},
 {'name': 'Python Beginner', 'price': 300}
]
```

---

#### Step 2: Filter

```text
Keep Books Below ₹800
```

#### Python Code

```python
filtered_books = []

for book in python_books:
    if book["price"] < 800:
        filtered_books.append(book)

print(filtered_books)
```

#### Output

```text
[
 {'name': 'Python Basics', 'price': 500},
 {'name': 'Python Beginner', 'price': 300}
]
```

---

#### Step 3: Sort

```text
Arrange By Price
```

#### Python Code

```python
sorted_books = sorted(
    filtered_books,
    key=lambda book: book["price"]
)

print(sorted_books)
```

#### Output

```text
[
 {'name': 'Python Beginner', 'price': 300},
 {'name': 'Python Basics', 'price': 500}
]
```

---

#### Step 4: Aggregate

```text
Calculate Total Price
```

#### Python Code

```python
total_price = sum(
    book["price"]
    for book in sorted_books
)

print(total_price)
```

#### Output

```text
800
```

---

#### Complete Logic

```text
Books
  ↓
Search
  ↓
Python Books
  ↓
Filter
  ↓
Affordable Books
  ↓
Sort
  ↓
Organized Books
  ↓
Aggregate
  ↓
Summary Information
  ↓
Knowledge
```

---

##  Key Understanding

Aggregation summarizes many records into a smaller and more useful result.

Instead of viewing every record individually, aggregation provides an overall picture.

#### Python Example

```python
prices = [500, 700, 900, 300]

print("Count:", len(prices))
print("Sum:", sum(prices))
print("Average:", sum(prices) / len(prices))
print("Maximum:", max(prices))
print("Minimum:", min(prices))
```

#### Output

```text
Count: 4
Sum: 2400
Average: 600.0
Maximum: 900
Minimum: 300
```

---

##  Simple Memory Rule

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
```

#### Python Memory Rule

```python
# Search
if book == "Python Basics":
    print(book)

# Filter
if price < 800:
    filtered.append(price)

# Sort
sorted(prices)

# Aggregate
sum(prices)
```

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

Aggregation
│
└── Summarizes Records

Information
│
└── Useful Results

Knowledge
│
└── Better Decisions
```

---

##  Python Understanding

```text
Search
  ↓
Comparison

Filter
  ↓
Condition Checking

Sort
  ↓
Ordering Rules

Aggregation
  ↓
Summary Calculations
```

### Common Aggregation Functions

#### Count

```python
len(records)
```

#### Sum

```python
sum(values)
```

#### Average

```python
sum(values) / len(values)
```

#### Maximum

```python
max(values)
```

#### Minimum

```python
min(values)
```

---

## My Thought

Now I understand that aggregation is the process of summarizing multiple records into a single meaningful result.

Worker 1 traverses records.

Worker 2 reads values.

The Aggregator combines values.

Worker 3 repeats the process for all records.

The Return Gate provides the final summary.

Aggregation helps convert detailed information into summary information that supports better understanding and decision making.

I also learned that aggregation commonly produces:

```text
Count

Sum

Average

Maximum

Minimum
```

and these operations are heavily used in schools, libraries, stores, business reports, analytics dashboards, search systems, and data science applications.

Aggregation is the final step that transforms organized information into useful knowledge.

---
