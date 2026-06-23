Day 2 - Variables

What is a Variable?

A variable is a named container that stores information.

Just like we keep items in labeled boxes, a computer stores information in variables so it can use that information later.

---

Why Do We Need Variables?

Sometimes we can directly give values to the computer.

Example:
```python
print("Lakshaga")
print(30)
```
This works perfectly.

So why use variables?

Variables become useful when information needs to be:

- Remembered
- Reused
- Changed
- Calculated
- Collected from users

Without variables, we would have to repeat values again and again.

With variables, we store once and use many times.

---

## When Variables Are Not Needed

Variables are useful, but they are not required for every situation.

If a value is used only once and will never change, we can directly use the value.

Example:

```python
print("Hello World")
```
Output:

```text
Hello World
```
No variable is needed because the text is used only once.

Another example:
```python
print(10 + 20)
```
Output:
```text
30
```
The numbers are used only for this calculation, so variables are optional.

Using variables here would also work:
```python
a = 10
b = 20

print(a + b)
```
Both programs produce the same output.

---

When Variables Become Important

Variables are helpful when information:

- Needs to be remembered
- Is reused multiple times
- Can change later
- Comes from user input
- Is used in calculations

Example:
```python
name = "Lakshaga"

print(name)
print(name)
print(name)
```
Instead of writing the same value repeatedly, we store it once and reuse it.

This makes programs easier to modify and maintain.

---

Simple Rule

If a value is used only once, a variable may not be necessary.

If a value needs to be remembered, reused, or changed, a variable is usually the better choice.


---
Tea Making Logic with Variables

Suppose we want to store the ingredients needed to make tea.
```python 
water_cups = 1
milk_cups = 1
tea_powder_spoons = 2
sugar_spoons = 3
```
Here:

- "water_cups" stores 1 cup of water
- "milk_cups" stores 1 cup of milk
- "tea_powder_spoons" stores 2 spoons of tea powder
- "sugar_spoons" stores 3 spoons of sugar

Now our instructions become:

1. Take "water_cups" and "milk_cups"
2. Add "tea_powder_spoons"
3. Boil the mixture
4. Add "sugar_spoons"
5. Mix and serve

The computer stores only the values.

The programmer provides meaning through good variable names.

---

How Does the Computer Know It Is a Cup or Spoon?

The computer does not know.

For example:
```python
water = 1
```
The computer only knows:

- Variable name = "water"
- Value = "1"

It does not know whether 1 means:

- 1 cup
- 1 spoon
- 1 litre
- 1 kilogram

That meaning comes from the programmer.

This is why descriptive variable names are important.
```python
water_cups = 1
sugar_spoons = 3
```
These names make the program easier to understand.

---

Example
```python
name = "Lakshaga"
age = 30
```
Here:

- "name" stores text
- "age" stores a number

The computer remembers these values and allows us to use them later.

---

Using Variables

```python
name = "Lakshaga"

print(name)
```
Output
```text
Lakshaga
```
The computer looks inside the variable and prints the stored value.

---

## Data Types

Every value stored in a variable has a data type.

A data type tells the computer what kind of information is being stored.

### Integer (int)

Whole numbers.

age = 30
sugar_spoons = 3

Examples:

1
10
100

---

### Float

Numbers with decimal values.

milk_litres = 1.5
temperature = 98.6

Examples:

1.5
2.75
99.99

---

### String (str)

Text enclosed in quotes.

name = "Lakshaga"
drink = "Tea"

Examples:

"Python"
"India"
"Hello"

---

### Boolean (bool)

Stores only True or False.

tea_ready = True
shop_open = False

Examples:

True
False

---

Tea Making Example with Different Data Types

drink_name = "Tea"
water_cups = 1
milk_cups = 1.5
tea_ready = False

Variable| Value| Data Type
drink_name| Tea| String
water_cups| 1| Integer
milk_cups| 1.5| Float
tea_ready| False| Boolean

---

## My Thought

On Day 1, I learned that programming is giving instructions to a computer.

Today I learned that instructions need information to work with.

Variables store that information.

I also learned that every value has a data type, which helps the computer understand how to process the data.

---

## What I Learned Today

- Variables store information.
- Variables have names.
- Good variable names provide meaning.
- Variables help us remember and reuse data.
- Variables make programs flexible and easier to update.
- Every value has a data type.
- Common data types are Integer, Float, String, and Boolean.

## Programming Rule #2

Store once, use many times.

Variables help programs remember information so that instructions can use it whenever needed.
