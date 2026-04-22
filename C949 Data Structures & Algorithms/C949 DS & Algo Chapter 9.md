9.1 Graphs: Introduction
		-[Graph]: data structure for representing connections among items, and consists of vertices connected by edges
				-[vertex]: (or node) represents an item in a graph
				-[edge]: represents a connection between two vertices in a graph
	Adjacency and Paths
		-In a graph:
			-two vertices are adjacent if connected by an edge
			-a path is a sequence of edges leading from a source (starting) vertex to a destination (ending) vertex. Path length is the number of edges in the path
			-the distance between two vertices is the number of edges on the shortest path between those vertices
	Connected vs. Disconnected
		-[Connected graph]: contains a path between every pair of vertices
		-[Disconnected graph]: does not contain a path between every pair of vertices
9.2 Applications of Graphs
	Geographic Maps and Navigation
		-graphs often used to represent a geographic map that contains information about places and travel routes
		-each edge in such a graph has an associated numerical value called a weight that represents the length of a travel route, either in total distance or expected time needed to traverse the route
	Product Recommendations
		-graph can be used to represent relationships between products
		-vertices in the graph corresponding to a customer's purchased products have adjacent vertices representing products that can be recommended to the customer
	Social and Professional Networks
		-graph may use a vertex to represent a person
		-edge could be used to represent relationship between two people, friendships, or business conducted between two people
9.3 Graph Representations: Adjacency Lists
	Adjacency Lists
		-each vertex has a list of adjacent vertices, each list item representing an edge
	Advantages of Adjacency Lists
		- key advantage is size of O (V+E)
		- sparse graph has far fewer edges than the maximum possible
9.4 Graph Representations: Adjacency Matrices
	Adjacency Matrices
		-each vertex is assigned to a matrix row and column, and a matrix element is 1 if the corresponding two vertices have an edge or is 0 otherwise
9.5 Graphs: Breadth-first Search
	Graph Traversal and Breadth-First Search
		-algorithm commonly must visit every vertex in a graph in some order, known as [graph traversal]
		-to [visit] a vertex during a graph traversal means to perform an action of interest with that vertex, like printing the vertex's label or adding the vertex to an output list
		-[Breadth-First Search]: traversal that visits a starting vertex, then all vertices of distance 1 form that vertex, then of distance 2, and so on, without revisiting a vertex
	Vertex Visitor
		-BFS visits all vertices in a graph
		-a list of vertices can be returned from a BFS method, if desired
		-greater flexibility achieved by using a [vertex visitor method]: method that is called each time a vertex during traversal
	Breath-First Search Algorithm
		-an algorithm for breadth-first search enqueques the starting vertex in a queue
		-while the queue is not empty, the algorithm dequeques a vertex from the queue, visits the dequeue vertex, enqueues that vertex's adjacent vertices and repeats
		-when the BFS algorithm first encounters a vertex tath vertex is aid to have been [discovered]
		-the vertices in the queue are called the [frontier] being vertices thus far discovered but not yet visited
		-already discovered vertex is not enqueued again
9.6 Graphs: Depth-First Search
	Graph Traversal and Depth-First Search
		-[Depth-First Search (DFS)]: traversal that visits a starting vertex, then visits every vertex along each path starting from that vertex to the path's end before backtracking 
	DFS Algorithm
		-pushes the starting vertex onto a stack
		-while stack is not empty, algorithm pops the vertex from the stack's top
		-if vertex has not already been visited, algorithm visits the vertex and pushes the adjacent vertices to the stack
9.7 Directed Graphs (Digraph)
		-consists of vertices connected by directed edges
		-[directed edge]: connection between a starting vertex and a terminating vertex
		-in directed graph, a vertex Y is adjacent to a vertex X if an edge exists from X to Y
		-many graphs are directed, like those representing links between web pages, maps for navigation, or college course prerequisites
	Paths and Cycles
		-in a directed graph: 
			-[path]: is a sequence of directed edges leading form a source (starting) vertex to a destination (ending) vertex
			-[cycle]: is a path that starts and ends at the same vertex. 
		-directed graph is [cyclic] if the graph contains a cycle, and [acyclic] if the graph does not contain a cycle
	Incoming and Outgoing Edges
		-[Outgoing Edge]: an edge that has V as the starting vertex 
		-[Incoming Edge]: an edge that has V as the terminating vertex 
		-vertex's [degree]: is the number of edges containing the vertex
		-in a directed graph, vertex's degree is the sum of the number of incoming and outgoing edges
