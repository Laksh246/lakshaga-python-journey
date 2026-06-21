# Day 14 - if, elif, else (Multiple Inspectors)

## What I Learned

Sometimes there are more than two possible outcomes.

The "if-elif-else" structure allows a program to choose one action from multiple possibilities.

---

## Real Life Example: Exam Grades

Suppose a student writes an exam.

The Inspector checks the student's marks.

Possible outcomes:

- 90 or above → Grade A
- 75 or above → Grade B
- 50 or above → Grade C
- Below 50 → Fail

The Inspector must choose only one result.

---

## Inspector's Decision Tree

Student Marks
      │
      ▼
Marks ≥ 90 ?
   │
 ┌─┴─┐
Yes  No
 │    │
 A   Marks ≥ 75 ?
         │
      ┌──┴──┐
     Yes   No
      │      │
      B    Marks ≥ 50 ?
               │
            ┌──┴──┐
           Yes   No
            │      │
            C    Fail

---

## Python Idea

marks = 82

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
elif marks >= 50:
    print("Grade C")
else:
    print("Fail")

---

## Understanding the Keywords

if

Checks the first condition.

if marks >= 90:

---

elif

Means:

«"Else, if this condition is true."»

elif marks >= 75:

The Inspector checks this only if the previous condition was False.

---

else

Means:

«"If none of the above conditions are true."»

else:

---

Inspector Team Example

Imagine a school.

Worker 1 - Traversal

Visits a student's record.

---

Worker 2 - Processing

Reads the student's marks.

Example:

Marks = 82

---

Inspector

Checks conditions one by one:

82 ≥ 90 ? ❌

82 ≥ 75 ? ✅

Decision:

Grade B

The Inspector stops checking after finding a match.

---

Worker 3 - Automatic Repetition

Repeats the process for all students.

---

## Important Concept

- if = First condition
- elif = Additional conditions
- else = Default action
- Only one matching branch runs
- Once a match is found, remaining checks are skipped

---

## Real Life Example: Weather

The Inspector checks the weather.

If raining → Take umbrella

Else if sunny → Wear sunglasses

Else if cloudy → Carry both

Else → Normal day

The Inspector chooses one action.

---

## Key Understanding

In Day 13, the Inspector had two choices:

True  → Action A
False → Action B

In Day 14, the Inspector has many choices:

Condition 1 → Action A

Condition 2 → Action B

Condition 3 → Action C

Else → Default Action

The Inspector checks conditions from top to bottom and stops when a match is found.

---

## My Thought

Now I understand that "if-elif-else" allows a program to choose from multiple possible actions. The Inspector checks conditions one by one and selects the first matching option. This helps programs handle more complex situations than simple yes-or-no decisions.

The team now has:
List = Storage
Worker 1 = Traversal
Worker 2 = Processing
Inspector = Decision Maker
Worker 3 = Automatic Repetition

And the Inspector has become smarter:
Day 12 → One condition (if)
Day 13 → Two choices (if-else)
Day 14 → Multiple choices (if-elif-else)
