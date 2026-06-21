# Day 17 - Return Values (Getting Results Back from a Function)

## What I Learned

A function can do more than perform an action.

A function can also send a result back to the place where it was called.

This is called a **return value**.

Without a return value, a function only performs a task.

With a return value, a function can produce a result that can be used later.

---

## Real Life Example: Juice Machine

Imagine a juice machine.

### Inputs

- Apples
- Water
- Sugar

---

### Processing

The machine:

- Washes apples
- Crushes apples
- Mixes ingredients

---

### Output

The machine produces:

```text
Apple Juice
```

The juice comes out of the machine and can be used.

This is similar to a function returning a value.

---

## Function as a Machine

```text
Inputs
   ↓
Function
   ↓
Processing
   ↓
Return Result
```

---

## Python Idea

```python
def make_juice():
    return "Apple Juice"

juice = make_juice()

print(juice)
```

Output:

```text
Apple Juice
```

---

## What Happens Here?

Step 1:

The function creates a result.

```python
return "Apple Juice"
```

---

Step 2:

The result leaves the function.

---

Step 3:

The result is stored.

```python
juice = make_juice()
```

---

Step 4:

The stored result can be used later.

```python
print(juice)
```

---

## Print vs Return

### Print

Shows information on the screen.

```python
def greet():
    print("Hello")
```

Output:

```text
Hello
```

After displaying it, the value is not available for reuse.

---

### Return

Sends information back.

```python
def greet():
    return "Hello"
```

Now the result can be stored and reused.

```python
message = greet()
```

---

## Real Life Understanding

### Print

Like a teacher making an announcement.

```text
"Class starts at 9 AM."
```

Everyone hears it.

Nothing is handed back.

---

### Return

Like a shop giving a bill after purchase.

```text
Purchase
   ↓
Bill Returned
```

The bill can be saved and used later.

---

## Function with Input and Return

```python
def make_juice(fruit):
    return fruit + " Juice"

drink = make_juice("Mango")

print(drink)
```

Output:

```text
Mango Juice
```

---

## Programming Team Model

### Input Supplier

Provides information.

Example:

```text
Mango
```

---

### Function Machine

Processes the information.

---

### Return Gate

Sends the final result back.

```text
Result Returned
```

---

## Important Concept

A function can:

### Perform an Action

```python
print("Hello")
```

or

### Return a Result

```python
return "Hello"
```

Returning is more powerful because the result can be stored, reused, and processed further.

---

## Key Understanding

Without return:

```text
Input
  ↓
Function
  ↓
Display Result
```

With return:

```text
Input
  ↓
Function
  ↓
Return Result
  ↓
Store and Reuse
```

---

## My Thought

Now I understand that a return value is like receiving the final product from a machine. The function performs processing and then sends the result back. Unlike print, which only displays information, return allows the result to be stored, reused, and passed to other parts of the program. This makes functions much more useful and flexible.
