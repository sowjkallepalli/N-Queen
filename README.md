# **N-Queens Problem Solver (Backtracking)**
**Author:** Kallepalli Lakshmi Sowjanya 
**Approach:** Solving N queen problem using backtracking 

## **Overview**  
The **N-Queens problem** is a classic combinatorial optimization problem in which the goal is to place `N` queens on an `N × N` chessboard so that no two queens threaten each other. This means:  
- No two queens can be in the same row.  
- No two queens can be in the same column.  
- No two queens can be on the same diagonal.

  This is a generic problem for popular [8 queen problem] (https://en.wikipedia.org/wiki/Eight_queens_puzzle).


This repository contains a Python implementation using **backtracking** to solve the **N-Queens problem**, specifically for `N = 22`, though the code supports any `N` value.  

## **Approach**  
- The solution uses **backtracking** with **set-based pruning** to efficiently explore valid queen placements.  
- **Column, positive diagonal, and negative diagonal constraints** are used to eliminate invalid moves early.  
- The search is **stopped after 4 valid solutions** for performance optimization.  
- The results are printed in the required format, with each solution represented as a list of `(row, column)` pairs.  

## **Example Output (for N = 4)**  
```
(0,1) (1,3) (2,0) (3,2)

(0,2) (1,0) (2,3) (3,1)
```

## **How to Run the Code**  
1. Clone this repository:  
   ```bash
   git clone https://github.com/sowjkallepalli/N-Queens.git
   cd n-queens-solver
   ```
2. Run the Python script:  
   ```python
   python n_queens.py
   ```
3. The first **4 valid solutions** will be printed in the console.  

## **Modifications**  
- To **find all solutions**, remove the condition:  
  ```python
  if len(result) == 4:
      return
  ```  
- You can change `N` by modifying the `n` variable:  
  ```python
  n = 22  # Change this to any value of N
  ```

## **Complexity Analysis**  
- The worst-case time complexity is **O(N!)**, but pruning techniques significantly improve performance.  

## **Future Enhancements**  
- Optimize the algorithm using **bitwise operations** for even faster execution.  
- Implement parallel processing for large `N` values.  
