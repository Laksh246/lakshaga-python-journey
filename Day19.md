# Day 19 - Looping Through Dictionaries (Reading a Complete Record)

## What I Learned

A dictionary stores information as key-value pairs.

Sometimes I do not want to access just one key.

Instead, I want to read all the information stored inside the dictionary.

A loop can automatically traverse through all key-value pairs.

---

## Real Life Example: Student Record

Imagine a student record.

```text
Student
│
├── Name       → Lakshaga
├── Age        → 30
├── Department → Computer Science
└── City       → Salem
```

This is a dictionary.

Suppose I want to read the entire record.

I could manually read:

```text
Name       → Lakshaga
Age        → 30
Department → Computer Science
City       → Salem
```

But for large records, this becomes repetitive.

---

## The Smart Way (Using a Loop)

Instead of reading each field manually, I can tell the loop:

> Read every key-value pair in the student record.

The loop performs the repetition automatically.

---

## Python Idea

```python
student = {
    "name": "Lakshaga",
    "age": 30,
    "department": "Computer Science",
    "city": "Salem"
}

for key, value in student.items():
    print(key, "→", value)
```

---

## Output

```text
name → Lakshaga
age → 30
department → Computer Science
city → Salem
```

---

## Understanding What Happens

### Step 1

```text
key = name
value = Lakshaga
```

Output:

```text
name → Lakshaga
```

---

### Step 2

```text
key = age
value = 30
```

Output:

```text
age → 30
```

---

### Step 3

```text
key = department
value = Computer Science
```

Output:

```text
department → Computer Science
```

---

### Step 4

```text
key = city
value = Salem
```

Output:

```text
city → Salem
```

---

## Programming Team Model

### Dictionary

Stores the student record.

```text
Student
│
├── Name
├── Age
├── Department
└── City
```

---

### Worker 1 - Traversal

Visits each key-value pair one by one.

```text
Name
 ↓
Age
 ↓
Department
 ↓
City
```

---

### Worker 2 - Processing

Reads the current key and value.

Example:

```text
Name → Lakshaga
```

---

### Worker 3 - Automatic Repetition

Repeats the process for all remaining key-value pairs.

---

## Important Concept

A dictionary contains:

```text
Key → Value
```

Example:

```text
Name → Lakshaga
```

During looping:

```text
key = Name

value = Lakshaga
```

The loop automatically moves through every pair.

---

## List vs Dictionary Loop

### List Loop

```python
fruits = ["Apple", "Mango", "Orange"]

for fruit in fruits:
    print(fruit)
```

Traversal:

```text
Apple
 ↓
Mango
 ↓
Orange
```

---

### Dictionary Loop

```python
for key, value in student.items():
    print(key, value)
```

Traversal:

```text
Name → Lakshaga
 ↓
Age → 30
 ↓
Department → Computer Science
 ↓
City → Salem
```

---

## Key Understanding

A list stores items by position.

A dictionary stores information by labels (keys).

A loop can automatically traverse through every key-value pair and process the information.

This allows complete records to be read without manually accessing each field.

---

## My Thought

Now I understand that a dictionary is like a large labeled container holding multiple key-value pairs. A loop can automatically traverse through the entire record. Worker 1 visits each key-value pair, Worker 2 reads the information, and Worker 3 repeats the process until all information in the dictionary has been processed.
