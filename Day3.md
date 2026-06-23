# Day 3 - Variables Doing Work

## What Did I Learn Today?

On Day 2, I learned that variables store information.

Today I learned that variables can also work together to perform calculations.

A program does not just store data.

It can process data and produce new information.

---

## From Storage to Processing

Suppose we store two numbers:

```python
a = 10
b = 5
```

The computer remembers these values.

But we can also ask the computer to perform a calculation:

```python
c = a + b
```

Now:

```text
a = 10
b = 5
c = 15
```

The result is stored in another variable.

This means variables can store both original values and calculated values.

---

## Complete Example

```python
a = 10
b = 5

c = a + b

print(c)
```

### Output

```text
15
```

The computer:

1. Stores 10 in `a`
2. Stores 5 in `b`
3. Adds the values
4. Stores the result in `c`
5. Prints the result

---

## Tea Making Logic Example

On Day 2, we stored ingredients in variables.

```python
water_cups = 1
milk_cups = 1
```

Now we can calculate the total liquid.

```python
total_liquid = water_cups + milk_cups
```

Result:

```text
2 cups
```

The variables are no longer just storing information.

They are helping us create new information.

---

## Why Is This Important?

Computers become useful when they process data.

Example:

```python
salary = 50000
bonus = 5000

total_salary = salary + bonus
```

Result:

```text
55000
```

The computer transforms stored data into useful information.

This is the beginning of problem solving through programming.

---

## Common Arithmetic Operations

### Addition (+)

```python
a = 10
b = 5

result = a + b
```

Output:

```text
15
```

---

### Subtraction (-)

```python
a = 10
b = 5

result = a - b
```

Output:

```text
5
```

---

### Multiplication (*)

```python
a = 10
b = 5

result = a * b
```

Output:

```text
50
```

---

### Division (/)

```python
a = 10
b = 5

result = a / b
```

Output:

```text
2.0
```

---

## More Arithmetic Operators

### Modulus (%)

Returns the remainder after division.

```python
10 % 3
```

Output:

```text
1
```

### Exponent (**)

Raises a number to a power.

```python
2 ** 3
```

Output:

```text
8
```

### Floor Division (//)

Returns the whole-number part of a division.

```python
10 // 3
```

Output:

```text
3
```

---

## Store + Calculate + Result

A simple programming pattern is:

```text
Input Data
      ↓
Store in Variables
      ↓
Perform Calculation
      ↓
Store Result
      ↓
Display Output
```

Example:

```python
a = 10
b = 5

result = a + b

print(result)
```

---

## Connecting Day 1, Day 2, and Day 3

### Day 1

Instructions tell the computer what to do.

```text
Add two numbers
```

### Day 2

Variables store the numbers.

```python
a = 10
b = 5
```

### Day 3

Variables work together to perform calculations.

```python
result = a + b
```

Now the computer is not only storing information.

It is processing information.

---

## My Thought

Today I learned that variables are not just containers.

They can participate in calculations and help create new information.

This makes programming more powerful because computers can process data instead of only storing it.

---

## What I Learned Today

- Variables can store values.
- Variables can be used in calculations.
- Results can be stored in new variables.
- Computers process data using arithmetic operations.
- Python provides addition, subtraction, multiplication, division, modulus, exponent, and floor division operators.
- Programming is moving from storing information to processing information.

### Programming Rule #3

**Store → Process → Result**

Variables are not just containers. They are the building blocks used to create new information.
