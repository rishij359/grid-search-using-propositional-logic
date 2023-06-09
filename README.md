# Logical Agent for Landmine World: Finding Gold using Propositional Logic and SAT Solver

## Problem statement

<img src="img\Grid.png" width="500">

The figure above shows a Land mine world containing several land mines. There is an agent in room [1,1]. The goal of the agent is to find the location of gold in the Land mine world. The agent “knows” that gold is present in a room if and only if the room has four adjacent rooms each having a landmine (see the figure above). So, gold cannot be present in any of the rooms along the boundary of the Land mine world. The agent is able to detect a land mine from the rooms that are adjacent to the room containing the land mine. There are four possible percepts that the agent can have: 0, 1, 2 and 3. The percept n means that n number of adjacent rooms have a land mine. (A percept value of 4 will not be possible because the agent will not be able to reach such a room.) In the figure shown above, if the agent is in room [2,1], then it will perceive 1. If the agent is in room [3,2], then the percept will be 2. In room [1,3], the percept will be 0. The agent only needs to find the location of the room that contains gold. It is possible that after visiting all the “safe” rooms agent is unable to infer the location of gold. So, the two possible outputs of your program will be:
1. Gold is present in room [x,y].
2. Gold could not be detected after visting all the safe rooms.

Write a python program that uses propositional logic sentences to check which rooms are safe. The inference should be drawn using the SAT solver python-sat 1 . The logical agent can take four actions: Up, Down, Left and Right. These actions help the agent move from one room to an adjacent room. You may assume that land mine will not be present in room [1,1]. Safe room is a room that you are sure (through logical inference) that it does not contain a land mine. While trying to move from the current room to an unvisited safe room, you can use breadth first search to find the shortest path (through the previously visited safe rooms). If there are no unvisited safe rooms left and Gold cannot be inferred, then the program should give the output 2 mentioned above. Instead of symbols, you must use integers because the SAT solvers use positive and negative integers to stand for positive and negative literals.

## Discription of the solution

The project implemented a logical agent that uses propositional logic sentences to check which rooms are safe in a Landmine world. The agent is equipped with a SAT solver python-sat to infer the location of gold. The agent can only detect landmines from adjacent rooms and knows that gold is present in a room if and only if the room has four adjacent rooms each having a landmine.

The agent moves from one room to an adjacent room using breadth-first search to find the shortest path through the previously visited safe rooms. The agent only needs to find the location of the room that contains gold. If the agent is unable to infer the location of gold after visiting all the safe rooms, the output is that Gold could not be detected after visiting all the safe rooms.

The program uses Glucose3 class from the pysat.solvers library to represent positive and negative literals. The code has been thoroughly tested for different minefield world configurations and edge cases. The project provided hands-on experience in implementing a logical agent using propositional logic sentences and SAT solver python-sat to solve real-world problems.
