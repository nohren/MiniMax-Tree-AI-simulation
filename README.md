# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This simulation is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine and simulates alternating levels of player difficulty.  Difficulty is determined by tree node search depth.

**Premise**
This is a game of taking teddy bears from bins.  For each game, the number of bins vary as do the number of bears.  This webGL game runs 100 simulations! Meaning, it will take around 2 minutes, hardware dependant, to finish.  In the end you will see the breakdown of games won for each player.

https://nohren.github.io/MiniMax-Tree-AI-simulation/

**Winning condition**
The player that leaves one last teddy bear in the bin wins.  In other words the player that takes the last teddy bear loses.  The goal is to influence the course of events so that the other player takes the last teddy bear.  The bots can see down the tree (future results of a decision) to make their decision.  It is important to note, that despite the path that a player takes, the enemy has a say, and that the very next move will change that path, unless the path is "check-mate" (opposing player is out of viable options).



**Difficulty level:**
 
 Easy - depth 3 
 
 Medium - depth 4 
 
 Hard - depth 5

**Inner Workings:**

On bot A's turn, it will look n depth down the tree, it spots a winning condition through recursing a winning condition up from its leaves and depending on if the parent node is maximizing or minimizing, will transmit this winning condition making a path to the very next move of the player.  Bot A will take the path with the greatest value (1).

On bot B's turn, it will look n depth down the **new** tree that has been generated based off of bot A's decision.  It will choose the most advantagous decision for bot B, the path of lowest value, since it is minimizing.

Both bot A and bot B possess advanced heuristic algorithms that can infer a winning condition based on a non winning conditions current state and future potential.

This process continues until there is only one teddy bear left and bot a or b loses by taking it.

**Example Tree**

![image](https://drive.google.com/uc?export=view&id=1TmYRmUjQyiRQUbEfTMYjeanQE0k1RhO5)

<p>&nbsp;</p>

**Player 1's tree as seen printed in the Unity console (No minimax score because it has not been recursed yet)**

![image](https://drive.google.com/uc?export=view&id=1MukVgZ-4hZ0awSCrFkiOw6OVIGLXYBFj)

<p>&nbsp;</p>

**This is with MiniMax visualization**
![image](https://drive.google.com/uc?export=view&id=1ClKM6nRTqeKxNnG0Jk3NiNLcaJEmr8vO)




**Results applicable to us :smiley:**


**Seize the initiative :runner: , it's a 1.5x advantage :point_right:**: Bot A won 1.5x more than Bot B of equal skill simply because bot A goes first.  Taking the initiative forces player 2 into a corner from the get go.  If bot A is of greater skill forseeing the course of events, this advantage bumps up to 2x.


**Forsee the checkmate first! This boosts your advantage 3x :raising_hand: Envision farther out than your opponent :see_no_evil:**: Bot B despite having lost the initiative, won more than A, when it had greater skill.  Meaning the advantage of initiative is cancelled out when the defensive opponent has greater skill foreseeing the future.

**I define seeing the future as looking down the line vertically as well as horizontally on the next possible move and assesing each action and result for a future checkmate condition. In other words, forseeing all the depth on all the breadth.  Alternatively, in life, you can pick your ideal destination, then recurse back up from the depth to pick the next breadth decision that gets you there. But I digress!**

This advantage is 3x (despite the loss of intiative) when skill is overmatched. ( :robot: Bot B - hard vs. Bot A- easy :see_no_evil:).  It is a stronger advantage than initiative.

Imagine what happens when you seize the initiative and practice forsight! :metal:

**The enemy always has a say:** After your move, the tree of options, breadth and depth is recreated for the other team. And vice versa. A new tree is generated after each action/consequence cycle.  When done intentionally, this is what we call forcefully "boxing in" your opponent or intentionally reducing the acceptable options they have to choose from. Eventually they are out of good options and you win.

**Sample data - Numbers represent wins...      Random Range of bins (2-6), random range of bears (1-6), 100 games, 8 different difficulty categories. Results are as expected.**

![image](https://drive.google.com/uc?export=view&id=1yb47WSTStES85KPqYH2O5dN5fWrn9fgr)

<p>&nbsp;</p>

**My Crude drawing of forcing the check mate.  In this simple scenario, if you go first you win, assuming you know how the game is played!**
![image](https://drive.google.com/uc?export=view&id=1g8EQ5cubcqwOBaRYJs4h8uaUj6msO1DI)

**Any additional insights that you see, just fork it!!**
