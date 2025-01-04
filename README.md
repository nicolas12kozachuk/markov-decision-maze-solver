# Maze Solver Using Markov Decision Processes

## Project Description

This project implements a **Maze Solver** using **Markov Decision Processes (MDPs)**. The solver finds the optimal path in a maze by modeling it as an MDP with states, actions, transition probabilities, and rewards. The value iteration algorithm is used to calculate the optimal policy that guides the agent from the starting point to the goal. A study of the execution time for the maze solver is also performed.

### Key Features
- **States**: Represent each cell in the maze as open space (1) or wall (0).
- **Actions**: Include moving up, down, left, and right within the maze boundaries.
- **Transition Probabilities**: Encoded in matrices based on the feasibility of moves.
- **Rewards**: Defined to encourage optimal paths and discourage invalid moves.

## Code Details

The implementation, provided in the `Markov_Decision_Maze_Solver_MxN.ipynb` notebook, includes:
1. **Maze Representation**: Defines the maze as an \(M \times N\) grid.
2. **MDP Formulation**:
   - Transition matrices for each action (Up, Down, Left, Right).
   - Reward matrices that scale with maze size.
3. **Value Iteration Algorithm**:
   - Iteratively calculates state values until convergence.
   - Outputs the optimal policy for navigating the maze.
4. **Visualization**: Displays the maze and the solution path.

### Example Outputs
- The solver works for mazes of varying sizes, e.g., 5x5, 10x10, and 25x25 grids.
- Execution times scale exponentially with the number of states due to the complexity of value iteration.

## Study of Execution Time

A detailed study of execution time was conducted for mazes of various sizes. The results show:
- Execution time increases exponentially with the number of states due to the nested loops in value iteration.
- For an \(N \times N\) maze, the execution time approximately follows:
  \[
  T(N) = 3e^{2N}
  \]

### Sample Execution Times:
| Maze Size | Average Time (s) |
|-----------|------------------|
| 5x5       | 1.2             |
| 10x10     | 21.2            |
| 15x15     | 64.4            |
| 20x20     | 167.2           |
| 25x25     | 428.8           |

These findings highlight the limitations of value iteration for larger mazes and the need for more efficient algorithms for scalability.

## Results Summary

- **Performance**: Efficiently finds paths for small to medium-sized mazes.
- **Execution Time**: Grows exponentially with maze size.
- **Visualization**: Outputs the maze with the optimal solution path highlighted.

## Files

- `Markov_Decision_Maze_Solver_MxN.ipynb`: The code for the solver, including implementation details.
- `Maze Solver Using Markov Decision Processes Report.pdf`: Detailed explanation of the methodology and results.

## How to Run

1. Open the Jupyter Notebook (`Markov_Decision_Maze_Solver_MxN.ipynb`).
2. Modify the maze dimensions (M and N) as desired.
3. Run the notebook to compute the solution and visualize the output.

## Dependencies
- Python 3.x
- Jupyter Notebook
- Required libraries: NumPy, Matplotlib

## References
The project is based on the theory of Markov Decision Processes and value iteration, leveraging matrix-based representations for transitions and rewards.

---

For more details, refer to the report or the codebase.
