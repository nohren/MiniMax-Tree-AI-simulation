# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This game is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine.  It simulates alternating levels of difficulty.  Player difficulty is determined by tree node search depth.

**Difficulty level:**
Depth: 3 - Easy
Depth: 4 - Medium
Depth: 5 - Hard

**Simulation:**

On bot A's turn, it will look n depth down the tree, if it spots a winning condition it will select the path that leads to this condition on it's next move. 

On bot B's turn, it will look n depth down the **new** tree that has been generated based off of bot A's decision.  It will choose the most advantagous decision for bot B.

Both bot A and bot B possess advanced heuristic algorithms that can infer a winning condition based on a non winning conditions current state and future potential.

This process continues until there is only one teddy bear left and bot a or b loses by taking it.
