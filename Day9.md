# Day 9 - Functions with Input (Parameters & Arguments)

## What I learned
Functions can take input values and produce different outputs based on those inputs. This makes programs flexible like real apps such as a mobile camera.

---

# Real Life Example: Mobile Camera

When I open my mobile camera, I see options like:

- Mode → selfie / portrait / night
- Flash → on / off
- Filter → beauty / black & white

These options decide how the final photo will be taken.

---

# Parameters and Arguments Together (Camera Model)

Let’s understand both together using one clear flow:

---

##  Python Example (Function Definition)

## Step 1: Parameters (Design Stage)
Inside the function:
mode → parameter (empty slot / label)
flash → parameter (empty slot / label)
filter → parameter (empty slot / label)

These are only placeholders created when designing the camera system.

## Step 2: Arguments (User Usage Stage)
Now we actually use the function:

# Python
take_photo("portrait", "off", "beauty")
Here:
"portrait" → argument for mode
"off" → argument for flash
"beauty" → argument for filter

These are real values filled into the empty slots.

## Full Mobile Camera Thinking
Camera System                                          Programming
Mode, Flash, Filter (labels in camera)                  Parameters
Portrait, Off, Beauty (user choices)                    Arguments
Final captured photo                                    Output

## Complete Flow
Camera is designed with slots (parameters)
User selects options (arguments)
Function receives values
Photo is generated based on choices

## Another Real Life Example: Coffee Machine
Parameters → sugar level, milk level, strength
Arguments → 2 spoons, full milk, strong coffee
Same machine, different results based on inputs.

## Key Understanding
Parameters = named empty slots inside function
Arguments = actual values passed into those slots when calling function

## My thought
Now I understand that functions work like a mobile camera where parameters define the available options and arguments are the actual choices that produce different results.

---

## 🐍 Python Example (Function Definition)

``` python
def take_photo(mode, flash, filter):
    print("Mode:", mode)
    print("Flash:", flash)
    print("Filter:", filter)
 '''

