# Day 15 - Nested if (Multiple Decision Gates)

## What I Learned

Sometimes a single decision is not enough.

A program may need to pass through multiple decision gates before an action can be performed.

This is called a **nested if**.

A nested if means:

> One condition must be satisfied before the next condition is checked.

---

## Real Life Example: Library Book Borrowing

Imagine a student wants to borrow a book from a library.

The student must pass through multiple gates.

### Gate 1

Is the student a library member?

### Gate 2

Does the student have any overdue books?

### Gate 3

Is the requested book available?

Only if all gates approve can the student borrow the book.

---

## Decision Flow

```text
Gate 1: Library Member?
        │
     ┌──┴──┐
    No    Yes
    │       │
 Reject     ▼
       Gate 2: Overdue Books?
              │
           ┌──┴──┐
          Yes   No
          │      │
       Reject    ▼
          Gate 3: Book Available?
                 │
              ┌──┴──┐
             No    Yes
             │       │
          Reject   Allow Borrowing
```

---

## Python Idea

```python
member = True
overdue = False
available = True

if member:
    if not overdue:
        if available:
            print("Borrow Allowed")
```

---

## Understanding the Gates

### Gate 1

Checks:

> Is the student a library member?

If NO:

```text
Reject
```

The process stops.

---

### Gate 2

Checks:

> Does the student have overdue books?

If YES:

```text
Reject
```

The process stops.

---

### Gate 3

Checks:

> Is the book available?

If NO:

```text
Reject
```

The process stops.

If YES:

```text
Borrow Allowed
```

---

## Another Example: Exam Eligibility

### Gate 1

Attendance ≥ 75% ?

### Gate 2

Assignment Submitted ?

### Gate 3

Marks ≥ 50 ?

---

## Decision Flow

```text
Attendance ≥ 75?
        │
     ┌──┴──┐
    No    Yes
    │       │
Not Eligible ▼

Assignment Submitted?
        │
     ┌──┴──┐
    No    Yes
    │       │
Not Eligible ▼

Marks ≥ 50?
        │
     ┌──┴──┐
    No    Yes
    │       │
   Fail   Pass
```

---

## Programming Team Model

### Worker 1 - Traversal

Visits an item.

---

### Worker 2 - Processing

Collects information needed for decisions.

---

### Gate 1

Checks the first condition.

---

### Gate 2

Checks the second condition.

---

### Gate 3

Checks the third condition.

---

### Worker 3 - Automatic Repetition

Repeats the process when needed.

---

## Important Concept

A nested if means:

```text
Gate 1
   ↓
Gate 2
   ↓
Gate 3
   ↓
Action
```

Each gate must approve before moving to the next gate.

If any gate rejects, the process stops.

---

## Key Understanding

Day 12:

```text
One Gate
```

Day 13:

```text
One Gate
Two Choices
```

Day 14:

```text
One Gate
Many Choices
```

Day 15:

```text
Multiple Gates
Checked One After Another
```

Programs can now make layered decisions using multiple approval gates.

---

## My Thought

Now I understand that a nested if is like passing through multiple decision gates. Each gate checks a condition and decides whether the process can continue. If all gates approve, the final action is performed. If any gate rejects, the process stops. This helps programs make step-by-step decisions in an organized way.
