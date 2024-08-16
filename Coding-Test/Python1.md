# Python Coding Test Datatype and Complexity

[Course Source](https://www.youtube.com/watch?v=m-9pAwq1o3w&list=PLRx0vPvlEmdAghTr5mXQxGpHjWqSz0dgC)

## Online Judges

- **International:** Codeforces, TopCoder, LeetCode, CodeCHEF
- **Domestic:** BOJ, CodeUp, Programmers, SW Expert Academy

## Complexity
- **Time Complexity:** Evaluates the time taken for each algorithm to perform.
- **Space Complexity:** Evaluates the memory usage for each algorithm to perform.

### Big-O Notation
Big-O Notation considers the term that increases the fastest as the input size grows. We only keep the term with the highest order.

### Efficiency
- **Good:** Constant time - Logarithmic time - Linear time - Log-linear time - Quadratic time - Cubic time - Exponential time
- **Bad:** When source code calls internal functions, the time complexity of these functions must also be considered. Typically, coding test problems have time limits of 1-5 seconds. In Python, if the number of operations exceeds 500 million, it can take up to 15 seconds.

### Steps for Solving Problems
1. Read the problem statement and think computationally.
2. Analyze the requirements (complexity analysis).
3. Find ideas for solving the problem.
4. Design and write the source code.

### Measuring Execution Time in Python
```python
import time
start_time = time.time()  # Start measuring

# Your code here

end_time = time.time()  
print("time-consumed:", end_time - start_time)  # Output the execution time
