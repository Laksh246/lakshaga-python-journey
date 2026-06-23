# Day 8 - Functions (Reusable Actions)

## What Did I Learn Today?

On Day 7, I learned that loops help programs repeat actions automatically.

Today I learned about **Functions**.

Functions help us group multiple instructions into a single reusable block.

Instead of writing the same code again and again, we can place it inside a function and call it whenever needed.

A function is like creating our own command.

---

## What Is a Function?

A function is a reusable block of code that performs a specific task.

Think of it as:

```text
Give a name
      ↓
Store multiple steps
      ↓
Run whenever needed
```

Instead of repeating instructions many times, we write them once inside a function.

---

## Real-Life Example: Coffee Machine

Imagine a coffee machine.

You press:

```text
Make Coffee
```

But internally the machine performs many steps:

```text
Boil Water
Add Coffee Powder
Mix Ingredients
Prepare Coffee
Serve Coffee
```

You do not manually perform every step.

One button starts the entire process.

This is similar to a function.

---

## Real-Life Example: Mobile Photo Capture

You open your phone camera and press:

```text
Take Photo
```

What actually happens?

```text
Open Lens
Adjust Focus
Capture Image
Save File
Show Preview
```

The phone performs many hidden steps automatically.

You only see:

```text
Take Photo
```

This is exactly how a function works.

One function can contain many instructions.

---

## Why Do We Need Functions?

Without functions:

```python
print("Opening camera")
print("Focusing lens")
print("Capturing image")
print("Saving photo")
```

If we need the same process again, we must rewrite all the steps.

---

With functions:

```python
def take_photo():
    print("Opening camera")
    print("Focusing lens")
    print("Capturing image")
    print("Saving photo")
```

Now we can simply call:

```python
take_photo()
```

The stored instructions execute automatically.

---

## Creating a Function

Python uses the `def` keyword.

Example:

```python
def greet():
    print("Hello")
```

This creates a function.

Nothing happens yet.

The function is only stored in memory.

---

## Calling a Function

To run the function:

```python
greet()
```

Output:

```text
Hello
```

Creating a function and running a function are two different things.

---

## Complete Example

```python
def take_photo():
    print("Opening camera")
    print("Focusing lens")
    print("Capturing image")
    print("Saving photo")

take_photo()
```

### Output

```text
Opening camera
Focusing lens
Capturing image
Saving photo
```

The computer executes every instruction inside the function.

---

## Tea Shop Example

Suppose customers repeatedly order tea.

Without a function:

```python
print("Boil Water")
print("Add Tea Powder")
print("Add Milk")
print("Serve Tea")
```

Again:

```python
print("Boil Water")
print("Add Tea Powder")
print("Add Milk")
print("Serve Tea")
```

This creates duplicate code.

---

With a function:

```python
def make_tea():
    print("Boil Water")
    print("Add Tea Powder")
    print("Add Milk")
    print("Serve Tea")
```

Now:

```python
make_tea()
make_tea()
```

The same instructions can be reused.

---

## A Common Confusion: Why Use print() Inside Functions?

When I first learned functions, I noticed many examples used `print()`.

This made me wonder:

```text
Is a function just a collection of print statements?
```

The answer is:

```text
No.
```

A function is a collection of instructions.

`print()` is only one type of instruction.

---

## What Does print() Actually Do?

The purpose of `print()` is:

```text
Display information to the user.
```

Example:

```python
print("Hello")
```

The computer performs the instruction:

```text
Show the text "Hello" on the screen.
```

So `print()` itself is an instruction, but its job is only to display information.

---

## Instructions Without print()

Many instructions do not display anything.

Example:

```python
age = 25
```

The computer performs:

```text
Create a variable called age
Store the value 25
```

Nothing appears on the screen.

---

Another example:

```python
total = 10 + 5
```

The computer performs:

```text
Add 10 and 5
Store the result in total
```

Again, nothing is displayed.

---

## Functions Do Not Need print()

Example:

```python
def calculate_total():
    price = 10
    quantity = 5
    total = price * quantity
```

This function contains instructions.

When called:

```python
calculate_total()
```

The computer executes the instructions.

But no output appears because there is no `print()` statement.

---

## Why Do Learning Examples Use print()?

When learning programming, `print()` helps us see what the computer is doing.

Example:

```python
def make_tea():
    print("Boil Water")
    print("Add Tea Powder")
    print("Add Milk")
    print("Serve Tea")
```

Output:

```text
Boil Water
Add Tea Powder
Add Milk
Serve Tea
```

The computer is not actually making tea.

The messages simply help us visualize the steps.

---

## Real Programs Use Actual Actions

Learning version:

```python
def take_photo():
    print("Opening Camera")
    print("Capturing Image")
```

Real mobile app logic:

```python
def take_photo():
    open_camera()
    focus_lens()
    capture_image()
    save_photo()
```

Here the function performs actions instead of displaying messages.

---

## Better Understanding of Functions

A function is not:

```text
A collection of print statements
```

A function is:

```text
A collection of instructions stored under a name
```

Those instructions can:

- Display information
- Store data
- Perform calculations
- Make decisions
- Repeat tasks
- Call other functions

---

## Function Thinking

Instead of thinking:

```text
Functions print things
```

Think:

```text
Functions perform tasks
```

Sometimes the task includes displaying information.

Sometimes the task performs calculations, processing, or other actions without displaying anything.

---

## Day 8 Insight

```text
A function is a reusable block of instructions.

print() is only one type of instruction used to display information.

Functions can perform many kinds of tasks, even when nothing is displayed on the screen.
```

## Functions and Loops

Functions work well with loops.

Example:

```python
def greet():
    print("Welcome")

for i in range(3):
    greet()
```

Output:

```text
Welcome
Welcome
Welcome
```

The loop repeats the function call.

---

## Functions and Decision Making

Functions can also work with conditions.

Example:

```python
def access_granted():
    print("Access Granted")

age = 20

if age >= 18:
    access_granted()
```

Output:

```text
Access Granted
```

Functions help organize code.

---

## Why Is This Important?

As programs grow larger:

- Code becomes longer
- Repetition increases
- Maintenance becomes difficult

Functions solve this problem.

They help:

- Reuse code
- Organize code
- Reduce repetition
- Improve readability

---

## Function Thinking

Instead of thinking:

```text
Write all steps again
```

Think:

```text
Create once
Reuse many times
```

This is the main purpose of functions.

---

## Connecting Day 1 to Day 8

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
    battery = battery + 10
```

### Day 8

Programs organize reusable actions into functions.

```python
def greet():
    print("Hello")
```

Now programming is not only storing, processing, communicating, deciding, and repeating.

It is also organizing tasks into reusable building blocks.

---


## My Thought

Today I learned that functions help avoid repeating the same code again and again.

A function is like a mobile app button that hides complex steps and produces a result.

Functions make programs cleaner, easier to understand, and easier to maintain.

---

## What I Learned Today

- Functions are reusable blocks of code.
- Python uses the `def` keyword to create functions.
- Functions must be called to execute.
- Functions reduce repetition.
- Functions help organize programs.
- Functions can work with loops and conditions.

### Programming Rule #8

**Create Once → Reuse Many Times**

Functions allow programmers to group instructions into reusable building blocks.
