---
title: "My Notes - Problem Solving - Solving Coding Problems"
subtitle: "How I Solve Coding Problems"
layout: post
author: "Coosoti"
header-style: text
tags:
  - Coding Interview
  - Problem Solving
  - How to solve it
  - Python
  - C
  - JavaScript
---
#### Introduction

![image](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20200305191534/How-to-Approach-a-Coding-Problem.png)
[*Image is from GeeksforGeeks Website*](https://www.geeksforgeeks.org/how-to-approach-a-coding-problem/)

Programming is all about problem-solving, and if I need to be a better software engineer, I need to get better at understanding and solving coding problems.

After much research, I stumbled upon an blog post by [Madison Kanna](https://www.freecodecamp.org/news/how-to-solve-coding-problems/) explaining her 4-step problem-solving method.

I have adopted her method, which she borrowed from G. Polya's book *How to solve it*. I will illustrate the technique here using Python language and a simple function.

**Consider this**

> Create a function that adds together two integers and returns that value

***Here is how I would solve it***

#### Step-1. Understanding the Problem

* Do not rush into coding at first
* Read through the problem slowly
* Think though any parts you may not understand

**Note:** If you do not understand the problem, you cannot solve it.

**You may ask yourself these questions to understand better the problem**

- **What are the inputs?**

    * In my case study, the inputs are two integers. Ask yourself these questions:

    * *Will the input always be two integers? What if the function receives three or zero integers?*
    * *Will the inputs be always integers? What if the function receives string as inputs?*

    ```
    // inputs: 3, 6
    ```


- **What are the outputs?**

    * In our case, the output is one integer - sum of the two integers
    * *What will the function return? An integer, a string, boolean, etc*

- **Create example inputs against expected output**

    * *Simple/straightforward examples*

    ```
    // add(3, 6) ---> 9
    // add(7, 9) ---> 16
    ```

    * *Complex/Edge Cases Examples*

    ```
    // add('a', 'c') ---> this should return an error as int is expected not a string
    ```

    **Note:** Sometimes the instruction on the problem may tell you to only
 expect integers as input or ask you what to do if there are no inputs or if the inputs exceed the accepted number.

    **Note:** One must always practice ***Defensive Coding***. That is, you should always anticipate what could go wrong and how you would handle them.

#### Step-2. Devising a Plan

- Note down how you would solve the problem in a pseudocode.

- In our case study:

    ```
    # pseudocode

    // create a sum variable - initialize it to Zero
    // add first and second inputs using the '+' operator
    // store the value of the result on the sum variable
    // return the sum variable as the output
    ```

    **Note:** Consider systematically how you, a human being, would solve this problem - Not how the code would solve it.

#### Step-3. Carrying Out the Plan

* Code the solution on the computer in an actual code using the pseudocode as a guide.

    ```
    #!/usr/bin/env python3

    sum = 0
    def add(a, b):
        """add two integers and return sum -> integer"""
        sum = a + b
        return sum

    print(add(3, 6))
    print(add(7, 9))
    ```

* Output

    ```
    # output
    9
    16
    ```

**Note:** Do not prematurely optimize your code.
**Note:** If you find that part of the problem is complex, ignore it and solve the part you can. Then, you might also solve it afterward.

#### Step-4. Look back

* take time and reflect on your working solution
* figure out how to make improvements
* refactor the code to be more efficient

- **to be more price, the code could look like this after refactoring**

   ```
     #!/usr/bin/env python3

     def add(a, b):
         """add two integers and return a + b -> integer"""
         return a + b

     print(add(3, 6))
     print(add(7, 9))
     ```
