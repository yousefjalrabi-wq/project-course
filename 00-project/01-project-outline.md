---
name: Yousef Jihad Alrabi
neptun: TWIRXA
id: 2026-NP-02
github: https://github.com/yousefjalrabi-wq/project-course
trello: https://trello.com/b/55dO87X2/2026-np-02-thesis-project
---
# Procedural Generation and Automatic Evaluation of Game Levels

This project investigates procedural generation and automatic evaluation of 2D grid-based mazes. It compares Recursive Backtracking (randomized depth-first search) with Randomized Prim's algorithm. Generated mazes will be measured using structural metrics, and a proposed estimated-difficulty model will be investigated through reproducible experiments with different parameters and random seeds.

## Objectives
- **Primary objective:** Implement and compare two maze-generation algorithms and develop an automatic evaluation approach for the generated mazes.
- **Target users / stakeholders:** Game developers, students, and researchers studying procedural generation; project supervisor.
- **Measurable success criteria:** Generate valid, connected mazes with both algorithms; calculate solution-path length, dead-end proportion, corridor characteristics, and branching; report distributions across multiple seeds and parameter settings; investigate whether parameter changes influence estimated difficulty.
- **Constraints:** 2D grid-based maze representation; core generation and evaluation algorithms implemented and understood by the student; reproducible experiments; version-controlled source code. The estimated-difficulty model must be justified and its limitations explained.

## Scope
### In scope
- Generating 2D grid-based mazes using Recursive Backtracking and Randomized Prim.
- Configurable maze size, random seeds, and selected generation parameters.
- Validity and connectivity checks.
- Structural measurements, including shortest solution path, dead ends, corridor structure, and branching.
- A proposed compound estimated-difficulty score and evaluation of its relationship to a specified solving strategy's effort.
- Experiments across multiple configurations, initially 100 mazes per configuration, with statistical comparisons and representative maze visualizations.

### Out of scope
- A complete playable video game.
- Polished graphics or a 3D game world.
- Claims that estimated difficulty exactly predicts every human player's experience.

## Notes
The exact difficulty formula, its weights and validation procedure, and additional generation parameter settings will be finalized during specification. The initial implementation language is planned to be Python. Experimental results will be reported with variability and limitations, not only averages.
