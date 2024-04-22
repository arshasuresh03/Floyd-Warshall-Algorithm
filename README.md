# Floyd-Warshall-Algorithm
It is used to find the shortest paths between all pairs of nodes in a weighted graph. This algorithm is highly efficient and can handle graphs with both positive and negative edge weights

Here's a detailed description of the Floyd-Warshall algorithm:

Initialization:
Initialize a 2D array dist[][] of size (V x V) where V is the number of vertices in the graph.
Set dist[i][j] to the weight of the edge from vertex i to vertex j if there is an edge between them, otherwise set it to infinity.
Set dist[i][i] to 0 for all i, representing the distance from a vertex to itself.

Main Loop:
The algorithm iterates over all vertices k from 1 to V.
For each pair of vertices (i, j), it checks if the shortest path from i to j passing through k is shorter than the current shortest path from i to j.
If it is, update dist[i][j] with the new shortest path distance.

Relaxation:
For each vertex pair (i, j), consider the intermediate vertex k.
If the path from i to k and then from k to j is shorter than the current shortest path from i to j, update dist[i][j] with the new shorter distance.

Termination:
Repeat the main loop for all vertices k.
After V iterations, the dist[][] array contains the shortest distances between all pairs of vertices.

Negative Cycle Detection:
After the main loop, check for negative cycles by examining the diagonal elements of the dist[][] array.
If any diagonal element dist[i][i] is negative, it indicates the presence of a negative cycle reachable from vertex i.

Output:
The dist[][] array now holds the shortest distances between all pairs of vertices.
It represents the shortest path distances from each vertex to all other vertices in the graph.

DEMO:

![image](https://github.com/arshasuresh03/Floyd-Warshall-Algorithm/assets/160167081/674d9842-bdfc-4ff9-bb42-99ffb1df0576)
