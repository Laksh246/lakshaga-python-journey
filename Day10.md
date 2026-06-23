# Day 10 - Lists (Fridge Example)

## What Did I Learn Today?

On Day 9, I learned that functions can receive inputs using parameters and arguments.

Today I learned about **Lists**.

A list allows us to store multiple related items together in a single container.

Instead of creating many separate variables, we can organize everything inside one list.

---

## Why Do We Need Lists?

Suppose I want to store items in a fridge.

Without a list:

```python
item1 = "milk"
item2 = "eggs"
item3 = "vegetables"
item4 = "fruits"
```

This works for a few items.

But what if the fridge contains:

- 20 items
- 50 items
- 100 items

Creating separate variables becomes difficult.

Lists solve this problem.

---

# Real Life Example: Fridge

A fridge stores many items together in one place:

- milk
- eggs
- vegetables
- fruits

Instead of keeping items separately, everything is stored inside one fridge.

In programming, this fridge is called a **List**.

---

## Creating a List

Python uses square brackets.

```python
fridge = ["milk", "eggs", "vegetables", "fruits"]
```

The entire collection is stored in one variable.

---

## Understanding the List

```text
fridge
│
├── milk
├── eggs
├── vegetables
└── fruits
```

The variable `fridge` stores multiple values together.

---

## Accessing Items in a List

Each item has a position called an **Index**.

Python starts counting from **0**.

```python
fridge = ["milk", "eggs", "vegetables", "fruits"]

print(fridge[0])
print(fridge[1])
print(fridge[2])
print(fridge[3])
```

Output:

```text
milk
eggs
vegetables
fruits
```

---

## Why Does Index Start at 0?

Python counts positions like this:

```text
Position    Item

0           milk
1           eggs
2           vegetables
3           fruits
```

The first item is always at position 0.

This is called **Zero-Based Indexing**.

---

## Fridge Thinking

```text
List = Fridge

Items = Things Stored Inside

Index = Position of Items
```

Real life:

```text
Open Fridge
      ↓
Find Position
      ↓
Pick Item
      ↓
Close Fridge
```

Programming:

```python
print(fridge[1])
```

Output:

```text
eggs
```

---

## Why Is This Important?

Imagine storing student names.

Without a list:

```python
student1 = "Arun"
student2 = "Priya"
student3 = "Rahul"
student4 = "Meena"
```

With a list:

```python
students = ["Arun", "Priya", "Rahul", "Meena"]
```

Much cleaner and easier to manage.

---

## Lists and Loops

Lists become very powerful when combined with loops.

Example:

```python
fridge = ["milk", "eggs", "vegetables", "fruits"]

for item in fridge:
    print(item)
```

Output:

```text
milk
eggs
vegetables
fruits
```

The loop automatically visits every item.

---

## Can a List Store Different Data Types?

Yes.

Python lists can store multiple data types together.

Example:

```python
mixed_data = [
    "Lakshaga",
    30,
    72.5,
    True
]
```

Here:

```text
"Lakshaga" → String
30         → Integer
72.5       → Float
True       → Boolean
```

All these values can exist inside the same list.

---

## Real-Life Fridge Example

Just like a real fridge can contain different kinds of items:

```text
Milk Packet
12 Eggs
2.5 Liters Juice
Ice Available (True)
```

A Python list can also store different types of information together.

Example:

```python
fridge = [
    "milk",
    12,
    2.5,
    True
]
```

Python allows mixed data types inside a list.

---

## Understanding the Loop Variable

Consider this example:

```python
fridge = ["milk", "eggs", "fruits"]

for item in fridge:
    print(item)
```

A common question is:

```text
Where did "item" come from?
```

We never created it before.

---

## Python Creates the Loop Variable Automatically

During each repetition, Python automatically creates and updates the variable.

Thinking:

```text
Take first item from fridge
Store in item
Print item

Take next item from fridge
Store in item
Print item

Take next item from fridge
Store in item
Print item
```

---

### Iteration 1

```python
item = "milk"
print(item)
```

Output:

```text
milk
```

---

### Iteration 2

```python
item = "eggs"
print(item)
```

Output:

```text
eggs
```

---

### Iteration 3

```python
item = "fruits"
print(item)
```

Output:

```text
fruits
```

---

## Is "item" a Special Keyword?

No.

It is simply a variable name chosen by the programmer.

These are all valid:

```python
for item in fridge:
    print(item)
```

```python
for food in fridge:
    print(food)
```

```python
for x in fridge:
    print(x)
```

```python
for anything in fridge:
    print(anything)
```

Python does not care about the name.

The programmer chooses it.

---

## Why Is "item" Commonly Used?

Because it reads naturally.

```python
for item in fridge:
```

can be understood as:

```text
For each item in the fridge
```

which makes the code easier to read.

---

## Day 10 Insight

```text
A list can store multiple data types in Python.

The variable used in a for loop is called a loop variable.

Python automatically creates and updates this variable during each iteration.

The loop variable does not need to be declared beforehand.
```
---
## Lists and Functions

Functions can work with lists.

Example:

```python
def show_items(items):

    for item in items:
        print(item)
```

Function call:

```python
show_items(["milk", "eggs", "fruits"])
```

