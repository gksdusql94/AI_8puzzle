# 8-Puzzle Solver

## Overview

This project implements an AI-based 8-puzzle solver using various search algorithms. The solver is capable of solving the 8-puzzle using three different search methods: Breadth-First Search (BFS), Depth-First Search (DFS), and A* Search with heuristic functions. The program outputs statistics about the search performance, including the path to the goal, number of expanded nodes, and memory usage.

## Algorithms Implemented
- **Breadth-First Search (BFS):** Explores nodes level by level, using a queue to store nodes.
- **Depth-First Search (DFS):** Explores as far as possible along a branch before backtracking, using a stack for node storage.
- **A* Search (AST):** Uses a heuristic function (Manhattan distance) to estimate the cost of reaching the goal and minimizes the total estimated cost.

## How to Run

### Prerequisites
- Python 3.x

### Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/gksdusql94/AI8_puzzle.git
   cd 8_puzzle

2. Run the program with the desired search method:
'''bash
python3 8_puzzle.py <method> <input_board>
<method>: The search method to use (bfs, dfs, ast).
<input_board>: The initial board configuration, provided as a comma-separated string of numbers 0-8 where 0 represents the blank space. For example: 1,2,3,4,5,6,7,8,0.
Example usage:
'''bash
python3 8_puzzle.py bfs 1,2,3,4,5,6,7,8,0

### Output
The output file (output.txt) will contain the following information:

Path to goal: The sequence of moves required to solve the puzzle.
Cost of path: The number of moves taken to reach the goal.
Nodes expanded: The total number of nodes expanded during the search.
Search depth: The depth at which the goal was found.
Maximum search depth: The maximum depth reached during the search.
Running time: The time taken to complete the search.
Maximum RAM usage: The maximum memory used during the search.

### Example Output
'''bash
Input: bfs 1,2,3,4,5,6,7,8,0
path_to_goal: ['Left', 'Up']
cost_of_path: 2
nodes_expanded: 5
search_depth: 2
max_search_depth: 4
running_time: 0.0021
max_ram_usage: 10.23 MB

### Notes
The goal state is considered to be 0,1,2,3,4,5,6,7,8, where 0 represents the blank space.
The program uses Manhattan distance as the heuristic for A* search.
