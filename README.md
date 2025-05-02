
# AI Maze Pathfinding & MDP Solver

This project demonstrates maze generation and pathfinding using classic search algorithms (BFS, DFS, A*) and decision-making algorithms from Markov Decision Processes (Value Iteration and Policy Iteration). The project includes performance comparisons across multiple metrics including path length, search cost, memory usage, and execution time.

---

## 🧩 Features

- **Maze Generation** using Randomized Kruskal’s Algorithm
- **Pathfinding Algorithms**:
  - Breadth First Search (BFS)
  - Depth First Search (DFS)
  - A* Search with Manhattan Heuristic
- **Markov Decision Process (MDP) Solvers**:
  - Value Iteration
  - Policy Iteration
- **Visualization** of paths using Pygame
- **Performance Metrics**:
  - Path complexity
  - Wall density
  - Explored nodes
  - Final path length
  - Execution time
  - Memory usage

---

## 📁 File Structure

```
.
├── AI_Assignment_astar.ipynb
├── AI_Assignment_bfs.ipynb
├── AI_Assignment_dfs.ipynb
├── AI_Assignment_maze_generator.ipynb
├── AI_Assignment_mdp_policy_iteration.ipynb
├── AI_Assignment_mdp_value_iteration.ipynb
├── Mazes/
│   └── [10.npy, 20.npy, ..., 200.npy]  # Pre-generated mazes
├── Paths/
│   └── BFS_30.png, DFS_30.png, etc.   # Visual outputs
├── results.csv                        # Performance metrics
├── results_final.csv                 # Final summarized results
└── README.md
```

---

## 🧠 Algorithm Overview

### Maze Generator:
- **Algorithm**: Randomized Kruskal’s
- **Output**: Saves mazes of various sizes in `.npy` format

### Search Algorithms:
- **BFS**: Explores level-by-level, guarantees shortest path in unweighted graphs
- **DFS**: Goes deep into one path before backtracking, not optimal for shortest path
- **A***: Uses `f(n) = g(n) + h(n)`, where `h(n)` is Manhattan distance

### MDP Solvers:
- **Value Iteration**: Computes value functions iteratively using Bellman updates
- **Policy Iteration**: Iteratively evaluates and improves the policy

---

## ⚙️ How to Run

1. Ensure Python and the following libraries are installed:
   ```bash
   pip install numpy pygame pandas pillow
   ```

2. Run the maze generator:
   ```bash
   python AI_Assignment_maze_generator.ipynb
   ```

3. Run each algorithm notebook (`.ipynb`) individually to visualize paths and compare metrics:
   - `AI_Assignment_bfs.ipynb`
   - `AI_Assignment_dfs.ipynb`
   - `AI_Assignment_astar.ipynb`
   - `AI_Assignment_mdp_value_iteration.ipynb`
   - `AI_Assignment_mdp_policy_iteration.ipynb`

---

## 📊 Evaluation Criteria

Each algorithm is evaluated based on:
- **Execution Time**
- **Memory Usage**
- **Number of Explored Nodes**
- **Final Path Length**
- **Wall Density**
- **Path Complexity** (dead ends, branching)

---

## 📌 Observations

- **A\*** performs best in terms of execution time and optimality.
- **DFS** is fastest but has longer paths.
- **Value Iteration** in MDPs uses the least memory and is most scalable.
- **Policy Iteration** is less efficient on larger grids.

---

## 🏁 Conclusion

- For known goal states and optimization, **MDP Value Iteration** is ideal.
- For unknown goals or exploratory scenarios, **A\*** is the best compromise.
- Visual outputs and performance metrics are saved for easy comparison.
