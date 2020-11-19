# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This simulation is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine and simulates alternating levels of player difficulty.  Difficulty is determined by tree node search depth.

**Premise**
This is a game of taking teddy bears from bins.  For each game, the number of bins vary as do the number of bears.  This webGL game runs 100 simulations! Meaning, it will take around 2 minutes, hardware dependant, to finish.  In the end you will see the breakdown of games won for each player.

https://nohren.github.io/MiniMax-Tree-AI-simulation/

**Winning condition**
The player that leaves one last teddy bear in the bin wins.  In other words the player that takes the last teddy bear loses.  The goal is to influence the course of events so that the other player takes the last teddy bear.  The bots can see down the tree (future results of a decision) to make their decision.  It is important to note, that despite the path that a player takes, the enemy has a say, and the very next move will change that path, unless the path is "check-mate" i.e the other player has no viable winning options i.e boxed into a corner.  

**Difficulty level:**
 
 Easy - depth 3 
 
 Medium - depth 4 
 
 Hard - depth 5

**Inner Workings:**

On bot A's turn, it will look n depth down the tree, if it spots a winning condition it will select the path that leads to this condition on it's next move. 

On bot B's turn, it will look n depth down the **new** tree that has been generated based off of bot A's decision.  It will choose the most advantagous decision for bot B.

Both bot A and bot B possess advanced heuristic algorithms that can infer a winning condition based on a non winning conditions current state and future potential.

This process continues until there is only one teddy bear left and bot a or b loses by taking it.


**Results applicable to us :smiley:**


**Seize the initiative :runner: , it's a 1.5x advantage :point_right:**: Bot A won 1.5x more than Bot B of equal skill simply because Bot A goes first.  Taking the initiative forces player 2 into a corner from the get go.  If bot A is of greater skill forseeing the course of events (against equal skill from bot b), this advantage bumps up to 2x.


**Forsee the checkmate first! :raising_hand: Envision farther out than your opponent :see_no_evil:**: Bot B despite having lost the initiative, won more than A, when it had greater skill.  Meaning the advantage of initiative is cancelled out when the defensive opponent has greater skill foreseeing the future.

I define seeing the future as looking down the line on a possible move and assesing each action and resulting action for a future checkmate condition. Then doing this for each possible move right now.  In other words, forseeing all the depth on all the breadth.  

At this point there should be a decent path to choose. And ideally it's one containing a checkmate condition. 

This advantage becomes 1.5x (despite the loss of intiative) when skill is overmatched. ( :robot: Bot B - hard vs. Bot A- easy :see_no_evil:).  

Imagine what happens when you seize the initiative and practice forsight! :metal:

**The enemy always has a say:** After your move, the tree of options, breadth and depth is recreated for the other team, and the opponent may choose a different path than the one you initially set out on, the with the checkmate.  Especially if it is more advantageous to the opponent.  This means you will need to constantly adapt and practice forsight (generate new trees of action/consequence/action).


**Any additional insights that you see, just fork it!!**
