# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This game is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine.  It simulates alternating levels of difficulty.  Player difficulty is determined by tree node search depth.

**Premise**
This webGL game runs 100 simulations! it will take around 2 min hardware depdant to finish.  In the end you will see the breakdown of winning games for each player.

**Winning condition**
The player that takes the last teddy bear loses.  The other player wins.  The goal is to influence the course of events to the other player takes the last teddy bear.  The bots can see down the tree to see who will take the last one to make their choices.  It is important to note, that despite the path that a player takes, the enemy has a say, and the very next move can change that path.  

**Difficulty level:**
 
 Easy - depth 3 
 
 Medium - depth 4 
 
 Hard - depth 5

**Inner Workings:**

On bot A's turn, it will look n depth down the tree, if it spots a winning condition it will select the path that leads to this condition on it's next move. 

On bot B's turn, it will look n depth down the **new** tree that has been generated based off of bot A's decision.  It will choose the most advantagous decision for bot B.

Both bot A and bot B possess advanced heuristic algorithms that can infer a winning condition based on a non winning conditions current state and future potential.

This process continues until there is only one teddy bear left and bot a or b loses by taking it.


**Results**
Observation 1: **Seizing the initiative is a HUGE advantage**: Bot A won more than Bot B of equal or lesser skill simply because Bot A goes first.
