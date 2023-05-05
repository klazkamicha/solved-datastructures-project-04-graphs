Download Link: https://assignmentchef.com/product/solved-datastructures-project-04-graphs
<br>
You are required to implement two solutions for problems that are embedded in a graph data structure: Prim’s algorithm in a undirected weighted graph, Dijkstra’s algorithm in a directed weighted graph; you can only use adjacency lists to represent your graphs. You are also required to create UML diagrams for each of the classes that you implement. Finally, you have to provide the means to test your system by developing a menu program that allows the user to manipulate your structures.

You may use the queue, stack, and list algorithms defined in the C++ standard library (STL). You must use your own implementation for the hash table. Also, any array must be dynamically allocated.

Underflow exceptions might be generated in some of the functions you implement. Make sure exceptions are thrown and caught where appropriate.

<h1>Deliverables</h1>

<ul>

 <li>A 1 page report that explains the design of your solutions. Please include what each teammate did and approximate hours spent on the project.</li>

 <li>An implementation of Prim’s algorithm.</li>

 <li>An implementation of Dijkstra’s algorithm.</li>

 <li>A menu program to test the implemented data structures.</li>

</ul>

<h1>1           Prim’s algorithm</h1>

In this part of the project, you need to implement three classes, a <em>Graph Class</em>, a <em>Vertex Class</em>, and an <em>Edge Class</em>; create their respective UML diagrams. Calculate the running time of your functions and include them in your report.

<em>1.1      Description</em>

<h2>1.1         Description</h2>

A spanning tree of graph G=(V, E) is another graph T = (V, F) with the same vertices as G, and |<em>V </em>| − 1 edges of E that form a tree.

A minimum spanning tree (MST) T of G is a spanning tree whose total weight (summed over all edges of T) is minimal.

For this part of the project you will <strong>implement Prim’s algorithm to find an MST in a undirected weighted graph; an adjacency list has to be used to represent the graph</strong>. Vertices are represented by their names in the graph. To ease the execution of some of your operations, your graph has to have a hash table to store all the vertices, where the key is the name of the vertex and the value is the vertex object. In the event you need information (data, edges, etc) about a particular vertex, you will have to hash the vertex’s name and find the vertex object in the table (you may use linear probing).

<strong>1.2      Data Members</strong>

Specify all the data members your implementation needs.

<strong>1.3      Member Functions Constructors</strong>

Defines constructor. Maximum graph size is 20 vertices.

<h2>Destructor</h2>

Defines destructor. Clean up any allocated memory.

<strong>Accessors bool empty() </strong>Returns true if the graph is empty, false otherwise.

<strong>int degree(string v) </strong>Returns the degree of the vertex v. Throw an illegal argument exception if the argument does not correspond to an existing vertex.

<strong>int edgeCount()          </strong>Returns the number of edges in the graph <strong>bool isConnected()          </strong>Determines if the graph is connected.

<strong>double adjacent( string u, string v ) </strong>Returns the weight of the edge connecting vertices u and v. If the vertices are the same, return 0. If the vertices are not adjacent, return -1 (our representation of infinity). Throw an illegal argument exception if the arguments do not correspond to existing vertices.

<em>1.3      Member Functions</em>

<strong>DFS(string v) </strong>Performs DFS traversal starting on vertex v. Reset vertices after the traversal. Prints the order of vertices visited.

<strong>BFS(string v) </strong>Performs BFS traversal starting on vertex v. Reset vertices after the traversal. Prints the order of vertices visited.

<strong>MST( string v ) </strong>Returns the minimum spanning tree using Prim’s algorithm of those vertices which are connected to vertex v. Throw an illegal argument exception if the argument does not correspond to an existing vertex.

<h2>Mutators</h2>

<strong>void buildGraph()              </strong>Reads structure from a text file and builds a undi-

rected weighted graph.

<strong>clear() </strong>Removes all the elements in the undirected weighted graph <strong>reset() </strong>Iterates over all vertices in the graph and marks them as unvisited.

<strong>insert(string u, string v, double w) </strong>If the weight w <em>&lt; </em>0 or w = ∞, throw an illegal argument exception. If the weight w is 0, remove any edge between u and v (if any). Otherwise, add an edge between vertices u and v with weight w. If an edge already exists, replace the weight of the edge with the new weight. If the vertices do not exist or are equal, throw an illegal argument exception.

<strong>Friends</strong>

Defines friends for this class.

<h1>2           Dijkstra’s algorithm</h1>

In this part of the project, you need to implement three classes, a <em>DirGraph Class</em>, a <em>Vertex Class</em>, and an <em>Edge Class</em>; create their respective UML diagrams. Calculate the running time of your functions and include them in your report.

<h2>2.1         Description</h2>

Dijkstra’s algorithm is an algorithm to find the shortest path among vertices in a graph.

