# A* Pathfinding Algorithm

My project is an implementation of the A* algorithm in Python, using Pygame.
I have a grid of squares, instead of nodes, which I use as the graph for the A* 
algorithm to run on. To briefly explain the A* algorithm, it works to find the
shortest and fastest path by combining elements of Djikstra's algorithm, which
finds the shortest path, and Greedy Best-First Search to have a general direction
on where to go. It does this using heuristics, which is the function that predicts
the lowest cost it would take to get from the start to the finish.

## Things needed to run the project
Download Pygame


## Files

### UI.py

When I run the project, it uses Pygame to generate the grid.
Then, on the first left-click, it spawns the start. Then the end node, and then
you can draw any boundaries you want. Right-click deletes squares. Pressing the
delete key will randomly generate a maze. Pressing the space bar will prompt
the A* algorithm to find the shortest path in the shortest time possible it can
from the start to end square.

There is a Spot class that defines a lot of things that make visualizing the
A* possible as well as making implementing A* easier, such as the color of the
square indicating its purpose or having methods that turn squares into certain
things like the beginning or end. 

There is also my heuristic function. I 
use diagonal distance, which means my map allows for diagonal movement, and I
use the octile distance, meaning the cost for moving diagonal is sqrt2.

## Sources Used

I used ChatGPT for help writing the algorithm.

https://www.youtube.com/watch?v=JtiK0DOeI4A. This is a Youtube video that I used
to implement the UI aspect, such as the Spot class and the general construction
of the Pygame board.

I also used https://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html
which was the link in the rubric to understand heuristics and A* more. It also
gave me the idea for the tie-breaking.

## What I would do if I had more time

One thing I may do if I had more time is implementing difference costs of
grids. For example, certain open, non-barrier squares could be colored gray 
instead of white to indicate a higher cost of moving through, such as 2 instead
of 1. I would probably have to switch the heuristic and algorithm back to 
Manhattan distance because doing diagonals between those would be weird.

