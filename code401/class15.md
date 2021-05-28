# Read : 15

## Trees

- In computer science, a **tree** is a widely used abstract data type that simulates a hierarchical tree structure, with a root value and subtrees of children with a parent node, represented as a set of linked nodes.

- A tree data structure can be defined recursively as a collection of nodes *(starting at a root node)*, where each node is a data structure consisting of a value, together with a list of references to nodes *(the "children")*, with the constraints that no reference is duplicated, and none points to the root. 

- Alternatively, a tree can be defined abstractly as a whole (*globally*) as an ordered tree, with a value assigned to each node.

- Both these perspectives are useful: while a tree can be analyzed mathematically as a whole, when actually represented as a data structure it is usually represented and worked with separately by node *(rather than as a set of nodes and an adjacency list of edges between nodes, as one may represent a digraph, for instance)*.

- For example, looking at a tree as a whole, one can talk about "the parent node" of a given node, but in general, as a data structure, a given node only contains the list of its children but does not contain a reference to its parent *(if any).*

- **Terminology**:
  - **Neighbor**: Parent or child.
  - **Ancestor**: A node reachable by repeated proceeding from child to parent.
  - **Descendant**: A node reachable by repeated proceeding from parent to child. Also known as subchild.
  - **Internal node**: A node with at least one child.
  - **Degree**: For a given node, its number of children. A leaf has necessarily degree zero.
  - **Degree of tree**: The degree of a tree is the maximum degree of a node in the tree.
  - **Distance**: The number of edges along the shortest path between two nodes.
  - **Level**: The level of a node is the number of edges along the unique path between it and the root node.[2]
  - **Width**: The number of nodes in a level.
  - **Breadth**: The number of leaves.
  - **Forest**: A set of n ≥ 0 disjoint trees.
  - **Ordered tree**: A rooted tree in which an ordering is specified for the children of each vertex.
  - **Size of a tree**: Number of nodes in the tree. 


- **Traversal and search methods**:
    - Stepping through the items of a tree, by means of the connections between parents and children, is called *walking the tree*, and the action is a *walk* of the tree.
    - A walk in which each parent node is traversed before its children is called a **pre-order** walk.
    - A walk in which the children are traversed before their respective parents are traversed is called a **post-order** walk.
    - A walk in which a node's left subtree, then the node itself, and finally its right subtree are traversed is called an **in-order** traversal.


##### [Go Back](code_401_reading_notes.md)