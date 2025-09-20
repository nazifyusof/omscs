# Game Playing

## Readings
week 3: 
- Game Playing through Depth-limited Search; game play vs. an opponent in Isolation;
- AIMA: Chapter 1-2 
- AIMA: Chapter 5.0-5.2
- R&N slides on Game Playing(https://faculty.cc.gatech.edu/~thad/6601-gradAI-fall2015/chapter06.pdf)

week 4:
- AIMA: Chapter 5.3-5.7
- handout on Alpha-Beta Pruning: https://faculty.cc.gatech.edu/~thad/6601-gradAI-fall2015/Korf_Multi-player-Alpha-beta-Pruning.pdf 

## Game of isolation
- https://static.us.edusercontent.com/files/4Nqr21BMCjFKLgnwbCQgh9i9
- To avoid bad first move, we will keep the table of best moves, called opening book

## Min and Max Algorithm
- Min level is when it is the opponent's turn
- Max level is when it is our turn
- Top of the tree is always gonna be a max level
- For each max node, pick the max value of its children
- For each min node, pick the min value of its children
- Middle has 16 possible moves in third moves
- Nodes MINIMAX will need to visit
  - b^d, where b is the branching factor and d is the depth of the tree
- In 5x5, average branching factor is 8
  - 8^25 = 1.2 million years, need to be faster!

## Depth-limited Search
- Only go to a certain depth, x < 10.3
- To be safe, go to depth 9 max
- What happen at level 9?
  - We need to evaluate the goodness of a node at level 9 based on how much we expect to win from that position
- We want an evaluation function that returns a higher number depending on how good the board is for computer player
- We call the evaluation function as Number My Moves
- The evaluation of my_moves above is different for depth 2 and 3
  - At depth 2, winning moves has lower scores
  - Is the function bad? No, it is just that the depth is too low

## Quiescent Search
- If we find a branch where our computer loses, we give a score of -1, if it wins, we give a score of +100
  - After level 3, weve reached a quiescent state, recommended branches are not changing much
- Often time will give better result, at the beginning of the game, or at the end of the game

## Iterative Deepening
- Iterative deepening doesnt waste much time. 
  - Because of the exponential nature of the problem, the amount of time is dominated by the last level searched
- With Iterative Deepening, 
  - We are going to serch the level 1 and get an answer for what we think is the best move. We keep the answer incase we run out of time
  - We''ll start the process again, but this time we will search to level 2
  - If we finish searching level 2 before time is up, we keep it's best move and restart searching level 3
  - We'll continue this process until we run out of time and return the best move found so far
  - We should do the same thing we did to determine quiescence, and quiescence is a good side effect of iterative deepening

## Understanding exponential time, branching factor b = 2
- Level 0: 1 Tree Nodes, 1 Iterative Deepening Nodes
- Level 1: 3 Tree Nodes, 4 Iterative Deepening Nodes
- Level 2: 7 Tree Nodes, 11 Iterative Deepening Nodes
- Level 3: 15 Tree Nodes, 26 Iterative Deepening Nodes
- Level 4: 31 Tree Nodes, 57 Iterative Deepening Nodes
- Level 5: 63 Tree Nodes, 120 Iterative Deepening Nodes
-  b = 2, Tree Nodes n = 2^(d+1) - 1, Iterative Deepening Nodes = <2n

## Understanding exponential time, branching factor b = 3
- Level 0: 1 Tree Nodes, 1 Iterative Deepening Nodes
- Level 1: 4 Tree Nodes, 5 Iterative Deepening Nodes
- Level 2: 13 Tree Nodes, 18 Iterative Deepening Nodes
- Level 3: 40 Tree Nodes, 58 Iterative Deepening Nodes
- Level 4: 121 Tree Nodes, 179 Iterative Deepening Nodes
- b = 3, Tree Nodes n = (3^(d+1) - 1)/2, Iterative Deepening Nodes = <2n
- b = k, Tree Nodes n = (k^(d+1) - 1)/(k-1), Iterative Deepening Nodes = <2n

## Horizon Effect
- The computer player cannot see far enough into the future to solve a problem

## Good eval functions
- Number of opponent's moves: it would label board as good when oppo has more moves
- squares remaining: constantly decreasing with each moves
- squares remaining - my moves: penalize computer player with more potential moves
- my moves - opponent's moves: good isolation function, penalize boards where opponent has more moves

## Evaluating eval functions
- my moves - 2 * opponent's moves: good eval function: cause computer player to chase opponent around the board

## Alpha-Beta Pruning
- Pruning technique to allow us ignore the whole section of the tree that we know will not affect the final decision
- In min level, if we find a value that is less than the best value found so far at a max level, we can prune the rest of the children of this min node
- b^(d*alpha-beta) in best case

## 5x5 Analysis
- Alpha-beta pruning, symmetry and see players split across half the board(check remaining moves) helps to determine faster
- Player one can win easily by moving to the center of the board, then do 180 degree of oppnents moves
  - How does player 2 defend against this?
    - By moving to a location where player 1 cannot reflect
    - There are 8 such locations
- It's better to be the player two
  - Create a great book of opening moves
  - if a player doesn't occupy the center square, the other player can take it and win easily
- Once you have a a good opening book;
  - use your understanding of equivalent moves and hash tables to load and search efficiently
  - After exhausting book of opening moves, implement minimax, add iterative deepening and alpha-beta pruning
  - Focus on evaluation function
    - Up to us to decide

## 3 player alpha beta pruning

## Sloppy Isolation

## Sloppy Isolation EXPECTIMAX


## 

## 

## 

## 

## 

## 

## 

## 

## 

## 



