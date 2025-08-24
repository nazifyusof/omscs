# Search

## Challenge 1
![img.png](img/img_1.png)

The answer is None of the above. We can use tri-directional search, with A*, with three simultaneous searches from each of the three nodes. The search will stop when any two of the three searches meet.

## Challenge 2
![img.png](img/img_2.png)

IDA* is a combination of depth-first search and A* search. It performs a series of depth-limited searches, increasing the depth limit with each iteration based on the cost function f(n) = g(n) + h(n), where g(n) is the cost to reach node n and h(n) is the heuristic estimate to the goal. This allows IDA* to use less memory than traditional A* while still finding an optimal solution.

Readings: https://www.cs.princeton.edu/courses/archive/fall06/cos402/papers/korfrubik.pdf

## Definition of a problem
- Initial State
- Action(s) -> Set of possible actions {a1, a2, ...}
- Result(s,a) -> s'
- Goal Test(s) -> True/False
- Path Cost(s -> s -> s) -> n, or Step Cost(s,a,s') -> n

## Route Finding
- Frontier = The endpoints of paths we have explored but not yet expanded
- Explored = Set of nodes already explored
- Unexplored = Set of nodes not yet explored

## Tree/Graph Search 
- As we start to explore the state, we keep track of the frontier and explored set to avoid duplicates or cycles.
 
### Breadth-First Search(BFS)
- The algorithms only stops when the destination is removed from the frontier. The reason is because it might not be the shortest path to the destination if we stop when we first reach it.
- BFS is optimal, guaranteed to find the cheapest path to the goal
- Frontier is a by level if visualized as a tree, FIFO queue
- BFS is complete, guaranteed to find a solution if one exists, assuming finite branching factor and finite depth of solution

### Uniform-Cost Search (UCS), cheapest-first
- Start with lowest total cost path
- UCS continues to search until we pop the goal node from the frontier. We continue looking to see if there is a cheaper path to the goal node.
- UCS is optimal, guaranteed to find the cheapest path to the goal
- Frontier is more complex than BFS, as it is ordered by path cost
- UCS is complete, guaranteed to find a solution if one exists, assuming finite branching factor and finite step cost > 0
- 

### Depth-First Search (DFS)
- DFS is not optimal. It can also give suboptimal solutions. 
- Frontier is a stack, LIFO
- DFS is not complete, it can get stuck in infinite loops. We can use depth-limited search to solve this problem.

### Greedy Best-First Search
- Moves towards the goal, but does not consider the cost to reach the node
- If there's a barrier, it will move around it, but it might not be the optimal path
- Solved by A* search

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