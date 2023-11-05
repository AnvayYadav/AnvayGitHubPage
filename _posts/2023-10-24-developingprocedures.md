---
toc: true 
comments: true 
layout: post 
title: 3.12 3.13 Developing Procedures
description: 3.12 3.13 Developing Procedures
type: plans
courses: { compsci: {week: 9} } 
---


def procedural_abstraction(parameter):
# Perform a specific task
result = parameter * 2
return result

Function to calculate the sum of two numbers
def summing_machine(first_number, second_number):
# Perform the specific task of adding two numbers
sum_result = first_number + second_number
return sum_result

Example usage of procedural_abstraction function
input_value = 5
abstraction_result = procedural_abstraction(input_value)
print("Result of procedural_abstraction:", abstraction_result)

Example usage of summing_machine function
num1 = 7
num2 = 5
sum_result = summing_machine(num1, num2)
print(f"The sum of {num1} and {num2} is:", sum_result)