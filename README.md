# :evergreen_tree: MiniMax-Tree-AI-simulation :robot:
This simulation is based off of the "Don't take the last Teddy" game by Dr. Tim "Dr. T" Chamillard.  It is played machine against machine and simulates alternating levels of player difficulty.  This "game" is simply for game theory observation and has no controls.

**Premise**
For each game, the number of bins vary as do the number of bears. The player that takes the last teddy bear loses.  The goal is to force your opponent into that position. This webGL game runs 100 simulations! Meaning, it will take around 2 minutes, hardware dependant, to finish.  In the end you will see the breakdown of games won for each AI player.

https://nohren.github.io/MiniMax-Tree-AI-simulation/

**Difficulty level:**
 
 Easy - depth 3 
 
 Medium - depth 4 
 
 Hard - depth 5
"check-mate" (opposing player is out of viable options).
**Inner Workings:**

On player 1's turn, it will look n depth down the tree, it can spot a winning condition through recursion.  A winning condition is recursed up from its leaves, depending on if the next node higher likes that condition (maximizing or minimizing), and will transmit the winning condition to the top of the tree.  Player 1 will take the path with the greatest value (1).

On player 2's turn, it will look n depth down the **new** tree that has been generated after the action and result of player 1's move.  It will choose the most advantagous decision, the lowest value, since it is minimizing.

Both player 1 and player 2 have heuristics that can infer a winning condition from non winning conditions.

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


**Seize the initiative :runner: , it's a 1.5x advantage :point_right:**: Bot A won 1.5x more than Bot B of equal skill simply because bot A goes first.  (caveat unless they are both of easy skill- this why forsight is more valueable).  Taking the initiative forces player 2 into a corner from the get go.  If bot A is of greater skill forseeing the course of events, this advantage bumps up to 2x.


**Forsee the checkmate first! This boosts your advantage 3x :raising_hand: Envision farther out than your opponent :see_no_evil:**: Bot B despite having lost the initiative, won more than A, when it had greater skill.  Meaning the advantage of initiative is cancelled out when the defensive opponent has greater skill foreseeing the future.

**I define seeing the future as looking down the line vertically as well as horizontally on the next possible move and assesing each action and result for a future checkmate condition. In other words, forseeing all the depth on all the breadth.  Alternatively, in life, you can pick your ideal destination, then recurse back up from the depth to pick the next breadth decision that gets you there. But I digress!**


Imagine what happens when you seize the initiative and practice forsight! :metal:

**The enemy always has a say:** After your move, the tree of options, breadth and depth is recreated for the other team. And vice versa. A new tree is generated after each action/result cycle.  When done intentionally, this is what we call forcefully "boxing in" your opponent or intentionally reducing the acceptable options they have to choose from. Eventually they are out of good options and you win.

**Sample data - Numbers represent wins...      Random Range of bins (2-6), random range of bears (1-6), 100 games, 8 different difficulty categories. Results are as expected.**

![image](https://drive.google.com/uc?export=view&id=1yb47WSTStES85KPqYH2O5dN5fWrn9fgr)

<p>&nbsp;</p>

**My Crude drawing of forcing the check mate.  In this simple scenario, if you go first you win, assuming you know how the game is played!**
![image](https://drive.google.com/uc?export=view&id=1g8EQ5cubcqwOBaRYJs4h8uaUj6msO1DI)

**Any additional insights that you see, just fork it!!**