For this part of the project you will <strong>implement Dijkstra’s algorithm to find the shortest path between a source vertex and the rest of the vertices in a directed weighted graph; an adjacency list has to be used to represent the graph</strong>. Vertices are represented by their names in the graph. To ease the execution of some of your operations, your graph has to have a hash table to store all the vertices, where the key is the name of the vertex and the value is the vertex object. In the event you need information (data, edges, etc) about a particular vertex, you will have to hash the vertex’s name and find the vertex object in the table.

<strong>2.2      Data Members</strong>

Specify all the data members your implementation needs.

<strong>2.3      Member Functions Constructors</strong>

Defines constructor. Maximum graph size is 20 vertices.

<h2>Destructor</h2>

Defines destructor. Clean up any allocated memory.

<strong>Accessors bool empty() </strong>Returns true if the graph is empty, false otherwise.

<strong>int inDegree(string v) </strong>Returns the indegree of the vertex v. Throw an illegal argument exception if the argument does not correspond to an existing vertex.

<strong>int outDegree(string v) </strong>Returns the outdegree of the vertex v. Throw an illegal argument exception if the argument does not correspond to an existing vertex.

<em>2.3      Member Functions</em>

<strong>int edgeCount()        </strong>Returns the number of edges in the graph

<strong>double adjacent( string u, string v ) </strong>Returns the weight of the edge connecting vertices u and v. If the vertices are the same, return 0. If the vertices are not adjacent, return -1 (our representation of infinity). Throw an illegal argument exception if the arguments do not correspond to existing vertices.

<strong>DFS(string v) </strong>Performs DFS traversal starting on vertex v. Reset vertices after the traversal. Prints the order of vertices visited.

<strong>BFS(string v) </strong>Performs BFS traversal starting on vertex v. Reset vertices after the traversal. Prints the order of vertices visited.

<strong>shortPath( string u, string v ) </strong>Returns the shortest path using Dijkstra’s between vertices u and v. Throw an illegal argument exception if the arguments do not correspond to existing vertices.

<strong>double distance( string u, string v ) </strong>Returns the shortest distance between vertices u and v. Throw an illegal argument exception if the arguments do not correspond to existing vertices. The distance between a vertex and itself is 0.0. The distance between vertices that are not connected is -1 (our representation of infinity).

<h2>Mutators</h2>

<strong>void buildGraph()         </strong>Reads structure from a text file and builds a directed

weighted graph.

<strong>clear()            </strong>Removes all the elements in the undirected weighted graph <strong>reset() </strong>Iterates over all vertices and marks them as unvisited.

<strong>insert(string u, string v, double w) </strong>If the weight w ≤ 0, throw an illegal argument exception. If the weight is w <em>&gt; </em>0, add an edge between vertices u and v. If an edge already exists, replace the weight of the edge with the new weight. If the vertices do not exist or are equal, throw an illegal argument exception.

<strong>Friends</strong>

Defines friends for this class.

<h1>3           Graph Representation</h1>

<h2>Format for the text file</h2>

The example text file for the buildGraph() method is uploaded to Canvas. Up to twenty vertices (string) will be listed with white spaces between, followed by a new line. Next, each edge will be listed: u (string), space, v (string), space, weight (double), new line. The same format is used for directed and undirected graphs.

<h2>Format for printing Prim’s MST (edges and total weight)</h2>

A B 4

A C 6.4

C F 3

A D 9

Distance: 22.4

<h2>Format for printing Dijkstra’s shortest path (distance to each node from A)</h2>

<ul>

 <li>0</li>

 <li>4</li>

 <li>1</li>

 <li>6</li>

</ul>

F 7

<h1>4           The Menu Program</h1>

In order to test your program, you are required to implement a menu program that provides the means to run each of the functions in your classes (name your executable proj4). The TA will choose one group to demo the project.

<h2>Format for the Menu Program</h2>

First, prompt the user for the type of graph (char ’d’ for directed or char ’u’ for undirected). Next, prompt for a file name (using path provided) for the .txt file to load the graph. The format of an example .txt file is provided on Canvas for you to be able to test your work. Next, give the following options for the specific graph (please have them in this <strong>EXACT </strong>order for grading purposes):

<h2>Undirected Graph (Prim’s)</h2>

<ol>

 <li>Empty?</li>

 <li>Degree (v)</li>

 <li>Edge count</li>

 <li>Connected?</li>

 <li>Adjacent (u, v)?</li>

 <li>DFS (v)</li>

 <li>BFS (v)</li>

 <li>Print MST (v)</li>

 <li>Clear</li>

 <li>Insert (u, v, w)</li>

 <li>Exit</li>

</ol>

<h2>Directed Graph (Dijkstra’s)</h2>

<ol>

 <li>Empty?</li>

 <li>InDegree (v)</li>

 <li>OutDegree (v)</li>

 <li>Edge count5. Adjacent (u, v)?</li>

 <li>DFS (v)</li>

 <li>BFS (v)</li>

 <li>Print Short path (v)</li>

 <li>Clear</li>

 <li>Insert (u, v, w)</li>

 <li>Exit</li>

</ol>