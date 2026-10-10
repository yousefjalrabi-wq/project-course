---
name: Yousef Jihad Alrabi
neptun: TWIRXA
id: 2026-NP-02
project_outline: "[[00-project/01-project-outline]]"
---

# Procedural Generation and Automatic Evaluation of Game Levels

## 1. Project Overview
The project will implement a Python-based tool for generating and evaluating 2D grid-based mazes. Two generation algorithms, Recursive Backtracking and Randomized Prim, will be compared using measurable structural properties and an estimated difficulty score.

## 2. Maze Representation
Each maze will be represented as a rectangular grid of cells and walls. A fixed starting cell and goal cell will be used for evaluation. The maze dimensions and random seed will be configurable.

## 3. Generation Algorithms
### Recursive Backtracking
A randomized depth-first search algorithm that creates a maze by visiting neighboring cells and removing walls between them. The implementation will support a configurable preference for continuing in the same direction.

### Randomized Prim
A maze generation algorithm that starts from one cell and repeatedly connects a frontier cell to the growing maze. Frontier selection will be configurable to investigate its effect on maze structure.

## 4. Automatic Evaluation
The generated mazes will be assessed using:
- Shortest solution path length between start and goal.
- Number and proportion of dead ends.
- Corridor length characteristics.
- Branching points and branching frequency.
- Validity and connectivity checks.

## 5. Estimated Difficulty
A compound difficulty score will be investigated using normalized structural measurements. The precise formula and weights will be selected and justified during implementation. The score will be compared with the effort required by a defined maze-solving strategy. It will be treated as an estimate rather than a direct measurement of human difficulty.

## 6. Experiments
Both algorithms will be tested using multiple maze sizes, random seeds, and generation parameter settings. The initial target is 100 mazes per configuration. Results will be summarized using distributions, averages, and variability, with representative maze examples.

## 7. Technologies
- Python for generation, evaluation, and experiments.
- GitHub for version control and documentation.
- Trello for organizing tasks and tracking progress.

## 8. Expected Results
The project is expected to produce working maze generators, automatic measurement functions, a proposed difficulty model, and experimental comparisons showing how algorithms and parameters affect maze structure and estimated difficulty.

## 9. Limitations
The project will focus on 2D grid mazes, not a complete playable game. The difficulty score will not be assumed to predict every human player's experience.