Output:

```text
milk
eggs
fruits
```

Now a function can process many values at once.

---

## Adding New Items

A fridge can receive new items.

Lists can too.

Example:

```python
fridge = ["milk", "eggs"]

fridge.append("fruits")
```

Now:

```text
milk
eggs
fruits
```

The list grows.

---

## Removing Items

Suppose the milk is finished.

```python
fridge.remove("milk")
```

Now:

```text
eggs
fruits
```

The item is removed.

---

## List Thinking

Without Lists:

```text
One Variable
One Value
```

With Lists:

```text
One Variable
Many Values
```

This is the biggest advantage of lists.

---
## Common List Operations

Lists are not just for storing items.

We can also modify, search, count, and organize data inside a list.

---

### 1. Add an Item (append)

Adds a new item to the end of the list.

```python
fridge = ["milk", "eggs"]

fridge.append("fruits")

print(fridge)
```

Output:

```text
['milk', 'eggs', 'fruits']
```

---

### 2. Remove an Item (remove)

Removes a specific item.

```python
fridge = ["milk", "eggs", "fruits"]

fridge.remove("eggs")

print(fridge)
```

Output:

```text
['milk', 'fruits']
```

---

### 3. Find Number of Items (len)

Counts how many items are stored.

```python
fridge = ["milk", "eggs", "fruits"]

print(len(fridge))
```

Output:

```text
3
```

Thinking:

```text
How many items are inside the fridge?
```

---

### 4. Check Whether an Item Exists (in)

```python
fridge = ["milk", "eggs", "fruits"]

print("milk" in fridge)
```

Output:

```text
True
```

Thinking:

```text
Is milk inside the fridge?
```

---

### 5. Update an Item

Replace an existing item using its index.

```python
fridge = ["milk", "eggs", "fruits"]

fridge[1] = "bread"

print(fridge)
```

Output:

```text
['milk', 'bread', 'fruits']
```

Thinking:

```text
Remove eggs and place bread in the same position.
```

---

### 6. Access the Last Item

```python
fridge = ["milk", "eggs", "fruits"]

print(fridge[-1])
```

Output:

```text
fruits
```

Python counts backwards using negative indexes.

```text
-1 → Last item
-2 → Second last item
-3 → Third last item
```

---

### 7. Sort Items

```python
fruits = ["mango", "apple", "banana"]

fruits.sort()

print(fruits)
```

Output:

```text
['apple', 'banana', 'mango']
```

Thinking:

```text
Arrange items alphabetically.
```

---

### 8. Reverse a List

```python
fruits = ["apple", "banana", "mango"]

fruits.reverse()

print(fruits)
```

Output:

```text
['mango', 'banana', 'apple']
```

---

### 9. Clear the Entire List

```python
fridge = ["milk", "eggs", "fruits"]

fridge.clear()

print(fridge)
```

Output:

```text
[]
```

Thinking:

```text
Empty the entire fridge.
```

---

## List Operations Summary

| Operation | Purpose |
|------------|---------|
| append() | Add item |
| remove() | Remove item |
| len() | Count items |
| in | Check existence |
| list[index] | Access item |
| list[index] = value | Update item |
| sort() | Arrange items |
| reverse() | Reverse order |
| clear() | Remove all items |

---

## Fridge Analogy Summary

```text
Fridge                Python List

Store items           List
Add item              append()
Remove item           remove()
Count items           len()
Check item exists     in
Replace item          index assignment
Arrange items         sort()
Empty fridge          clear()
```
---

## Connecting Day 1 to Day 10

### Day 1

Instructions tell the computer what to do.

```text
Follow steps
```

### Day 2

Variables store information.

```python
name = "Lakshaga"
```

### Day 3

Variables process information.

```python
total = a + b
```

### Day 4

Programs interact with users.

```python
name = input("Enter your name: ")
```

### Day 5

Programs make decisions.

```python
if age >= 18:
    print("Adult")
```

### Day 6

Programs repeat actions a fixed number of times.

```python
for day in range(7):
    print("Brush Teeth")
```

### Day 7

Programs repeat until a condition changes.

```python
while battery < 100:
    battery += 10
```

### Day 8

Programs organize reusable actions into functions.

```python
def greet():
    print("Hello")
```

### Day 9

Functions receive inputs through parameters and arguments.

```python
def greet(name):
    print("Hello", name)
```

### Day 10

Programs store multiple values together using lists.

```python
fridge = ["milk", "eggs", "vegetables", "fruits"]
```

Now programming is not only storing, processing, communicating, deciding, repeating, and organizing actions.

It can also organize collections of related data.

---

## My Thought

Today I learned that a list is like a fridge.

Instead of creating separate variables for every item, multiple items can be stored together in one container.

Each item has a position called an index, which helps us access specific items when needed.

Lists make programs cleaner, more organized, and easier to manage.

---

## What I Learned Today

- Lists store multiple values in one place.
- Lists use square brackets `[]`.
- Each item has an index position.
- Index starts at 0.
- Items can be accessed using indexes.
- Lists work well with loops and functions.
- Items can be added or removed from a list.

### Programming Rule #10

**One Variable → Many Values**

Lists help organize related information inside a single container.
