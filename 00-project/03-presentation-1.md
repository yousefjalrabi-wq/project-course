---
project_outline: "[[00-project/01-project-outline]]"
---

<!-- 5xl -->
# Procedural Generation and Automatic Evaluation of Game Levels

Author: Yousef Jihad Alrabi  
Neptun: TWIRXA  
Supervisor: Péter Novák  
Project ID: 2026-NP-02

---

## Procedural generation

- Automatically creates game content using algorithms
- Uses parameters and random seeds to produce different levels
- This project focuses on 2D mazes

---

## Problem

- Manually designing many game levels takes time
- Automatically generated mazes may differ in structure and complexity
- Solvability alone cannot distinguish their difficulty
- We need automatic, measurable evaluation and comparison

---

## Target users

- Game developers experimenting with generated maze levels
- Students and researchers studying procedural generation
- Developers comparing generation methods and parameter settings

---

## Planned scope: 2D mazes

- 2D grid of walls and walkable passages
- Start and exit locations for measuring solution paths
- Maze generation, automatic evaluation, and comparison
- A complete playable game is outside the scope

---

## Planned scope: generation algorithms

**Recursive Backtracking (randomized DFS)**
- Extends a path and backtracks when no unvisited neighbour remains

**Randomized Prim**
- Expands a growing maze using randomly selected frontier options

- Compare the resulting maze structures

---

## Planned scope: evaluation

- Shortest solution-path length
- Dead-end count and proportion
- Corridor lengths and structure
- Branching and junctions
- Generation time as an additional comparison measure

---

## Planned scope: estimated difficulty

- Develop a combined score from structural measurements
- Compare estimated difficulty across generated mazes
- Investigate how well the score reflects a specified solving strategy's effort
- The formula and its validation are still to be finalized

---

## Initial user journeys

1. Choose a generation algorithm and parameters
2. Generate one or more mazes using recorded random seeds
3. Check validity and compute structural metrics
4. Estimate difficulty and inspect representative mazes
5. Compare results between algorithms and configurations

---

## Next steps

- Finalize generation parameters and difficulty-model approach
- Write the detailed specification and evaluation criteria
- Implement and test both generators and the metrics
- Initially generate 100 mazes per configuration
- Compare distributions and variability across settings
- Investigate whether parameters can influence estimated difficulty
