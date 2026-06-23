# Day 5 - IF / ELSE (Decision Making)

## What Did I Learn Today?

On Day 4, I learned how programs communicate with users through Input and Output.

Today I learned that programs can make decisions.

A program does not always perform the same action.

It can choose different actions based on conditions.

This is called **Decision Making**.

---

## What Is Decision Making?

Decision making means choosing between different actions based on a condition.

In real life, humans make decisions every day.

Examples:

- If it is raining, carry an umbrella.
- If the traffic signal is green, move forward.
- If a student passes the exam, promote to the next class.

Programs can also make similar decisions.

---

## Real-Life Example: ATM

When using an ATM:

```text
Enter PIN
      ↓
Is PIN Correct?
      ↓
Yes → Allow Access
No  → Deny Access
```

The ATM follows rules created by programmers.

It does not think like a human.

It simply checks whether the condition is True or False.

---

## Real-Life Example: Mobile Phone

When unlocking a phone:

```text
Scan Fingerprint
        ↓
Fingerprint Matches?
        ↓
Yes → Unlock Phone
No  → Reject Access
```

The phone is making a decision based on a condition.

---

## Decision Making in Python

Python uses `if` and `else` for decision making.

```python
if condition:
    do something
else:
    do something else
```

The program checks the condition.

- If the condition is True, the `if` block runs.
- If the condition is False, the `else` block runs.

---

## Simple Example

```python
age = 20

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

### Output

```text
Adult
```

The condition:

```python
age >= 18
```

evaluates to True.

Therefore, Python prints:

```text
Adult
```

---

## Tea Shop Example

Suppose a tea shop gives a discount for large orders.

```python
tea_count = 6

if tea_count >= 5:
    print("Discount Applied")
else:
    print("No Discount")
```

### Output

```text
Discount Applied
```

The program checks the condition and decides which message to display.

---

## Why Is This Important?

Without decision making, programs would always perform the same action.

Example:

```python
print("Access Granted")
```

This would grant access to everyone.

Decision making allows programs to enforce rules.

Example:

```python
pin_correct = False

if pin_correct:
    print("Access Granted")
else:
    print("Access Denied")
```

Now the program behaves differently based on the condition.

---

## Understanding Conditions

A condition produces either:

```text
True
```

or

```text
False
```

Examples:

```python
10 > 5
```

Result:

```text
True
```

Example:

```python
10 < 5
```

Result:

```text
False
```

Programs use these True/False values to make decisions.

---

## Common Comparison Operators

### Equal To (==)

```python
a == b
```

Checks whether two values are equal.

---

### Not Equal To (!=)

```python
a != b
```

Checks whether two values are different.

---

### Greater Than (>)

```python
a > b
```

Checks whether the left value is larger.

---

### Less Than (<)

```python
a < b
```

Checks whether the left value is smaller.

---

### Greater Than or Equal To (>=)

```python
a >= b
```

Checks whether the left value is larger or equal.

---

### Less Than or Equal To (<=)

```python
a <= b
```

Checks whether the left value is smaller or equal.

---

## Rules for Computers

Humans create rules.

Programs follow those rules.

For example:

```text
Rule:
If age is 18 or above,
allow voting.
```

Python version:

```python
age = 20

if age >= 18:
    print("Eligible to Vote")
else:
    print("Not Eligible")
```

The computer does not decide the rule.

The programmer decides the rule.

The computer only follows it.

---

## Decision Flow

A common programming pattern is:

```text
Input
   ↓
Check Condition
   ↓
True or False
   ↓
Choose Action
   ↓
Output
```

Example:

```python
age = 20

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

---

## Connecting Day 1, Day 2, Day 3, Day 4, and Day 5

### Day 1

Instructions tell the computer what to do.

```text
Follow steps
```

### Day 2

Variables store information.

```python
age = 20
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

Now programming is not only storing, processing, and communicating information.

It is also making choices based on rules.

---

## My Thought

Today I learned that computers can make decisions using conditions.

The computer does not think like a human.

Instead, programmers define rules and conditions.

The computer simply checks whether those conditions are True or False and performs the appropriate action.

Just like Terms and Conditions guide people, conditions guide computer programs.

---

## What I Learned Today

- Programs can make decisions.
- Python uses `if` and `else` for decision making.
- Conditions evaluate to True or False.
- Comparison operators help create conditions.
- Programmers define the rules.
- Computers follow the rules exactly.

### Programming Rule #5

**Input → Condition → Decision → Output**

Programs become intelligent when they can choose actions based on rules and conditions.
