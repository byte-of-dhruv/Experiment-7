# Experiment-7
Studying While Loop in Python

Dhruv Verulkar

25070123162

AIM

To study and implement the while loop in Python programming language and understand its working mechanism, flow control, and practical applications through various programs including counting, factorial computation, Fibonacci series generation, number reversal, palindrome checking, digit counting, and list searching.

THEORY

Introduction to Loops in Python A loop is a programming construct that allows a set of instructions to be executed repeatedly based on a condition or a count. Python supports three main types of loops: the while loop, the for loop, and nested loops. Loops are fundamental to programming as they reduce code redundancy and allow repetitive tasks to be performed efficiently without rewriting the same code multiple times.
The While Loop The while loop in Python is an entry-controlled loop that repeatedly executes a block of statements as long as the given condition remains True. Before each iteration, the condition is checked. If it evaluates to True, the body of the loop is executed. If it evaluates to False, the loop terminates and control passes to the next statement after the loop body. Syntax of the while loop: while condition: statement(s) The condition in a while loop can be any valid Python expression that returns a Boolean value (True or False). The body of the loop must contain a statement that eventually changes the value of the condition variable; otherwise, the loop will run indefinitely, resulting in an infinite loop.
Flow of Execution The execution flow of a while loop follows these steps:
The condition is evaluated first (entry-controlled).

If the condition is True, the loop body executes.

After the loop body executes, control goes back to re-evaluate the condition.

If the condition is False, the loop terminates.

Control passes to the first statement following the while loop.

Loop Control Statements
Python provides special statements to control the behavior of loops during execution.

break Statement: The break statement immediately terminates the loop regardless of the condition. When break is encountered inside a loop, Python exits the loop and execution continues with the first statement after the loop body. This is used in scenarios such as searching for an element in a list where we exit as soon as we find the target. continue Statement: The continue statement skips the rest of the loop body for the current iteration and jumps back to re-evaluate the condition. It is used when we want to skip certain iterations based on a condition, such as skipping even numbers and printing only odd numbers. else Clause with while: Python allows an optional else clause with the while loop. The else block executes when the loop condition becomes False naturally (not when terminated by break). This is particularly useful in search operations where we want to handle the case when an element is not found.

Practical Applications Covered in This Experiment
a) Printing Numbers 1 to N: A basic while loop that initializes a counter variable and increments it by 1 on each iteration until it exceeds the user-defined limit N. This demonstrates the basic working of entry-controlled loops.

b) Factorial Computation: The factorial of a number n (written as n!) is the product of all positive integers from 1 to n. The while loop multiplies the result by the current value of n and decrements n by 1 on every iteration until n reaches 0. For example, 5! = 5 x 4 x 3 x 2 x 1 = 120. c) Fibonacci Series: The Fibonacci sequence is a series where each number is the sum of the two preceding ones: 0, 1, 1, 2, 3, 5, 8, 13, ... The while loop updates two variables a and b such that a becomes b and b becomes the sum of the previous a and b. Two approaches are implemented: printing up to N terms and printing up to a given limit value.

d) Reversing a Number: The last digit of a number is extracted using the modulo operator (%). It is appended to the reversed number by multiplying the current reversed value by 10 and adding the digit. The original number is then integer-divided by 10. This process repeats until all digits are extracted.

e) Palindrome Checking: A palindrome is a number or string that reads the same forwards and backwards (e.g., 121, 'madam', 'icici'). For numbers, the reversed number is compared with the original. For strings, the two-pointer technique is used with the while loop to compare characters from both ends simultaneously. f) Counting Digits: The while loop counts the number of digits in an integer by repeatedly dividing the number by 10 and incrementing a counter until the number becomes 0. For example, 5445811 has 7 digits. g) Searching in a List: Linear search is implemented using a while loop that traverses the list from the beginning and compares each element with the key. If found, the index is reported and the loop breaks. The else clause handles the case where the element is not found. h) Printing Odd Numbers using continue: The continue statement is used to skip even numbers inside the while loop. The loop increments i, checks if it is even, and if so, skips the print statement using continue. Only odd values of i are printed.

ALGORITHM

Algorithm 1: Print Numbers 1 to N

Start.

Accept input value of n from the user.

Initialize i = 1.

While i <= n, repeat steps 5 and 6.

Print the value of i.

Increment i by 1 (i = i + 1).

Stop.

Algorithm 2: Factorial of a Number

Start.

Accept input value of n from the user.

Initialize fact = 1.

While n > 0, repeat steps 5 and 6.

Multiply fact by n (fact = fact * n).

Decrement n by 1 (n = n - 1).

Print fact.

Stop.

Algorithm 3: Fibonacci Series (N Terms)

Start.

Accept number of terms n.

Initialize a = 0, b = 1, i = 1.

While i <= n, repeat steps 5 to 7.

Print a.

Set c = a + b, a = b, b = c.

Increment i by 1.

Stop.

Algorithm 4: Reverse a Number

Start.

Accept number num from the user.

Initialize rev = 0.

While num > 0, repeat steps 5 to 7.

Extract digit = num % 10.

Update rev = rev * 10 + digit.

Remove last digit: num = num // 10.

Print rev.

Stop.

Algorithm 5: Palindrome Check (Number)

Start.

Accept number num from the user.

Store temp = num, initialize rev = 0.

Reverse num into rev using the while loop (same as Algorithm 4).

If temp == rev, print "Palindrome". Else print "NOT Palindrome".

Stop.

Algorithm 6: Searching an Element in a List

Start.

Define list nums = [10, 20, 30, 40, 50] and accept key from the user.

Initialize index i = 0.

While i < length of nums, repeat steps 5 and 6.

If nums[i] == key, print index and break.

Increment i by 1.

If loop ends without break (else block), print "element not found".

Stop.

CONCLUSION

In this experiment, we successfully studied and implemented the while loop in Python programming language. The while loop is one of the most powerful and flexible control structures in Python, enabling repeated execution of a block of code based on a dynamic condition rather than a fixed count. Through the various programs implemented, we observed that the while loop is particularly well-suited for situations where the number of iterations is not known in advance and depends on runtime conditions. Programs such as factorial computation, number reversal, digit counting, and palindrome checking all benefited from the flexibility offered by the while loop. We also studied the loop control statements break and continue, which provide additional flexibility in managing loop execution. The break statement allows early termination of the loop (as seen in the list search program), while the continue statement allows skipping specific iterations (as seen in printing odd numbers). The optional else clause with the while loop proves useful in handling the case when a loop ends without a break. The Fibonacci series program demonstrated two approaches to using the while loop: iterating a fixed number of times and iterating until a threshold value is reached. Both approaches reinforce the adaptability of the while loop for different problem types. The palindrome checking experiment was implemented in three distinct ways: using number reversal and comparison, using the two-pointer technique with a while loop, and using Python's string slicing shortcut. This demonstrated that while loops can serve as the backbone of various algorithmic strategies for the same problem. Overall, this experiment provided a thorough understanding of the while loop construct, its syntax, flow of control, practical use cases, and the importance of correctly updating loop variables to prevent infinite loops. The while loop forms a critical foundation for solving problems that involve repetition, iteration, and condition-based execution in Python.
