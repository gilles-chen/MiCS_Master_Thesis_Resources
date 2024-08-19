## 1. Basic Concepts

### Definition

A **data structure** is a particular way of organizing and storing data in a computer so that it can be accessed and modified efficiently.

### Importance

- **Efficiency**: Improves algorithm efficiency by providing methods to store and access data quickly.
- **Reusability**: Common data structures provide reusable implementations.
- **Abstraction**: Offers a way to handle data at a higher level of abstraction.

### Categories

Data structures can be broadly classified into two categories:

- **Linear Data Structures**
- **Non-Linear Data Structures**

---

## 2. Linear Data Structures

Linear data structures store data in a sequential manner. Each element is connected to its previous and next element, making data traversing linear.

### 2.1 Arrays

- **Description**: A collection of items stored at contiguous memory locations.
- **Characteristics**: Fixed size, homogeneous data elements.
- **Operations**:
  - **Access**: `O(1)` time complexity for accessing elements by index.
  - **Search**: `O(n)` in the worst case for unsorted arrays.
  - **Insertion/Deletion**: `O(n)` since elements may need shifting.
- **Applications**: Used in dynamic programming, where data is stored in a tabular format.

### 2.2 Linked Lists

- **Description**: A linear collection of data elements, called nodes, where each node points to the next.
- **Characteristics**: Dynamic size, efficient insertions/deletions.
- **Types**:
  - **Singly Linked List**: Each node points to the next node.
  - **Doubly Linked List**: Nodes have pointers to both next and previous nodes.
  - **Circular Linked List**: Last node points to the first node.
- **Operations**:
  - **Insertion/Deletion**: `O(1)` at the beginning, `O(n)` at arbitrary positions.
  - **Search**: `O(n)` time complexity.
- **Applications**: Implementation of queues and stacks, useful in scenarios with frequent insertions and deletions.

### 2.3 Stacks

- **Description**: A collection of elements with Last In, First Out (LIFO) access pattern.
- **Operations**:
  - **Push**: Add an element to the top.
  - **Pop**: Remove an element from the top.
  - **Peek/Top**: View the top element without removing it.
- **Time Complexity**: `O(1)` for push and pop operations.
- **Applications**: Function call management, syntax parsing, backtracking algorithms.

### 2.4 Queues

- **Description**: A collection of elements with First In, First Out (FIFO) access pattern.
- **Types**:
  - **Simple Queue**: Basic FIFO structure.
  - **Circular Queue**: Connects the end of the queue back to the front.
  - **Priority Queue**: Elements are processed based on priority.
- **Operations**:
  - **Enqueue**: Add an element to the end.
  - **Dequeue**: Remove an element from the front.
- **Time Complexity**: `O(1)` for enqueue and dequeue operations.
- **Applications**: Order processing, task scheduling, breadth-first search algorithms.

---

## 3. Non-Linear Data Structures

Non-linear data structures store data in a hierarchical manner and are more complex than linear structures.

### 3.1 Trees

- **Description**: A hierarchical data structure with a root node and child nodes forming a parent-child relationship.
- **Characteristics**:
  - **Root**: The topmost node.
  - **Leaf**: Nodes with no children.
  - **Height**: Longest path from the root to a leaf.
- **Types**:
  - **Binary Tree**: Each node has at most two children.
  - **Binary Search Tree (BST)**: Left child has a smaller value, right child has a greater value.
  - **AVL Tree**: Self-balancing BST.
  - **B-trees**: Used to efficiently store and manage databases and file systems.
- **Operations**:
  - **Insertion/Deletion/Search**: `O(log n)` in balanced trees.
  - **Traversal**: In-order, pre-order, post-order.
- **Applications**: Hierarchical data representation, databases, syntax trees in compilers.

### 3.2 Graphs

- **Description**: A collection of nodes, called vertices, and edges connecting pairs of vertices.
- **Characteristics**:
  - **Directed vs Undirected**: Edges have a direction or not.
  - **Weighted vs Unweighted**: Edges have weights or not.
- **Representation**:
  - **Adjacency Matrix**: 2D array representation.
  - **Adjacency List**: Array of lists.
- **Operations**:
  - **Traversal**: Depth-First Search (DFS), Breadth-First Search (BFS).
  - **Shortest Path**: Dijkstra’s, Bellman-Ford algorithms.
- **Applications**: Social networks, networking, pathfinding algorithms.

---

## 4. Advanced Data Structures

These structures offer more efficient data handling for specific applications.

### 4.1 Hash Tables

- **Description**: A data structure that maps keys to values using a hash function.
- **Characteristics**: Provides average `O(1)` time complexity for search, insert, and delete operations.
- **Operations**:
  - **Insert/Search/Delete**: `O(1)` on average, `O(n)` in the worst case.
  - **Handling Collisions**: Chaining, open addressing.
- **Applications**: Implementing associative arrays, caching, sets.

### 4.2 Heaps

- **Description**: A special tree-based data structure that satisfies the heap property.
- **Types**:
  - **Min-Heap**: Parent node has a value less than or equal to its children.
  - **Max-Heap**: Parent node has a value greater than or equal to its children.
- **Operations**:
  - **Insert/Delete**: `O(log n)`.
  - **Peek**: `O(1)` to get the minimum or maximum element.
- **Applications**: Priority queues, heap sort, scheduling algorithms.

### 4.3 Trie

- **Description**: A tree-like data structure used to store associative data structures.
- **Characteristics**: Used for dynamic sets of strings.
- **Operations**:
  - **Insert/Search**: `O(m)` where `m` is the length of the key.
  - **Prefix Searching**: Efficient prefix-based searches.
- **Applications**: Autocomplete systems, spell checkers.

### 4.4 Segment Trees and Fenwick Trees

- **Description**: Trees used for storing information about intervals or segments.
- **Segment Trees**: Allow querying of sums, minimums, and other range queries in `O(log n)` time.
- **Fenwick Trees (Binary Indexed Trees)**: Used for cumulative frequency tables.
- **Operations**:
  - **Update/Query**: `O(log n)`.
- **Applications**: Efficient range query solutions.

---

## 5. Complexity Analysis

Understanding the complexity of data structure operations is crucial for choosing the appropriate data structure.

- **Time Complexity**: Measures the time an algorithm takes relative to the input size.
- **Space Complexity**: Measures the amount of memory an algorithm uses relative to the input size.

| Data Structure                  | Access | Search | Insertion | Deletion |
|---------------------------------|--------|--------|-----------|----------|
| Array                           | O(1)   | O(n)   | O(n)      | O(n)     |
| Linked List                     | O(n)   | O(n)   | O(1)      | O(1)     |
| Stack                           | O(n)   | O(n)   | O(1)      | O(1)     |
| Queue                           | O(n)   | O(n)   | O(1)      | O(1)     |
| Binary Search Tree (BST)        | O(log n) | O(log n) | O(log n) | O(log n) |
| Hash Table                      | N/A    | O(1)   | O(1)      | O(1)     |

## 6. Choosing the Right Data Structure

Choosing the right data structure depends on the requirements of the application:

- **For Fast Lookups**: Hash tables.
- **For Ordered Data**: Trees (BST, AVL).
- **For Sequential Access**: Arrays or linked lists.
- **For Frequent Insertions/Deletions**: Linked lists, stacks, queues.