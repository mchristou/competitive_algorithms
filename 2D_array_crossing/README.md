# 2D array crossing

The code here uses Dijkstra's algorithm of the shortest path to find its way from the starting point to the end point as given by the user.
The dynamic programming features include memoisation with the help of a 2D array to store expensive function calls and recall them when needed,
and breaking the initial problem to smaller ones. The code moves only down and to the right of the current cell,
considers 0s to be obstacles (so it goes around them) and if there is no valid path between the starting point and the ending point,
it will display a corresponding message. Since 0s are obstacles, the end point cannot be a 0. The input includes a 12x20 2D matrix.
