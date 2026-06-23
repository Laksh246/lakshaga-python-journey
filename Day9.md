# Day 9 - Functions with Input (Parameters & Arguments)

## What Did I Learn Today?

On Day 8, I learned that functions help us group instructions into reusable blocks.

Today I learned that functions can also receive information from outside.

This makes functions more flexible and reusable.

Instead of performing the same task every time, a function can produce different results based on the values it receives.

---

## Why Do We Need Inputs in Functions?

Consider a camera app.

If the camera always took photos in only one mode:

```text
Portrait Mode
Flash Off
Beauty Filter
```

Every photo would be identical.

That would not be very useful.

Instead, users choose options before taking a photo.

These options are sent to the camera system.

Functions work the same way.

---

# Real Life Example: Mobile Camera

When I open my mobile camera, I can choose:

- Mode → Selfie / Portrait / Night
- Flash → On / Off
- Filter → Beauty / Black & White

These options influence the final photo.

The camera system receives the selected values and performs its task.

Functions receive values in a similar way.

---

## Understanding Parameters

Parameters are variables created inside a function definition.

Think of them as empty slots waiting for values.

Example:

```python
def take_photo(mode, flash, filter):
    print(mode)
    print(flash)
    print(filter)
```

Here:

```text
mode
flash
filter
```

are parameters.

They are placeholders.

No actual values exist yet.

---

## Understanding Arguments

Arguments are the real values supplied when calling the function.

Example:

```python
take_photo("portrait", "off", "beauty")
```

Here:

```text
"portrait"
"off"
"beauty"
```

are arguments.

These values fill the parameter slots.

---

## Complete Camera Flow

### Function Definition

```python
def take_photo(mode, flash, filter):
    print("Mode:", mode)
    print("Flash:", flash)
    print("Filter:", filter)
```

### Function Call

```python
take_photo("portrait", "off", "beauty")
```

### Output

```text
Mode: portrait
Flash: off
Filter: beauty
```

The function receives values and performs actions using them.

---

## Parameters vs Arguments

| Parameters | Arguments |
|------------|------------|
| Empty slots | Actual values |
| Created in function definition | Supplied during function call |
| Placeholder variables | Real data |
| Design stage | Usage stage |

---

## Coffee Machine Example

Imagine a coffee machine.

The machine is designed with options:

```text
Sugar Level
Milk Level
Coffee Strength
```

These are like parameters.

---

Customer chooses:

```text
2 Spoons Sugar
Full Milk
Strong Coffee
```

These are like arguments.

---

The machine receives the selections and prepares coffee.

Programming works the same way.

---

## Tea Shop Example

Without parameters:

```python
def make_tea():
    print("Tea Prepared")
```

The same tea is prepared every time.

---

With parameters:

```python
def make_tea(sugar):
    print("Sugar:", sugar)
```

Function calls:

```python
make_tea(1)
make_tea(2)
make_tea(3)
```

Output:

```text
Sugar: 1
Sugar: 2
Sugar: 3
```

Now the function can produce different results.

---

## Why Is This Important?

Without parameters:

```python
def greet():
    print("Hello Lakshaga")
```

Only one person can be greeted.

---

With parameters:

```python
def greet(name):
    print("Hello", name)
```

Now:

```python
greet("Lakshaga")
greet("Priya")
greet("Arun")
```

Output:

```text
Hello Lakshaga
Hello Priya
Hello Arun
```

The same function works for everyone.

---

## Functions Become Flexible

Without parameters:

```text
One Function
One Result
```

With parameters:

```text
One Function
Many Possible Results
```

This makes functions reusable and powerful.

---

## Function Flow

A common function pattern is:

```text
Create Function
       ↓
Define Parameters
       ↓
Call Function
       ↓
Pass Arguments
       ↓
Function Receives Values
       ↓
Perform Task
       ↓
Produce Output
```

---

## Connecting Day 1 to Day 9

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

Functions can receive values and produce different results.

```python
def greet(name):
    print("Hello", name)
```

Now programming is not only storing, processing, communicating, deciding, repeating, and organizing tasks.

Functions can also adapt their behavior based on input values.

---

## My Thought

Today I learned that functions work like a mobile camera.

Parameters define the available options.

Arguments are the actual choices selected by the user.

The same function can produce different results depending on the values it receives.

This makes programs flexible and reusable.

---

## What I Learned Today

- Functions can receive inputs.
- Parameters are placeholders inside functions.
- Arguments are actual values supplied to functions.
- Parameters receive arguments.
- One function can produce different results using different inputs.
- Functions become more reusable and flexible with parameters.

### Programming Rule #9

**Define Once → Accept Inputs → Produce Different Results**

Parameters and arguments allow one function to handle many situations without rewriting code.
