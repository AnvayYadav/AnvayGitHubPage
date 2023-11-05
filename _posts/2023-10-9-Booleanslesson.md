---
toc: true 
comments: true 
layout: post 
title: 3.5 Boolean Expressions and 3.6 Conditionals 
description: 3.5 Boolean Expressions and 3.6 Conditionals 
authors: Nitin Balaji, Akshay Nagesh, Anvay Yadav, Srini Nampalli 
courses: { compsci: {week: 7} } 
type: plans
---

### Booleans
2 Values
True
False

Example: my hair color is black: True

### Relational Operators
Equal to: a = b

Not equal to: a != b

Greater than: a > b

Less than: a < b

Greater than or equal to: a >= b

Less than or equal to: a <= b

### Popcorn Hack 1

In most states, the minimum age to drive is 16. How would we write a boolean expression to check if someone is at least 16 years old?
```
age >= 16
```


Write a boolean expression to check if the average of grade1, grade2, and grade3 is at least 70.
```
(grade1 + grade2 + grade3)/3 >= 70
```

Write a code to check if the temperature is less than 90 degrees
```
temp < 90
```
### Not operator
Not flips the condition
![](images/NoneOperator.png)

And operator
And combines two conditions together
AndOperator

Or operator
Or returns True if only one conditon is true
OrOperator

Popcorn Hack 2
You can go out if you did your homework and you scored at least an 80 on your exam. Write boolean expression for this
BooleanExercise

Example AP Question
ExampleQuestions A. II only
B. I and II only
C. I and III only
D. II and III only

Correct Answer: D

Question 1: What will be the value of z?
x = True
y = False
z = x and y

A. True
B. False
C. None
D. Syntax Error

Question 2: Which is the correct way to compare if two boolean variables a and b are equal in Python?

A. a = b
B. a == b
C. a and b
D. a equals b
Conditionals
Algorithm: a finite set of instructions that accomplish a specific task
Algorithm

Condition statements: fundamental concept in programming and logic
used to control the flow of a program by allowing it to make decisions based on certain conditions or criteria.
A condition statement typically consists of three main parts:
Condition: This is a Boolean expression or a logical test that evaluates to either true or false. It's the criteria that the program checks.
True Block: This is the set of instructions or code that gets executed if the condition is true. If the condition evaluates to true, the true block is executed.
False Block (optional): This is the set of instructions or code that gets executed if the condition is false. In some cases, there might be an alternative set of instructions to execute when the condition is false.
Example: If a student's average grade on exams is at least 75, they are eligible to receive extra credit. Otherwise, they must attend tutorial.
GradeExample


Example
In this example, the condition statement checks whether the value of x is greater than 5. If it's true, it executes the true block (printing "x is greater than 5"). Otherwise, it executes the false block (printing "x is not greater than 5").

x = 10
if x > 5:
    print("x is greater than 5")  # This is the true block
else:
    print("x is not greater than 5")  # This is the false block
Examples 2
Is another example of conditional statements using Elif. elif is a statement that is run right after the first if statement is run to be false. It is simply the condition after the If statement in the code if you want to implement more criteria to your code.

score = 90
attendance = 90
if score >= 90 and attendance >= 90:
    result = "Student receives an 'A+'."
elif score >= 80 and attendance >= 80:
    result = "Student receives a 'B' ."
else:
    result = "Student needs improvement in both score and attendance."
Popcorn Hack 2
Highest_score=None

scores = [10, 15, 38, 2 , 74, 94, 43, 19]

for score in scores:
  if Highest_score == None:
    Highest_score = score
  elif score > Highest_score:
    Highest_score = score

Highest_score = Highest_score - 1
print(Highest_score)

# What will be the final output of the program?
Popcorn Hack 3
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult.")
    driving_license = input("Do you have a driving license? (yes/no): ")
    if driving_license.lower() == "yes":
        print("You can legally drive.")
    else:
        print("You need to obtain a driving license to drive legally.")
else:
    print("You are a minor.")
    parental_consent = input("Are you a teenager (yes/no): ")
    if parental_consent.lower() == "yes":
        print("You can continue")
    else:
        print("You need to be at least a teenager to continue with the activity")

# If the age entered was 12, what would be all of the statements printed.

### Homework
Problem 1: Write a Python program that uses boolean logic to determine if a user is eligible to vote. The criteria for eligibility is that the user must be a citizen and must be 18 or older. Include comments in your code to explain each part of the program.

Problem 2: A company decided to give bonus of 5% to employee if his/her year of service is more than 5 years. Ask user for their salary and year of service and print the net bonus amount.

Problem 3: A school has following rules for grading system:


a. Below 25 - F
b. 25 to 45 - E
c. 45 to 50 - D
d. 50 to 60 - C
e. 60 to 80 - B
f. Above 80 - A
Ask user to enter marks and print the corresponding grade.