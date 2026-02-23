Aim:
To understand and implement for loops and nested loops in Python through practical examples, 
including printing sequences, summing numbers, matrix display, matrix multiplication, and pattern printing.

Introduction:
For loops in Python enable repeating a block of code over a sequence such as range, lists, or strings, making iterative tasks efficient.​
This notebook demonstrates basic for loop syntax for printing numbers and even numbers, 
summing first N numbers, nested loops for 3x3 matrix operations like display and multiplication of two matrices, along with patterns using reverse loops.

Algorithms.
1.
Print Numbers 1 to 5
Initialize the loop counter i starting from 1.
Continue the loop while i ≤ 5, incrementing i by 1 each iteration (using range(1,6)).
In each iteration, output the current value of i followed by a newline.
Loop terminates after i=5.
End program.

2.Print Even Numbers from 1 to 10
Initialize loop counter i at 2 (first even number after 1).
Continue while i ≤ 10, incrementing by 2 each time (range(2,11,2)).
Output i with newline in each iteration.
Loop ends at i=10.
End

3.Sum of First N Numbers (Example: N=6)
Input value of N (e.g., 6).
Set total accumulator to 0.
For i from 1 to N (range(1,N+1)): Add i to total.
After each addition, print current sum state for visualization.
After loop, final total holds sum (formula: N*(N+1)/2 = 21 for N=6).
End.

4.Display 3x3 Matrix
Define 3x3 matrix A = [, , ].
Outer loop: For each row index i (0 to 2).
Inner loop: For each column j (0 to 2), print A[i][j] without trailing space.
After inner loop, print newline for next row.
Repeat for all rows.
End.​

5.Multiplication of Two 3x3 Matrices
Define A and B as identical 3x3 matrices: [, , ].
Initialize result as 3x3 zero matrix: [, , ].
Triple nested loops:
Outer i (rows of result, 0-2).
Middle j (columns of result, 0-2).
Inner k (0-2): result[i][j] += A[i][k] * B[k][j].
After loops, print each row of result.
End (yields [, , ]).

6.Star Pattern (Reverse Pyramid)
Outer loop: i from 5 down to 1 (range(5,0,-1)).
For each i, print '-' repeated i times (e.g., i=5: '-----').
Each print adds automatic newline.
Loop ends at i=1.
End.

Conclusion:
This experiment successfully demonstrates the versatility of for loops and nested loops in Python for iterative tasks.​
Key concepts like sequence iteration, accumulation, matrix traversal, and pattern generation were implemented with correct outputs matching expected results, 
reinforcing practical understanding of loop control structures.​
These techniques form foundational skills for algorithm design and data processing in programming coursework.
