# Suduko_solver
I created a suduko solver using backtracking.

Algorithm:
1.	Create a function that checks if the given matrix is valid sudoku or not. Keep HashMap for the row, column and boxes. If any number has a frequency greater than 1 in the HashMap return false else return true;
2.	Create a recursive function that takes a grid and the current row and column index.
3.	Check some base cases. If the index is at the end of the matrix, i.e., i=N-1 and j=N then check if the grid is safe or not, if safe print the grid and return true else return false. The other base case is when the value of column is N, i.e j = N, then move to next row, i.e., i++ and j = 0.
4.	if the current index is not assigned then fill the element from 1 to 9 and recur for all 9 cases with the index of next element, i.e. i, j+1. if the recursive call returns true then break the loop and return true.
5.	if the current index is assigned then call the recursive function with index of next element, i.e., i, j+1

Complexity Analysis:
●	Time complexity: O(9^(n*n)). 
For every unassigned index, there are 9 possible options so the time complexity is O(9^(n*n)). The time complexity remains the same but there will be some early pruning so the time taken will be much less than the naive algorithm but the upper bound time complexity remains the same.
●	Space Complexity: O(n*n). 
To store the output array a matrix is needed.
