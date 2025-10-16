# Sem 2 Breakdown Alg&C
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  01-02-2025
> > *Module :* [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Algorithms and Complexity]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#]]
> [[#]]
> [[#]]
> [[#]]

---
## Semester 2 x breakdown 

> [!leaf]+ Sem 2 Topic Branches
> This part of the course is NOT about automota & FSM but DESIGN of algorithms and especially the analysis of algorithms
> Below is the list of topics contained within [[Yr2 Notes📘/Semester 1 & 2/Algo & Complexity/Algorithms and Complexity]] for Semester 2 topics
> - determine complexity of variety of algorithms
> - describe variety of data structures
> - demonstrate correctness of algorithm choice
> - $big$ $Ο$, $big$ $\Theta$ and $big$ $Ω$ notation
> - Ackermann function
> - Graphs and trees 
> -  shortest path / divide and conquer etc
> - loop invariants
> - the Master Theorem
> - Formal Analysis of algorithms

----
## Courseworks & exams for the module

## EXAM

70% of 10 cred module. its fat. end of it. study bish
Topics cover semester 1 and semester 2
format of exam not decided yet but they will make clear
Tutorials and work will be given every week


▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.15: Shortest Paths 1 -- Dijkstra's Algorithm](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=3b2bb1eb-ee24-42a6-98e9-b2b200676e2a) 10:15, Tue, 1 Apr 2025

1. Introduction to general graphs and shortest pathfinding algorithms
2. Representation of graphs in computer systems
3. Adjacency list representation
4. Global adjacency matrix representation
5. Path counting using matrix multiplication
6. Introduction to weighted graphs
7. Dijkstra's algorithm overview
8. Single source shortest path problem
9. Initialization of Dijkstra's algorithm (source node and estimates)
10. Settled vertices and priority queue
11. Relaxation of edges in Dijkstra's algorithm
12. Maintaining estimates during the algorithm's execution
13. Proof of correctness for Dijkstra's algorithm
14. Invariants in Dijkstra's algorithm
15. Running example of Dijkstra's algorithm
16. Complexity analysis of Dijkstra's algorithm
17. Priority queue operations and data structure considerations
18. Alternative implementations for dense graphs
19. Bucket queue optimization for integer weights
20. Storing paths for retrieval in Dijkstra's algorithm

Thursday 27 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.14: Heaps and heapsort](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=73faa80a-7b80-4071-b60e-b2ad00fbbce1) 17:15, Thu, 27 Mar 2025

1. Overview of Heaps and Heap Sort
2. Definition and properties of a heap
3. Concept of max heap and min heap
4. Complete binary tree structure
5. Priority queues and their operations
6. Comparisons between binary search trees and heaps
7. Insertion operation in a heap
8. Deletion of maximum element from a heap
9. Sift down operation in a heap
10. Sift up operation in a heap
11. Time complexity of heap operations: O(log n)
12. Implementation of heaps using arrays
13. Representing a heap using array indices
14. Building a heap from an unordered array in linear time
15. Heap sort algorithm and its steps
16. Correctness argument for heap sort
17. Comparison with selection sort
18. Increasing key operation and challenges of finding elements
19. Use of a map for locating keys in the heap
20. Overview of advanced trees: AVL trees, A23 trees, Red-Black trees
21. Introduction to graph theory and pathfinding algorithms (upcoming topics)

Tuesday 25 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.13 Treesort, Quicksort](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5f8aa717-6b56-420d-86e8-b2ab0077fc1d) 09:15, Tue, 25 Mar 2025

1. Importance of daylight and time changes.
2. Introduction to sorting algorithms.
3. Binary search trees (BST) and their properties.
4. In-order traversal of BST results in sorted order.
5. Tree sort algorithm using binary search trees.
6. Duplicate keys in BST and stable sorting.
7. Loop invariant concept and its application to tree sort.
8. Correctness argument for the tree sort algorithm.
9. Complexity analysis of tree sort:
    - Worst-case time complexity: O(n²)
    - Average-case time complexity: O(n log n)
10. Self-balancing trees and their effect on sorting.
11. Introduction to quicksort algorithm.
12. Partitioning strategy in quicksort:
    - Picking a pivot.
    - Rearranging elements around the pivot.
13. Pointers in the quicksort algorithm:
    - Left and right pointers.
    - Scanning for elements to swap.
14. Recursion in quicksort on sub-arrays.
15. Code implementation of the quicksort algorithm.
16. Complexity analysis of quicksort:
    - Worst-case time complexity: O(n²)
    - Average-case time complexity: O(n log n)
    - Discussion of balanced vs. unbalanced partitioning.
17. Practical considerations and optimizations for quicksort.
18. Poly-algorithms: combining sorting methods (quicksort with insertion sort).
19. Additional considerations: cache efficiency in sorting algorithms.

Thursday 20 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.12: Binary Search Trees; AVL trees](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=a3d1e2b1-9dff-4d95-aac5-b2a600fbc43d) 17:15, Thu, 20 Mar 2025

1. Importance of efficient data storage and retrieval
2. Comparison of data structures: linked lists, sorted arrays, hash tables
3. Limitations of hash tables for partial key searches
4. Introduction to binary search trees (BST)
5. Structure and properties of binary search trees
6. In-order traversal of binary search trees
7. Complexity analysis of searching, inserting, and deleting in binary search trees
8. Worst-case scenarios leading to unbalanced trees
9. Introduction to AVL trees as self-balancing binary search trees
10. Definition of balance factor in AVL trees
11. Maintaining balance factors (0, 1, -1) in AVL trees
12. Rebalancing operations: single rotations (left/right)
13. Cases of imbalance: right-right and left-left situations
14. Left rotation example in AVL trees
15. Right rotation example in AVL trees
16. Double rotations: right-left and left-right situations
17. Implementation details for AVL trees (height and balance factor storage)
18. Average-case performance of random binary search trees
19. Importance of maintaining logarithmic height in AVL trees
20. Comparison of AVL trees and other self-balancing trees (e.g., red-black trees)
21. Introduction to Fibonacci numbers related to AVL tree structure
22. Future topic: graph algorithms

Tuesday 18 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.11: Introduction to Graphs and Trees](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5b0fc03d-9db9-4e8f-86fc-b2a40077f9a5) 09:15, Tue, 18 Mar 2025

1. Definition of graphs (vertices and edges)
2. Types of graphs: directed vs. undirected
3. Graph representations (functions for edges, weights)
4. Paths and cycles in graphs
5. Connected and disconnected graphs
6. Definition of trees as special types of graphs
7. Properties of trees (connected and acyclic)
8. Root node and hierarchy in trees
9. Graph exploration algorithms
10. Depth-first search (DFS) using stack
11. Breadth-first search (BFS) using queue
12. Traversals of trees: pre-order, in-order, and post-order
13. Implementation of tree traversals in code
14. Level-order traversal of trees
15. Distinctions between the use of stacks and queues in traversals
16. Importance of exploring graphs for data retrieval and manipulation
17. Applications of graph traversal in memory management (garbage collection)

Thursday 6 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.10: Hash Tables 2 -- open addressing](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=c7b4515c-b0bd-4fd7-b406-b29800fbca18) 17:15, Thu, 6 Mar 2025

1. Introduction to hash tables.
2. Collision resolution strategies overview.
3. Chaining in hash tables.
4. Hash function example and its poor distribution.
5. Structure of a hash table with chaining.
6. Average-case retrieval and insertion time complexity in chaining.
7. Open addressing as an alternative to chaining.
8. Probing in open addressing.
9. Linear probing explained.
10. Load factor in open addressing.
11. Insertion operation in open addressing.
12. Search operation in open addressing, including handling absent items.
13. Deletion operation challenges in open addressing.
14. Tombstone method for deletion.
15. Rehashing for cluster management after deletion.
16. Average-case time complexity analysis of hash table operations.
17. Quadratic probing and its advantages.
18. Double hashing technique.
19. Importance of a good hash function.
20. Hash function considerations (e.g., uniformity and information retention).
21. Hashing by division method and issues with table size.
22. Importance of table size selection (e.g., prime numbers vs. powers of two).
23. Risks associated with poor hash function design.
24. Worst-case performance concerns in hash tables.
25. Denial of Service attacks via hash flooding.
26. Conclusion on average performance and risks of hash tables.
27. Focus week announcement and reason for no lecture next week.
28. Problem classes related to hash tables.

Tuesday 4 Mar 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.9: Hash Tables 1 -- chaining](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e53e512a-4867-4da2-82ad-b296007818de) 09:15, Tue, 4 Mar 2025

