- - - - - - - - -
Objective
- - - - - - - - - 
Program to implement a communication network using graph and Dijkistra's algorithm using minheap data structure. 
(file name: Graph.java)
- - - - - - - - - - - - - - - - - - - - - -
Command Line Arguments
- - - - - - - - - - - - - - - - - - - - - -
javac Graph.java
java Graph <input filename>
The command line will prompt for the input file name.
Print-To print the graph
path <tailvertex> <headvertex> -To print the path
addedge <tailvertex> <headvertex> <transmit time> -To add an edge
deleteedge <tailvertex> <headvertex>  -To delete an edge
edgedown <tailvertex> <headvertex>  -To make an edge as Down
edgeup <tailvertex> <headvertex>  -To make an edge up
vertexdown <vertex>  -To make a vertex down
vertexup <vertex>  -To make a verted up
path <from_vertex> <to_vertex>  -To find the shortest path from the two vertices
reachable-To print the reachable vertex of the graph.
Quit-To quit the Java program
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
Brief Description of the program design:
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
Classes are used to represent each vertex and edge of the graph .
The program initially reads the input file and creates a graph using the minheap data structure.
Using the minheap data structure the program finds the shortest path for every node using the Dijkstra's algorithm.
Command line arguments are used to add vertex/edges, delete vertex/edges and to print the graph.
- - - - - - - - - - - - - - - - - - - 
Breakdown of the files:
- - - - - - - - - - - - - - - - - - -
The files containing the data are read from the command prompt.
The command prompt goes into an infinite loop and waits for the command from the user.
Depending on the command from the user the main routine calls the corresponding functions in the same file.
Print-calls the printgraph() function to print the graph.
Quit-calls the System.exit(0) function to exit the program.
Recheable-calls the reacheable() function to find and print the reacheable vertices.
Vertexdown-calls the downvertex() function to make a vertex invalid.
Vertexup-calls the upvertex() function to make a vertex valid.
Path-calls the weighted() function to find the minumum path and printpath() function to print the path.
Edgedown-calls the downedge() function to make an edge as invalid.
Edgeup-calls the upedge() function to make an edge valid.
Deleteedge-calls the deleteedge() function to delete an edge.
Addedge-calls the add1Edge() function to add an edge as a directed edge to the graph.

- - - - - - - - - - - -
Compiler used:
- - - - - - - - - - - -
java version "1.7.0_79"

- - - - - - - - -
Summary:
- - - - - - - - -
This files reads any file and forms a graph from it.
The program prints the output in alphabetical order.
The code does not differentiate between capital and small characters.
Double type numbers are not rounded.
	
- - - - - - - - - - - - - - - - -
Data Structure Design:
- - - - - - - - - - - - - - - - -
Classes are used to represent every vertex and edge in the graph. 
A minheap is used to store the vertex and they are sorted based on their weight. 
Sorting a minheap happens in O(n) runing time. 
Inserting a vertex takes O(logn) running time.
The Dijkstra's algorithm is implemented to find the shortest path using binary heap as the data structure.
The running time of Dijkstra's algorithm is O(|V|+|E|)*lg|V|
The reachable program is used to find the vertex that are reachable from a source vertex.
The running time of reachable funtion is O(|V|^2+(|V|*|E|))
