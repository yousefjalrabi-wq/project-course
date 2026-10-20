---
project_outline: "[[00-project/01-project-outline]]"
---

# Procedural Generation and Automatic Evaluation of Game Levels

## 1. Actors and permissions

| Role | Needs | Responsibility / access |
| --- | --- | --- |
| User | Generate mazes and see their results | Chooses settings, starts generation, and views measurements |

The first version is a simple Python tool for one user. No accounts or special permissions are needed.

## 2. Use cases / user stories

### Generate and evaluate mazes
- **Actor:** User
- **Precondition:** The Python program is ready to run.
- **Main flow:**
  1. The user chooses Recursive Backtracking or Randomized Prim.
  2. The user chooses the maze size and a random seed.
  3. The program generates a 2D grid maze with a start and an exit.
  4. The program measures the maze's shortest path, dead ends, corridors, and branching.
  5. The program calculates an estimated difficulty score and shows the results.
- **Alternative / error flow:** If the maze size or another input is invalid, the program displays an error and asks for a valid value.
- **Postcondition:** A generated maze and its evaluation results are available.

### Compare the two algorithms
- **Actor:** User
- **Precondition:** Both algorithms can generate and evaluate mazes.
- **Main flow:**
  1. The user selects the settings for a comparison.
  2. The program generates multiple mazes with each algorithm using recorded random seeds.
  3. The program calculates the same measurements for every maze.
  4. The program compares the results, including averages and variation.
- **Alternative / error flow:** If a run fails, the program reports the problem rather than treating the missing result as valid.
- **Postcondition:** The user can see how the two algorithms compare.

## 3. Functional requirements

| Requirement | Acceptance criteria | Priority |
| --- | --- | --- |
| The user can choose one of two maze-generation algorithms. | The program accepts Recursive Backtracking or Randomized Prim and uses the selected method. | Must |
| The user can set the maze size and random seed. | The program uses valid input settings and rejects invalid sizes. | Must |
| The program generates a 2D grid maze. | The generated maze has walls, passages, a start, and an exit. | Must |
| The program measures the shortest solution path. | The program finds and reports the shortest path from start to exit. | Must |
| The program measures maze structure. | The program reports dead ends, corridor lengths, and branching points. | Must |
| The program calculates an estimated difficulty score. | The program applies a clearly explained formula to the measurements and reports the score. | Must |
| The program compares both algorithms over multiple mazes. | It reports results for each algorithm and compares averages and variation. | Must |
| The program records generation time. | It reports how long each maze took to generate. | Should |
| The program displays a simple maze visualization. | The user can view a generated maze as a grid. | Should |

**Priority:** **Must** = required; **Should** = useful if time allows.

## 4. Business rules and constraints

| Rule or constraint | Reason |
| --- | --- |
| Mazes use a 2D grid of cells and walls. | Keeps generation and measurement simple. |
| Every generated maze has a defined start and exit. | Makes shortest-path measurement possible. |
| Both algorithms are tested using the same maze sizes and evaluation methods. | Makes comparisons fair. |
| The random seed is recorded for each maze. | Allows a result to be reproduced. |
| The difficulty score is an estimate, not a proven measure of human difficulty. | Maze difficulty can depend on the player and solving method. |
| The project focuses on generating and evaluating mazes, not building a full game. | Keeps the project manageable. |

## 5. User interface and workflow

The first version will use a simple Python interface, such as text input and printed results. The user chooses an algorithm, maze size, and random seed. The program generates the maze, measures its structure, and displays the results. The user can also run a batch of mazes to compare Recursive Backtracking and Randomized Prim. A simple grid drawing may be added to make the results easier to understand.

## 6. Non-functional requirements

| Requirement | How it will be verified |
| --- | --- |
| Repeating a run with the same algorithm, settings, and seed produces the same maze. | Run the same inputs twice and compare the generated grids. |
| Measurements are calculated consistently. | Test small mazes where the shortest path and dead ends can be checked manually. |
| Invalid inputs are handled clearly. | Try an invalid maze size and check that the program reports an understandable error. |
| Comparison results can be repeated. | Save the settings and seeds used, then rerun the comparison. |
| The code is easy to understand and maintain. | Keep generation, measurement, and comparison in separate Python functions. |

## 7. Open questions and risks

| Question / risk | Impact | Owner | Resolution / decision |
| --- | --- | --- | --- |
| How should the difficulty score be calculated? | Different formulas may give different rankings. | Student | Start with a simple formula using selected measurements; explain its limitations. |
| Does the score reflect actual solving effort? | A structural score may not match how hard a maze is to solve. | Student | Compare the score with the effort required by one clearly defined solving method. |
| How many mazes are enough for comparison? | Too few examples may give misleading results. | Student | Start with 100 mazes per algorithm for each tested configuration and compare averages and variation. |
| How should the algorithms' optional settings be handled? | Different settings may change maze structure. | Student | First compare both algorithms with basic settings; add one simple variation only if feasible. |