1. Introduction to hash tables
2. Key-value stores and their applications
3. Comparison with linear data structures (linked lists, arrays)
4. Constant time complexity for storing and searching
5. Worst-case vs. average-case complexity
6. Uniformity assumptions in hashing
7. Hash function and slots in hash tables
8. Pigeonhole principle and collisions
9. Birthday problem and its implications for hashing
10. Option 1: Hope for the best with hash collisions
11. Option 2: Chaining as a solution for collisions
12. Implementation of chaining in hash tables
13. Complexity of insertion, retrieval, and deletion in chaining
14. Load factor (α) and its significance
15. Average case complexity with uniform hashing
16. Effects of load factor on search and storage performance
17. Resizing hash tables and rehashing
18. Amortized complexity and its relation to resizing
19. Engineering considerations for choosing load factors
20. Uniform hashing implications for hash table efficiency
21. Risks of non-uniform data distributions and bad hash functions
22. Alternative collision resolution: Open addressing
23. Linear probing as a method for open addressing
24. Summary of hash table complexities and caveats

Thursday 27 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.8: Variable sized data collections 2](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=98fb3170-762d-4d7c-ae90-b29100fbb558) 17:15, Thu, 27 Feb 2025

1. Introduction to variable size linear data structures
2. Stack implementation using an array with resizing strategy
3. Amortized complexity and its significance
4. Fixed resizing strategy vs. geometric resizing strategy
5. Performance analysis of the doubling resizing strategy
6. Space complexity considerations in array-based implementations
7. Implementing a queue using arrays and pointers
8. Handling empty space and managing array wrap-around
9. Advantages of array-based implementations over linked lists
10. Queue implementation details and operations
11. ArrayList in Java as a built-in data structure
12. Data structures for sets and handling duplicates
13. Implementing a priority queue and associated complexities
14. Introduction to tree-based data structures for priority queues
15. Conclusion on implementation strategies and efficiencies

