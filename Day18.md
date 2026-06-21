# Day 18 - Dictionaries (Key → Value Storage)

## What I Learned

A dictionary stores information as **key → value** pairs.

Instead of finding data by position (index), a dictionary finds data using a key.

A dictionary is useful when each piece of information has a label.

---

## Real Life Example: Student ID Card

Imagine a student ID card.

It contains information like:

```text
Name       → Lakshaga
Age        → 30
Department → Computer Science
College    → ABC College
```

Each label has a corresponding value.

This is similar to a Python dictionary.

---

## Dictionary as a Record

```text
Label (Key)     → Information (Value)

Name            → Lakshaga
Age             → 30
Department      → Computer Science
```

---

## Python Idea

```python
student = {
    "name": "Lakshaga",
    "age": 30,
    "department": "Computer Science"
}
```

---

## Accessing Information

Suppose I want the student's name.

```python
print(student["name"])
```

Output:

```text
Lakshaga
```

---

Suppose I want the student's age.

```python
print(student["age"])
```

Output:

```text
30
```

---

## List vs Dictionary

### List

Stores information by position.

```python
fruits = ["Apple", "Mango", "Orange"]
```

Access:

```python
fruits[0]
```

Output:

```text
Apple
```

---

### Dictionary

Stores information by label.

```python
student["name"]
```

Output:

```text
Lakshaga
```

---

## Real Life Comparison

### Book

To find information:

```text
Go to Page 50
```

This is similar to a List (position-based).

---

### Student ID Card

To find information:

```text
Look at Name
Look at Age
Look at Department
```

This is similar to a Dictionary (label-based).

---

## Adding New Information

```python
student["city"] = "Salem"
```

Now:

```text
Name       → Lakshaga
Age        → 30
Department → Computer Science
City       → Salem
```

---

## Updating Information

```python
student["age"] = 31
```

The old value is replaced.

---

## Programming Team Model

### Dictionary

Stores labeled information.

---

### Key

Acts as a label.

Example:

```text
Name
Age
Department
```

---

### Value

Actual information stored.

Example:

```text
Lakshaga
30
Computer Science
```

---

### Lookup

Uses a key to retrieve a value.

```text
Name → Lakshaga
```

---

## Important Concept

A dictionary answers questions like:

```text
What is the student's name?

What is the student's age?

What is the student's department?
```

The key identifies what information is needed.

The value provides the answer.

---

## Key Understanding

Why Do We Need Dictionaries?

Before learning dictionaries, I wondered:

«Why can't I just use variables or lists?»

Using Separate Variables

name = "Lakshaga"
age = 30
department = "Computer Science"
city = "Salem"

This works, but Python sees them as separate variables.

There is no single container connecting them together as one student record.

---

Using a Dictionary

student = {
    "name": "Lakshaga",
    "age": 30,
    "department": "Computer Science",
    "city": "Salem"
}

Now Python knows that all the information belongs to one student.

Student
│
├── Name       → Lakshaga
├── Age        → 30
├── Department → Computer Science
└── City       → Salem

A dictionary groups related information together.

---

When a Dictionary is Better Than a List

Consider a student record.

Name       → Lakshaga
Age        → 30
Department → Computer Science
City       → Salem

Using a List

student = ["Lakshaga", 30, "Computer Science", "Salem"]

To get the department:

student[2]

But position 2 is not obvious.

I must remember:

0 = Name
1 = Age
2 = Department
3 = City

This can become confusing.

---

Using a Dictionary

student["department"]

Immediately tells me what information I am accessing.

Therefore, dictionaries are useful when data has labels or properties.

---

When a List is Better Than a Dictionary

Consider a book.

Page 1
Page 2
Page 3
Page 4

The order matters.

Using a list is natural.

book = ["Page 1", "Page 2", "Page 3", "Page 4"]

I can access pages by position.

book[0]

returns the first page.

---

Using a dictionary:

book = {
    "page1": "Page 1",
    "page2": "Page 2",
    "page3": "Page 3",
    "page4": "Page 4"
}

works, but the labels add little value because the order is already important.

Therefore, lists are useful when sequence and position matter.

---

Simple Rule

Variable

One labeled box

Example:

name → Lakshaga

---

List

One box holding many items in order

Example:

Book
│
├── Page 1
├── Page 2
├── Page 3
└── Page 4

Use when you have many items and order matters.

---

Dictionary

One box holding many labeled items

Example:

Student
│
├── Name → Lakshaga
├── Age → 30
├── City → Salem
└── Department → Computer Science

Use when you have one thing with many properties.

---

Memory Rule

Variable  → One Value

List      → Many Items

Dictionary → One Item with Many Properties

Examples:

Many Students          → List

One Student Details    → Dictionary

Many Books             → List

One Book Details       → Dictionary

Many Products          → List

One Product Details    → Dictionary

List:

```text
Position → Value
```

Example:

```text
0 → Apple
1 → Mango
2 → Orange
```

Dictionary:

```text
Key → Value
```

Example:

```text
Name → Lakshaga
Age → 30
Department → Computer Science
```

Lists organize data by position

Dictionaries organize data by labels.

---

## My Thought

Now I understand that a dictionary is like a student record or ID card. Instead of finding information by position, I use a label called a key. The key points to a value. Dictionaries are useful when information naturally has names or labels, making data easier to understand and retrieve.
