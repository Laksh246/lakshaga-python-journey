# Day 7 - While Loop (Real-Life Understanding)

## What Did I Learn Today?

On Day 6, I learned that loops help repeat actions automatically.

Today I learned about a special type of loop called the **while loop**.

A while loop repeats actions as long as a condition remains True.

Unlike a `for` loop, where we know the number of repetitions in advance, a `while` loop continues until a condition changes.

---

## What Is a While Loop?

A while loop keeps repeating a task as long as a condition is True.

```text
Check Condition
       ↓
Condition True?
       ↓
      Yes
       ↓
 Perform Action
       ↓
Check Condition Again
```

When the condition becomes False, the loop stops.

---

## Real-Life Example: Phone Charging

When my phone battery is low, I plug in the charger.

The phone keeps charging until the battery reaches 100%.

### Thinking Like a Loop

```text
Battery = 10%
      ↓
Charging...
      ↓
Battery = 20%
      ↓
Charging...
      ↓
Battery = 30%
      ↓
...
      ↓
Battery = 100%
      ↓
Stop Charging
```

The action repeats while the battery is below 100%.

---

## Python Idea

```python
battery = 10

while battery < 100:
    print("Charging...")
    battery = battery + 10
```

### Output

```text
Charging...
Charging...
Charging...
Charging...
Charging...
Charging...
Charging...
Charging...
Charging...
```

The loop stops when the battery reaches 100%.

---

## Real-Life Example: Filling a Water Tank

Imagine filling a water tank.

```text
Tank Level = 0%
       ↓
Keep Filling
       ↓
Tank Level = 100%
       ↓
Stop Filling
```

The filling process continues while the tank is not full.

This is another example of a while loop.

---

## Real-Life Example: Studying for an Exam

```text
While syllabus is not completed:
    Keep Studying
```

Once the syllabus is completed, the studying loop stops.

---

## Why Do We Need While Loops?

Sometimes we do not know how many times an action must repeat.

Example:

```text
Keep entering password until correct.
```

We do not know whether the user will enter the correct password in:

- 1 attempt
- 2 attempts
- 5 attempts

A while loop is useful in such situations.

---

## Password Example

```python
password = ""

while password != "python":
    password = input("Enter Password: ")

print("Access Granted")
```

### Sample Execution

```text
Enter Password: abc
Enter Password: 123
Enter Password: python

Access Granted
```

The loop continues until the correct password is entered.

---

## Understanding the Condition

A while loop depends on a condition.

Example:

```python
battery < 100
```

This condition can be:

```text
True
```

or

```text
False
```

As long as it remains True, the loop continues.

When it becomes False, the loop stops.

---

## Important Rule

The condition inside a while loop must eventually become False.

Otherwise, the loop will never stop.

Example:

```python
count = 1

while count <= 5:
    print(count)
    count = count + 1
```

Output:

```text
1
2
3
4
5
```

The variable changes and eventually stops the loop.

---

## Infinite Loop Example

```python
while True:
    print("Hello")
```

This loop never stops because the condition is always True.

This is called an **Infinite Loop**.

Programmers must be careful when using while loops.

---

## For Loop vs While Loop

### For Loop

Used when the number of repetitions is known.

```python
for day in range(7):
    print("Brush Teeth")
```

Example:

```text
Repeat exactly 7 times
```

---

### While Loop

Used when repetitions depend on a condition.

```python
battery = 10

while battery < 100:
    print("Charging...")
    battery = battery + 10
```

Example:

```text
Repeat until battery reaches 100%
```

---

## Repetition Flow

A common while-loop pattern is:

```text
Start
  ↓
Check Condition
  ↓
Condition True?
  ↓
Perform Action
  ↓
Update Variable
  ↓
Check Again
  ↓
Stop When False
```

---

## Why Is This Important?

Many real-world systems use while loops.

Examples:

- Phone charging
- ATM PIN verification
- Login systems
- Download progress
- Water tank filling
- Game loops

These systems continue working until a condition changes.

---

## Revisiting the For Loop

On Day 6, I learned about the `for` loop.

A `for` loop is used when we know in advance how many times a task should repeat.

Example:

```python
for day in range(7):
    print("Brush Teeth")
```

Output:

```text
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
Brush Teeth
```

Here we know exactly how many times the action should repeat.

The loop runs 7 times and then stops automatically.

---

## When Is a For Loop Useful?

Use a `for` loop when:

- Number of repetitions is known
- Repeating a fixed number of times
- Counting items

Examples:

```text
Repeat 5 times
Repeat 10 times
Print numbers from 1 to 100
```

---

## When Is a While Loop Useful?

Use a `while` loop when:

- Number of repetitions is unknown
- Repetition depends on a condition
- The program should continue until a goal is reached

Examples:

```text
Keep charging until battery reaches 100%
Keep asking for password until correct
Keep filling water tank until full
```

---

## For Loop vs While Loop

### For Loop

```python
for day in range(7):
    print("Brush Teeth")
```

Thinking:

```text
Repeat exactly 7 times
```

---

### While Loop

```python
battery = 10

while battery < 100:
    print("Charging...")
    battery = battery + 10
```

Thinking:

```text
Repeat until battery becomes 100%
```

---

## Simple Rule

### For Loop

```text
I know how many times to repeat.
```

Use:

```python
for
```

### While Loop

```text
I don't know how many times to repeat.
I only know the stopping condition.
```

Use:

```python
while
```
---

## Connecting Day 1 to Day 7

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
else:
    print("Minor")
```

### Day 6

Programs repeat actions a fixed number of times.

```python
for day in range(7):
    print("Brush Teeth")
```

### Day 7

Programs repeat actions until a condition changes.

```python
while battery < 100:
    print("Charging...")
```

Now programming is not only storing, processing, communicating, deciding, and repeating.

It can continue working dynamically until a goal is reached.

---

## My Thought

Today I learned that while loops are useful when we do not know in advance how many times a task must repeat.

The loop keeps running as long as a condition is True.

Many real-world systems work this way.

For example, phone charging, login systems, and ATM verification continue until a specific condition is satisfied.

---

If repetition is controlled by a fixed count
3 attempts
5 questions
10 students
7 days
Use:
```python
for
```
If repetition is controlled by a condition
Until battery reaches 100%
Until password is correct
Until water tank is full
Until user exits
Use:
```python
while
```
### Programming Rule

## FOR Loop
---------
Known number of repetitions (count)

## WHILE Loop
-----------
Unknown number of repetitions
Condition decides when to stop 

---

## What I Learned Today

- A while loop repeats while a condition is True.
- The loop stops when the condition becomes False.
- While loops are useful when the number of repetitions is unknown.
- Conditions control the execution of a while loop.
- Variables often change inside the loop.
- Infinite loops occur when conditions never become False.

### Programming Rule #7

**Check Condition → Repeat Action → Update → Stop**

While loops allow programs to continue working until a specific goal or condition is reached.
