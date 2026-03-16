At its core, the for loop follows a simple syntax: for item in iterable:.

When this line executes, Python performs an internal "handshake" with the object being looped over. It checks if the object is an Iterable—meaning it has an iter method that can return an Iterator. This iterator is responsible for keeping track of the current position and providing the "next" value until the sequence is exhausted.

Key Components:

The Target Variable: (e.g., item) This is a placeholder that gets reassigned to the value of each element in the sequence during every pass of the loop.

The Iterable: This can be any object capable of returning its members one at a time. This includes:

Sequences: Lists, Tuples, Strings, and Ranges.

Mappings: Dictionaries (where it iterates over keys by default).

Collections: Sets.

The range() Function Because Python loops are designed to iterate over objects, you need a specific tool if you simply want to repeat an action n times. This is where range() comes in.

Technically, range() is not a function but an immutable sequence type. When you call range(5), Python does not generate a list of five numbers in memory; instead, it creates a "range object" that calculates numbers on the fly (lazy evaluation). This makes it incredibly memory-efficient, whether you are iterating from 1 to 10 or 1 to 10,000,000.

The Anatomy of range(start, stop, step):

Start: The starting value (inclusive). Defaults to 0.

Stop: The ending value (exclusive). The loop terminates before reaching this number.

Step: The increment between each number. It can be positive (counting up) or negative (counting down).

Control Flow Tools: break, continue, and else To add "intelligence" to a loop, Python provides three keywords that alter the standard linear flow:
break: Immediately terminates the loop, skipping any remaining iterations.

continue: Skips the rest of the code inside the current loop block and "jumps" to the next item in the sequence.

else: This is a unique Python feature. A code block under else will execute only if the loop completes all iterations naturally (i.e., it was not terminated by a break). This is often used for search operations where you want to perform an action if a target was not found.

Nested Loops and Complexity Python allows you to place a loop inside another loop. During execution, the inner loop completes its entire cycle for every single iteration of the outer loop. Break: Stops the loop completely.
Continue: Skips the current iteration.

Multiplying two 3x3 Matrix: for i in range(3): # rows of a
for j in range(3): # rows of b
for k in range(3):
result[i][j] += a[i][k] * b[k][j]
for row in result:
print(row)

Algoritm:

A)Print Even Numbers from 1 to 10:

Start

Initialize a loop starting at i = 2, ending before 11, with a step increment of 2.

In each iteration, print the current value of i. End

B)Sum of First n Numbers: Start Input an integer value for n. Initialize a variable sum to 0. Initialize a loop that iterates from i = 1 to n. In each iteration, add the value of i to sum. After the loop finishes, print the final value of sum. End

C)Print a 3x3 Matrix: Start Define a 2D list (matrix) a with 3 rows and 3 columns. Outer loop: Iterate through each row index i (from 0 to 2). Inner loop: Iterate through each column index j (from 0 to 2). Print the element at a[i][j] followed by a space, without moving to a new line. After the inner loop finishes, print a newline character to move to the next row. End

D)Matrix Multiplication (3x3): Start Define two 3x3 matrices, a and b. Initialize a 3x3 matrix result filled with 0s. Outer loop: Iterate through each row i of matrix a. Middle loop: Iterate through each column j of matrix b. Inner loop: Iterate through index k (from 0 to 2) to perform dot product. Calculate result[i][j] = result[i][j] + (a[i][k] * b[k][j]). After all loops, iterate through each row in result and print it. End

E)Combinations of 3 Unequal Numbers: Start Define a list d containing three distinct numbers (1, 2, 3). Create three nested loops (i, j, k), each iterating from index 0 to 2. Check the condition: if d[i] != d[j] AND d[j] != d[k] AND d[i] != d[k]. If the condition is true, print the combination d[i], d[j], d[k]. End

F)Pattern Printing (Right-Angle and Pyramid) Algorithm for Right-Angle Triangle: Start Loop from i = 1 to 9. In each iteration, print the string "* " multiplied by i. End Algorithm for Pyramid Triangle: Start Set rows = 5. Loop from i = 1 to rows. In each iteration, print spaces equal to (rows - i) followed by the string "* " multiplied by i. End

Conclusion:

Hence for loop was used in python and programs were done using it.





#Syntax for python
for variable in sequence:
    statement(s)

     

#print numbers from 1 to 5
for i in range(1,6):
    print(i)

     
1
2
3
4
5

#print odd number 1 to 10
for i in range(1, 11, 2):
    print(i)
     
1
3
5
7
9

#print even number from 1 to 10
for i in range(2, 11, 2):
    print(i)
     
2
4
6
8
10

#Sum of n number
n = int(input("Enter the number: "))
total =0
for i in range(1, n+1):
    total = total + i
print("SUM = ",total)
     
Enter the number: 6
SUM =  21

# print 3*3 matrix display
A = [[1,2,3],
     [4,5,6],
     [7,8,9]]

for i in range(3):
  for j in range(3):
    print(A[i][j],end=" ")
  print()


     
1 2 3 
4 5 6 
7 8 9 

#Multiplication
A = [[1,2,3],
     [4,6,7],
     [8,9,10]]
B = [[1,1,1],
     [6,7,5],
     [3,2,1]]
Result = [[0,0,0],
          [0,0,0],
          [0,0,0]]
for i in range(3):
  for j in range(3):
    for k in range(3):
      Result[i][j] += A[i][k] * B[k][j]
for row in Result:
  print(row)
     
[22, 21, 14]
[61, 60, 41]
[92, 91, 63]

#Possible combination without repeatation
d1=1
d2=2
d3=3
d=[d1,d2,d3]
#123,132,231,312,312,321
for i in range(0,3):
  for j in range(0,3):
    for k in range(0,3):
      if(i!=j and j!=k and i!=k):
        print(d[i],d[j],d[k])
     
1 2 3
1 3 2
2 1 3
2 3 1
3 1 2
3 2 1

#Print right angle triangle
for i in range(1,6):
  print("*"*i)

     
*
**
***
****
*****

for i in range(5,0,-1):
  print("*"*i)
     
*****
****
***
**
*

#pyramid shape
for i in range(1,6):
  print(" "*(5-i)+" *"*i)
     
     *
    * *
   * * *
  * * * *
 * * * * *

#inverted pyramid
for i in range(5,0,-1):
  print(" "*(5-i)+" *"*i)
     
 * * * * *
  * * * *
   * * *
    * *
     *
