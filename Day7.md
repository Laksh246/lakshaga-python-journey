# Day 7 - While Loop (Real Life Understanding)

## What I learned
A while loop repeats actions as long as a condition is true.

---

## Real Life Example: Phone Charging

When my phone battery is low, I plug in the charger.

The phone keeps charging until it becomes 100%.

### Thinking like a loop:
- Battery = 10% → Charging starts   
- Battery increases step by step  
- While battery < 100% → keep charging  
- When battery = 100% → stop charging ✔️  

This is a while loop.

---

## Python idea

```python battery = 10
while battery < 100:
    print("Charging...")
    battery = battery + 10
'''
