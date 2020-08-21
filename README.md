# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This simulation is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine.  It simulates alternating levels of difficulty.  Player difficulty is determined by tree node search depth.

**Premise**
This webGL game runs 100 simulations! it will take around 2 min hardware dependant to finish.  In the end you will see the breakdown of winning games for each player.

https://orennelson.github.io/MiniMax-Tree-AI-simulation/

**Winning condition**
The player that takes the last teddy bear loses.  The other player wins.  The goal is to influence the course of events so that the other player takes the last teddy bear.  The bots can see down the tree (future results of a decision) to make their decision.  It is important to note, that despite the path that a player takes, the enemy has a say, and the very next move will change that path, unless the path is "check-mate" i.e the other player has no viable winning options i.e backed into a corner.  

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

Observation 1: 

**Seize the initiative, it's a 1.5x advantage**: Bot A won 1.5x more than Bot B of equal skill simply because Bot A goes first.  Taking the initiative forces player 2 into a corner from the get go.  If bot A is of greater skill forseeing the course of events (against equal skill from bot b), this advantage bumps up to 2x.

Observation 2:

**Forsee the checkmate first! Envision farther out than your opponent**: Bot B despite having lost the initiative, won more than A, when it had greater skill.  Meaning the advantage of initiative is cancelled out when the defensive opponent has greater skill foreseeing the future i.e seeing each players choices down the line into the future and the checkmate condition if one exists.  In other words, forseeing all the depth on all the breadth.  Then choosing the path with the checkmate.  This increases to 1.5x advantage despite the loss of intiative when skill is overmatched. ( Bot B - hard vs. Bot A- easy).  Imagine what happens when you seize the initiative and forsee the checkmate first.