Tuesday 25 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.7: variable sized data collections 1](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8a3f9b23-14df-4ecd-bef7-b28f0077fd2c) 09:15, Tue, 25 Feb 2025

1. Free bus passes for students
2. Financial support for students
3. Sustainable policies, including fossil-free careers
4. Affordable and better quality housing
5. Importance of student engagement
6. Variable-sized data collections in algorithms
7. Proving algorithm correctness with loop invariants
8. Analyzing algorithm complexity, including the master theorem
9. Impact of data storage on algorithm performance
10. Overview of data structures and their operational complexities
11. Arrays as basic data structures
12. Advantages and limitations of arrays
13. Linked lists: structure and nodes
14. Operations on linked lists: add, retrieve, check empty
15. Complexity analysis of linked lists
16. Comparison of linked lists and arrays
17. Stack data structure: operations and complexities
18. Array-based stack implementation
19. Fixed capacity vs. dynamic resizing of arrays
20. Concept of amortized complexity
21. Analysis of add operations in array-based stacks
22. Worst-case scenarios for array resizing
23. Strategies for improving array-based implementation efficiency
24. Transition from linked lists to array-based implementations
25. Concluding thoughts on data structures and performance comparisons

Thursday 20 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.6: The Master Theorem](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=5d0e7017-5fd3-4073-8759-b28a00fc0ea2) 17:15, Thu, 20 Feb 2025

1. Introduction to the Master Theorem
2. Analysis of time complexity for divide and conquer algorithms
3. Recap of merge sort and its time complexity as O(n log n)
4. Recap of binary search and its time complexity as O(log n)
5. Examples of recursive relations in algorithm analysis
6. Differences in time complexity when extra work increases (e.g., O(n²) scenario)
7. Recurrence relation forms: T(n) = aT(n/b) + f(n)
8. Definition and role of parameters a and b in recurrence relations
9. Understanding the critical polynomial and its significance
10. Master theorem cases:
    - Case 1: f(n) is polynomially smaller than n^(log_b(a))
    - Case 2: f(n) is asymptotically equal to n^(log_b(a))
    - Case 3: f(n) is polynomially larger than n^(log_b(a))