9.8 Weighted Graphs 
		-associates a weight with each edge
		-graph edge's [weight] or [cost], represents some numerical value between vertex items, such as flight cost between airports, connection speed between computers, or travel time between cities
		-weighted graph may be directed or undirected
	Path Length In Weighted Graphs
		-[Path Length]: is the sum of the edge weights in the path
	Negative Edge Weight Cycle
		-[Cycle Length]: is the sum of the edge weights in a cycle
		-[Negative edge weight cycle]: has a cycle length less than 0
		-shortest path does not exist in a graph with a negative edge weight cycle, because each loop around the negative edge weight cycle further decreases the cycle length, so no minimum exists
9.10 Algorithm: Dijkstra's Shortest Path
		-finding the shortest path between vertices in a graph has many applications
		-Dijkstra's shortest path algorithm determines the shortest path form a start vertex to each vertex in a graph
		-for each vertex, Dijkstra's algorithm determines the vertex's distance and predecessor 
		-vertex's [distance] is the shortest path distance from the start vertex
		-vertex's [predecessor] references the previous vertex along the shortest path form the start vertex
		-Dijkstra's algorithm initializes all vertices distances to infinity, initializes all vertices predecessors to None, and enqueques all vertices into a queue of unvisited vertices
		-algorithm the assigns the start vertex's distance with 0. While queue is not empty, the algorithm dequeques the vertex with the shortest distance
		-for each adjacent vertex, algorithm computes the distance of the path from the start vertex to the current vertex and continuing on to the adjacent vertex
		-if the path's distance is shorter than the adjacent vertex's current distance, a shorter path has been found
		-the adjacent vertex's current distance is updated to the distance of hte newly found shorter path's distance, and the vertex's predecessor is assigned with the current vertex
9.11 Algorithm: Bellman-Ford's Shortest Path 
		-determines the shortest path from a start vertex to each vertex in a graph
		-for each vertex, Bellman-Ford algorithm determines the vertex's distance and predecessor
		-does not require a specific order for visiting vertices during each main iteration
		-after each iteration, a vertex's current distance and predecessor may not be the shortest path from the start vertex
		-shortest path may propagate to only one vertex each iteration, requiring V-1 iterations to propagate from the start vertex to all other vertices
	Checking For Negative Edge Weight Cycles
		-Bellman-Ford algorithm supports graphs with negative edge weights
		-if a negative edge weight cycle exists, a shortest path does not exist
9.12 Topological Sort
		-topological sort of a directed, cyclic graph produces a list of the graph's vertices such that for every edge from a vertex X to a vertex Y, X comes before Y in the list
	Topological Sort Algorithm
		-associates an integer count with each vertex
		-each vertex's count is initialized to the number of edges incoming to the vertex
		-each vertex with an initial count of O is added to a vertex collection
		-after initialization, the algorithm's main loop does the following until the collection is empty:
				1. Remove any vertex from the vertex collection
				2. Append the removed vertex to the result ordering
				3. For each of the removed vertex's outgoing edges:
						1. Decrement the count for the edge's to-vertex
						2. If decremented count is 0, add the edge's to-vertex to the vertex collection
9.13 Minimum Spanning Tree
		-a subset of the graph's edge that connect all vertices in the graph together with the minimum sum of edge weights
		-graph must be weighted and connected
		-connected graph contains a path between every pair of vertices
	Kruskal's Minimum Spanning Tree Algorithm
		-determines the subset of a graph's edges that connect all the graph's vertices with the minimum possible sum of edge weights. uses 3 collections:
			1.[edge_queue]: a priority queue of edges, initially containing all graph edges. edge weights are priorities
			2.[result]: a list of edges comprising the minimum spanning tree, initially empty
			3.[vertex_sets]: a collection of vertex sets. each set represents vertices connected by edges in result. initially, vertex_sets contains one set for each vertex
9.14 All Pairs Shortest Path
		-all pairs shortest path algorithm determines the shortest path between all possible pairs of vertices in a graph

		