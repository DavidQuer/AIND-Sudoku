# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: *In this case we have defined another set of rules by adding the constraint that diagonal have to be unique. This affects what we consider peers of a box. So, we perform constraint propagation by repeatedly enforcing this new rules used by the strategies implemented such eliminate and only_choice.*

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: *This is a tricky one because, Naked Twins is a strategy by itself, therefore, is another constraint that we can use in each step when solving sudoku which helps us reduce the set of possible solutions. But, in addition to that, when we implement this statregy we are using a constraint, that when two cells are twins, the rest of the cells of this unit can contain those numbers, and we propagate it for all units. Thus, naked twins use constraint propagation and it's used by sudoku as a constraint that is propagated.*

To enforce these rules, we use constraint propagation. As explained in [4], constraint satisfaction is the process of finding a solution to a set of constraints that impose conditions that variables must satisfy. A solution is therefore a set of values for the variables that satisfies all constraints. To converge toward that set of values, we repeatedly enforce the strategy rules, reducing the set of possible values toward a possible solution for the Sudoku. As explained in [5], this rule enforcement (a.k.a. transformation) is called constraint propagation.*

Constraint Propagation

As explained in [4], constraint satisfaction is the process of finding a solution to a set of 
constraints that impose conditions that variables must satisfy. 
A solution is therefore a set of values for the variables that satisfies all constraints. 
To converge toward that set of values, we repeatedly enforce the strategy rules, 
reducing the set of possible values toward a possible solution for the Sudoku. 
As explained in [5], this rule enforcement (a.k.a. transformation) 
is called constraint propagation.
   
   
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