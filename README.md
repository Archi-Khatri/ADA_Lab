# Analysis and Design of Algorithms — Lab Programs

**Course:** Analysis and Design of Algorithms (23CS4PCADA)

**Institution:** B.M.S. College of Engineering, Bengaluru (Autonomous Institution under VTU)

**Student:** Archi R Khatri (1BM24CS051)

**Department:** Computer Science and Engineering

**Academic Year:** 2025–26 (February to June 2026)

---

## Repository Structure

```
ADA-Lab/
├── 1- Topologocal.c
├── 1- Topological.png
├── 2- Johnson's_Trotter.c
├── 2- Johnson's Trotter.png
├── 3 - Merge_Sort.c
├── 3 - Merge_Sort.png
├── 4 - Quick_sort.c
├── 4- Quick_Sort.png
├── 5 - Heap_Select.c
├── 5 - Heap_Select.png
├── 6 - Knapsack01.c
├── 6 - Knapsack01.png
├── 7 - Floyd.c
├── 7 - Floyd.png
├── 8 - Prims.c
├── 8 - Kruskals.c
├── 8 - MST.png
├── 9 - Fractional_Knapsack.c
├── 9 - Fractional_Knapsack.png
├── 10 -Dijsktra.c
├── 10 - Dijsktra.png
├── 11 - N_Queens.c
├── 11 - N_Queens.png
└── README.md
```

---

## Lab Programs

| # | Experiment | Algorithm Paradigm | Time Complexity |
|---|------------|-------------------|-----------------|
| 1 | Topological Ordering of Vertices in a Directed Graph | Graph / DFS | O(V + E) |
| 2 | Johnson-Trotter Algorithm to Generate Permutations | Decrease & Conquer | O(n!) |
| 3 | Merge Sort with Time Analysis | Divide & Conquer | O(n log n) |
| 4 | Quick Sort with Time Analysis | Divide & Conquer | O(n log n) avg, O(n²) worst |
| 5 | Heap Sort with Time Analysis | Transform & Conquer | O(n log n) |
| 6 | 0/1 Knapsack Problem | Dynamic Programming | O(n × W) |
| 7 | All Pairs Shortest Paths (Floyd-Warshall) | Dynamic Programming | O(V³) |
| 8 | Minimum Cost Spanning Tree (Prim's & Kruskal's) | Greedy | O(E log E) |
| 9 | Fractional Knapsack | Greedy | O(n log n) |
| 10 | Single Source Shortest Path (Dijkstra's) | Greedy | O(V²) |
| 11 | N-Queens Problem | Backtracking | O(N!) |

---

## Program Descriptions

### 1. Topological Sort
Performs a DFS-based topological ordering of vertices in a directed acyclic graph (DAG). Vertices are pushed onto a stack after all their descendants are visited, and the stack is then printed to yield the topological order.

### 2. Johnson-Trotter Algorithm
Generates all permutations of n elements by repeatedly swapping the largest "mobile" element — one whose direction arrow points toward a smaller adjacent element. Each swap yields a new permutation with exactly one transposition from the previous.

### 3. Merge Sort
Recursively divides the array into halves, sorts each half, and merges them back in sorted order. Guarantees O(n log n) in all cases with O(n) auxiliary space. Includes wall-clock time measurement.

### 4. Quick Sort (Randomized)
Uses a randomized pivot selection to partition the array around a pivot, then recursively sorts both partitions. Random pivot selection reduces the likelihood of worst-case O(n²) behavior. Includes time measurement over 50,000 iterations for accuracy.

### 5. Heap Sort
Builds a max-heap from the input array, then repeatedly extracts the maximum element to produce a sorted array. Fully in-place with O(1) extra space. Includes time measurement.

### 6. 0/1 Knapsack (Dynamic Programming)
Solves the 0/1 Knapsack problem using a bottom-up DP table of size (n+1) × (W+1). Each cell stores the maximum value achievable with the first `i` items and a weight capacity of `w`. Items cannot be split.

### 7. Floyd-Warshall Algorithm
Computes shortest paths between all pairs of vertices in a weighted graph. Iterates over all intermediate vertices, relaxing distances. Handles graphs with no negative cycles. Outputs a complete shortest distance matrix.

### 8. Minimum Spanning Tree — Prim's & Kruskal's
Two separate implementations of MST construction:
- **Prim's**: Grows the MST one vertex at a time by always adding the minimum weight edge connecting the current tree to an unvisited vertex.
- **Kruskal's**: Sorts all edges by weight and adds them to the MST using a Union-Find structure, skipping edges that would form a cycle.

### 9. Fractional Knapsack (Greedy)
Sorts items by their profit-to-weight ratio in descending order, then greedily fills the knapsack — taking full items where possible and a fraction of the next item if it exceeds remaining capacity.

### 10. Dijkstra's Shortest Path
Finds the shortest path from a given source vertex to a destination in a weighted graph using a greedy approach with an adjacency matrix. Tracks parent pointers to reconstruct and print the actual path.

### 11. N-Queens Problem (Backtracking)
Places N queens on an N×N chessboard such that no two queens attack each other (no shared row, column, or diagonal). Uses recursive backtracking with a `place()` check to prune invalid configurations.

---

## How to Compile and Run

All programs are written in C. Use `gcc` to compile:

```bash
gcc <filename>.c -o <output_name>
./<output_name>
```

**Example:**
```bash
gcc topological.c -o topological
./topological
```

For programs using the math library or time functions, no additional flags are needed beyond the standard compilation command above.

---

## Course Outcomes

| CO | Description |
|----|-------------|
| CO1 | Analyze time complexity of algorithms using asymptotic notations |
| CO2 | Apply various algorithm design techniques for a given problem |
| CO3 | Evaluate the appropriate algorithm/design technique for solving a given problem |
| CO4 | Conduct practical experiments by applying appropriate algorithm design technique to solve problems |

---

*Submitted in partial fulfillment for the award of Bachelor of Engineering in Computer Science and Engineering, Visvesvaraya Technological University, Belgaum.*
