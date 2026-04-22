==Connecting Everything With Graphs==
==Graphs==
>Data structure that specializes in relationships, as it easily conveys how data is connected

Each node is a [vertex] and each line is an [edge]
Vertices that are connected by and edge are said to be [adjacent] to each other

==Breadth-First Search==
> algorithm was a queue, which keeps track of which vertices to process next

==Graph Databases==
>Databases that store data in the form of a graph

==Weighted Graphs==
>Regular graph but contains additional information about the edges in the graph

==Dijkstra's Algorithm== 
Rules:
1. Make starting vertex out current vertex
2. Check all the vertices adjacent to the current vertex and calculate and record the weights from the starting vertex to all known locations
3. To determine next current vertex, find cheapest unvisited known vertex that can be reached from starting vertex
4. Repeat the first three steps until visited every vertex in the graph