11. Bounded growth in comparison to critical polynomials
12. Specific examples illustrating each case of the Master Theorem
13. Challenges when f(n) contains logarithmic factors
14. Instances where Master Theorem cannot be applied
15. Proof outline for Case 2 of the Master Theorem
16. Calculation and manipulation of recursive definitions
17. Transitioning from critical polynomials to logarithmic factors
18. Emphasis on the importance of function growth in algorithms
19. Conclusion of the Master Theorem's application in algorithm analysis
20. Preview of topics on data structures for the next lecture

Tuesday 18 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.5: The complexity of sorting](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=4890b503-8089-4e5c-a04c-b2880078869e) 09:15, Tue, 18 Feb 2025

1. Introduction to sorting complexity.
2. Comparison-based sorting definition.
3. Operations allowed: element comparisons (less than).
4. Analysis of sorting algorithms: Selection sort, Insertion sort, Shell sort, Merge sort.
5. Complexity comparisons: O(n²) vs. O(n^(3/2)) vs. O(n log n).
6. Overview of Merge Sort algorithm.
7. Recursive structure of Merge Sort: splitting into halves.
8. Height of binary trees in sorting algorithms.
9. Relationship between comparisons and binary tree height.
10. Logarithmic growth and its significance in complexity analysis.
11. Comparison-based sorting and information gain through comparisons.
12. Exploring possible outcomes and permutations of sorted elements.
13. Inductive proof of binary tree properties.
14. Proving that a binary tree of height L has at most 2^L leaves.
15. Factorial growth: n! and its properties.
16. Logarithmic properties and rules: log properties for manipulation.
17. Upper bound proof: n! ≤ n^n.
18. Lower bound proof: n! is not bounded below by n^n.
19. Proving log(n!) is O(n log n).
20. Establishing log(n!) is Θ(n log n) using asymptotic analysis.
21. Theoretical limits of comparison-based sorting algorithms.
22. Conclusion on the efficiency of Merge Sort within comparison-based sorting.

Thursday 13 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.4: interesting sorting algorithms](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=8afc49ae-83ec-4dcb-8db0-b28300fbcfbd) 17:15, Thu, 13 Feb 2025

1. Introduction to sorting algorithms
2. Overview of Donald Knuth and his contributions to computer science
3. Importance of Knuth's book and Chapter 3 on sorting
4. Introduction to Shell Sort
5. Comparison of Shell Sort and Insertion Sort
6. Mechanics of Shell Sort (choosing gaps and insertion sorting)
7. Complexity of Shell Sort and performance benefits
8. Gap sequences in Shell Sort
9. Correctness of Shell Sort
10. Overview of Merge Sort
11. Divide and conquer strategy in Merge Sort
12. Mechanics of Merge Sort (splitting and merging)
13. Complexity analysis of Merge Sort
14. Recurrence relation representation for Merge Sort
15. Proof of correctness for the merge operation
16. Loop invariants in Merge Sort
17. Comparison of performance between different sorting algorithms
18. Situations for using Shell Sort vs. Merge Sort
19. Conclusion and important takeaways from the lecture

Tuesday 11 Feb 2025

▼ [Algorithms and Complexity](https://lectures.circuit10.uk/#) [CM22008 2.3: Simple Sorting Algorithms; Loop Invariants](https://uniofbath.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=e4ee77ee-a9df-42fe-9f20-b28100784922) 09:15, Tue, 11 Feb 2025

1. Introduction to algorithm analysis
2. Asymptotic complexity and big Θ notation
3. Loop invariants as reasoning tools
4. Importance of sorting algorithms
5. Selection Sort algorithm
6. Correctness of Selection Sort using loop invariants
7. Complexity of Selection Sort (Θ(n²))
8. Insertion Sort algorithm
9. Correctness of Insertion Sort using loop invariants
10. Complexity of Insertion Sort (Best case: Θ(n), Worst case: Θ(n²), Average case: Θ(n²))
11. Physical demonstration using Bananagrams
12. Comparison of Sorting algorithms: Selection Sort vs. Insertion Sort
13. Real-world applications of sorting
14. Discussion of worst-case, best-case, and average-case complexities
15. Transition to more complex sorting algorithms in future lectures