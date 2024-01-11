---
toc: true 
comments: true 
layout: post
title: Team Teaching - Fault Tolerance & Parallel and Distributed Computing
description: Team Teaching - Fault Tolerance & Parallel and Distributed Computing
type: hacks
courses: { compsci: {week: 15} } 
---



Team teach HW questions answered:
## Sequential Code
```
def sequential_square(numbers):
    result = []
    for num in numbers:
        result.append(num**2)
    return result
if __name__ == "__main__":
    numbers_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    sequential_result = sequential_square(numbers_list)
    print(f"Sequential Result: {sequential_result}")
```
## Parallel Code
```
import concurrent.futures
def parallel_square(num):
    return num**2
if __name__ == "__main__":
    numbers_list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    with concurrent.futures.ThreadPoolExecutor() as executor:
        # Using ThreadPoolExecutor to parallelize the task
        parallel_result = list(executor.map(parallel_square, numbers_list))
    print(f"Parallel Result: {parallel_result}")
```
Example Flowchart:
We can make non fault tolerant systems fault tolerant, by introducing multiple paths between connected systems. If you do this, it will allow your system to continue and thrive even if something fails or some error pops up for one of the component.

![Flowchart](images/flowchart.png)