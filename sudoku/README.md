# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: *In the space of each unit where two matching box values occur, we use
the constraint that there cannot be any other boxes belonging to said unit
which contain either of the digits from the two matching boxes. We iterate
over each unit to ensure this constraint is enforced throughout the board.*

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *A collection of diagonal boxes are cached via
`diagonal_units = [[rows[i]+cols[i] for i in range(9)], [rows[i]+cols[::-1][i] for i in range(9)]]`.
From here the diagonal units are appended to the list of all existing units, so
that our constraint of different numbers belonging to each box of a given unit can
be enforced. Such a constraint is enforced via `only_choice` and `naked_twins`.*

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.