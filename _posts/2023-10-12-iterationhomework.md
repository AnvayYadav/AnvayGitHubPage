---
toc: true 
comments: true 
layout: post 
title: P1 Iteration Homework
description: P1 Iteration Homework
type: tangibles
courses: { compsci: {week: 8} } 
---



def aspects_of_life(aspect_list):
if not aspect_list:
return # Termination: Return when there are no more aspects to explore.
else:
current_aspect = aspect_list[0]
remaining_aspects = aspect_list[1:]

    print(f"Today, I {current_aspect}.")
    
    aspects_of_life(remaining_aspects)
my_life_aspects = ["Wake up", "School", "Club", "Sports", "Instruments", "Homework", "Sleep"]

aspects_of_life(my_life_aspects)

Code:

  def fibonacci(x):
    if x==1:
      return(0) # First terminating statement
    if x == 2:
      return(1) # Second terminating statement

    else:
      return(fibonacci(x-1)+ fibonacci(x-2))


  for i in range(8):    
    print(fibonacci(i+1))
First Terminating Statement (x == 1):

When x is equal to 1, the code returns 0. This is because the first Fibonacci number (F(1)) is defined as 0 in the sequence.
Second Terminating Statement (x == 2):

When x is equal to 2, the code returns 1. This is because the second Fibonacci number (F(2)) is defined as 1 in the sequence.