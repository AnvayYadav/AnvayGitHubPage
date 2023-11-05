---
toc: true 
comments: true 
layout: post 
title: 3.5 and 3.6 Homework Solution
description: 3.5 and 3.6 Homework Solution
courses: { compsci: {week: 7} } 
type: tangibles
---

# Problem 1 Solution

```
# Problem 1: Eligibility to Vote

# Get user input for age
age = int(input("Enter your age: "))

# Check eligibility based on age
if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote.")
```

# Problem 2 Solution

```
# Problem 2: Employee Bonus Calculation

# Get user input for salary and years of service
salary = float(input("Enter your salary: "))
years_of_service = int(input("Enter your years of service: "))

# Calculate bonus if years of service is more than 5
if years_of_service > 5:
    bonus = 0.05 * salary
    print(f"Your bonus amount is ${bonus:.2f}")
else:
    print("You are not eligible for a bonus.")
```

# Problem 3 Solution

```
# Problem 3: Grading System

# Get user input for marks
marks = float(input("Enter your marks: "))

# Determine the grade based on the given rules
if marks < 25:
    grade = "F"
elif 25 <= marks < 45:
    grade = "E"
elif 45 <= marks < 50:
    grade = "D"
elif 50 <= marks < 60:
    grade = "C"
elif 60 <= marks < 80:
    grade = "B"
else:
    grade = "A"

print(f"Your grade is {grade}")
```