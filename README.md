# Coding_interview_python

Note : this is a collection i created from several other resources available online for my reference .all credits to the creaters 

https://www.youtube.com/watch?v=FT55Gu_-3V8&ab_channel=DTechGeek

Data Structures

Data structures can often be a major part of optimizing and organizing your codebase. While deep-dives on each of these concepts are outside the scope of this article, we’ve provided a cheat-sheet for your next technical interview below. Find any that sound interesting? We encourage further reading to master them!

Heap
This kind of binary tree places the smallest value at the top. Helpful when creating priority queues.

Array
A data structure that places items sequentially. Offers fast lookups and appends, but its fixed size requires careful planning.

Dynamic Array
Similar to an ordinary array, except that a dynamic array expands to fit additional elements as needed.

Linked List
A flexibly-sized list in which each item contains a pointer for the next element. Although the list is easy to expand, lookups can take a lot of time.

Queue
A data structure in which each item is stored in the order it’s received.

Stack
A data structure in which the last item to be stored is the first item to be addressed.

Graph
Not an X/Y chart. Graphs are formed by nodes, and the relationships between the nodes are denoted via lines (edges). Good for creating functional diagrams, but difficult to scale.

Trie
Also known as a prefix tree, the trie is designed to store strings in a compact manner—mostly in cases where you’re storing words with a large number of shared prefixes.

Priority Queue
Distinct from a regular queue. Each item in the queue is given a priority, and higher-priority items are addressed first regardless of when they entered the queue. See also: Heap.

Bloom Filter
A probabilistic data structure that allows administrators to understand whether a set contains a given item—sometimes.

LRU Cache
Here, LRU stands for “Least Recently Used.” It’s a data structure that shows which item has gone unused for longest.

Hash Table
Also known as a hash table, this data structure stores hashed items for quick lookup.

Binary Tree (AKA Binary Search Tree or BST)
A tree in which the nodes to the left are always smaller than the nodes to the right. Balanced trees offer the best performance.

Red-Black Tree
A tree in which the black values remain constant, and the red values may change.

B-Tree
A self-balancing BST variant in which nodes are allowed to have more than two children.

Union Find
Also known as disjoint set structure. Stores non-overlapping sets.

Search
Candidates asked to implement search will most likely encounter one of two search methods in a technical interview—breadth first search and depth first search.

Breadth first search (BFS) searches across the tiers of a tree—first the top node, then the layer of nodes beneath it, then the nodes beneath that, and so on. The primary advantage of BFS is that it can be used to find the shortest path between any two nodes.

Meanwhile, depth first search (DFS) searches down pathways. Starting at the root of a data tree, it then searches all the way down one branch before moving on to the next. DFS is easy to implement and requires less memory most of the time.

Efficient Sorting
Sorting algorithms are another huge component of creating efficient code. Again, you don’t need to memorize the algorithms below, but you should be aware of their time and space complexity.

Selection Sort
The cursor scrolls left to right through a dataset. Every time the right number is smaller than the left number, the right number gets moved to the all the way to the left until the whole data set is sorted. Simple but inefficient.

Insertion Sort
The cursor compares itself to numbers on the left. If smaller, it changes places with the leftmost number and iterates until the data set is sorted.

Merge Sort
Divides the data set in half, then continues dividing until each item is an individual subset. Once this action is complete, the algorithm recombines the data set, sorting as it does.

Quicksort
An algorithm that recursively divides a data set into two halves, placing smaller elements to the left and larger elements to the right, until the whole data set is sorted.

Bubble Sort
Scrolls through a data set comparing every pair of numbers, placing the larger number on the right and the smaller number on the left, until the entire data set is sorted.

Heapsort
A “max heap” is created from a data set by comparing parent nodes with child nodes and then swapping them until the largest number is at the root. By deleting the root, swapping the first and last node, and starting the max heap again, you’ll eventually sort all numbers from least to greatest.

Types of Algorithms
Lastly, you should know the basic types of algorithms.

A recursive algorithm triggers itself repeatedly until it reaches what’s known as a base case, which is when the algorithm stops.

An iterative algorithm also loops repeatedly, but only while a certain condition is true. These can be somewhat more efficient than recursive algorithms, but recursive algorithms can solve more complex problems.

A greedy algorithm is given a set of specific criteria and then selects data that matches those criteria. This algorithm can improve the time efficiency of an application, but only in cases where there’s a small amount of matching data in a large data set.

Asymptotic Notation
Refer back to the “Review time and space constraints” section of the Do’s and Don’ts above. Asymptotic notation is used to describe how long your algorithm will run when given different inputs. There are three symbols you’ll need to remember:

·   Big O: Under the worst-case scenario, this is how long the algorithm will run

·   Big Omega (Ω): This is the best-case scenario for runtime

·   Big Theta (Θ): The runtime value is the same in the best-case and worst-case scenarios

In a multi-part algorithm, the runtime is always calculated using its slowest part. Please note: you can always communicate your applications’ performance constraints if you’re unfamiliar with this terminology in a pinch.



# Tech Interview Cheat Sheet

# Table of Content
- [Asymptotic Notation](#asymptotic-notation)
- [Data Structures](#data-structures)
  - [Array](#array)
  - [Linked List](#linked-list)
  - [Hash Table or Hash Map](#hash)
  - [Binary Tree](#binary-tree)
- [Algorithms](#algorithms)
  - [Algorithm Basics](#algorithm-basics)
  - [Search Algorithms](#search-algorithms)
    - [Breadth First Search](#breadth-first-search)
    - [Depth First Search](#depth-first-search)
  - [Sorting Algorithms](#sorting-algorithms)
    - [Selection Sort](#selection-sort)
    - [Insertion Sort](#insertion-sort)
    - [Merge Sort](#merge-sort)
    - [Quick Sort](#quick-sort)
- [Additional Resources](#additional-resources)


# <a id="asymptotic-notation"></a>Asymptotic Notation
### Definition:
Asymptotic Notation is the hardware independent notation used to tell the time and space complexity of an algorithm. Meaning it's a standardized way of measuring how much memory an algorithm uses or how long it runs for given an input.

#### Complexities
The following are the Asymptotic rates of growth from best to worst:
- constant growth - ``O(1)`` Runtime is constant and does not grow with `n`
- logarithmic growth – ``O(log n)`` Runtime grows logarithmically in proportion to `n`
- linear growth – ``O(n)`` Runtime grows directly in proportion to `n`
- superlinear growth – ``O(n log n)`` Runtime grows in proportion _and_ logarithmically to `n`
- polynomial growth – `O(n^c)` Runtime grows quicker than previous all based on `n`
- exponential growth – `O(c^n)` Runtime grows even faster than polynomial growth based on `n`
- factorial growth – `O(n!)` Runtime grows the fastest and becomes quickly unusable for even
small values of `n`

[(source: Soumyadeep Debnath, _Analysis of Algorithms | Big-O analysis_)](https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/)

Visualized below; the x-axis representing input size and the y-axis representing complexity:

![#](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Comparison_computational_complexity.svg/400px-Comparison_computational_complexity.svg.png)

[(source: Wikipedia, _Computational Complexity of Mathematical Operations_)](https://en.wikipedia.org/wiki/Computational_complexity_of_mathematical_operations)

#### Big-O notation
Big-O refers to the upper bound of time or space complexity of an algorithm, meaning it worst case runtime scenario. An easy way to think of it is that runtime could be better than Big-O but it will never be worse.
#### Big-Ω (Big-Omega) notation
Big-Omega refers to the lower bound of time or space complexity of an algorithm, meaning it is the best runtime scenario. Or runtime could worse than Big-Omega, but it will never be better.
#### Big-θ (Big-Theta) notation
Big-Theta refers to the tight bound of time or space complexity of an algorithm. Another way to think of it is the intersection of Big-O and Big-Omega, or more simply runtime is guaranteed to be a given complexity, such as `n log n`.

#### What you need to know
- Big-O and Big-Theta are the most common and helpful notations
- Big-O does _not_ mean Worst Case Scenario, Big-Theta does _not_ mean average case, and Big-Omega does _not_ mean Best Case Scenario. They only connote the algorithm's performance for a particular scenario, and all three can be used for any scenario.
- Worst Case means given an unideal input, Average Case means given a typical input, Best case means a ideal input. Ex. Worst case means given an input the algorithm performs particularly bad, or best case an already sorted array for a sorting algorithm.
- Best Case and Big Omega are generally not helpful since Best Cases are rare in the real world and lower bound might be very different than an upper bound.
- Big-O isn't everything. On paper merge sort is faster than quick sort, but in practice quick sort is superior.

# <a id="data-structures"></a>Data Structures
### <a id="array"></a> Array
#### Definition
- Stores data elements based on an sequential, most commonly 0 based, index.
- Based on [tuples](http://en.wikipedia.org/wiki/Tuple) from set theory.
- They are one of the oldest, most commonly used data structures.

#### What you need to know
- Optimal for indexing; bad at searching, inserting, and deleting (except at the end).
- **Linear arrays**, or one dimensional arrays, are the most basic.
  - Are static in size, meaning that they are declared with a fixed size.
- **Dynamic arrays** are like one dimensional arrays, but have reserved space for additional elements.
  - If a dynamic array is full, it copies its contents to a larger array.
- **Multi dimensional arrays** nested arrays that allow for multiple dimensions such as an array of arrays providing a 2 dimensional spacial representation via x, y coordinates.

#### Time Complexity
- Indexing:         Linear array: `O(1)`,      Dynamic array: `O(1)`
- Search:           Linear array: `O(n)`,      Dynamic array: `O(n)`
- Optimized Search: Linear array: `O(log n)`,  Dynamic array: `O(log n)`
- Insertion:        Linear array: n/a,         Dynamic array: `O(n)`


### <a id="linked-list"></a> Linked List
#### Definition
- Stores data with **nodes** that point to other nodes.
  - Nodes, at its most basic it has one datum and one reference (another node).
  - A linked list _chains_ nodes together by pointing one node's reference towards another node.

#### What you need to know
- Designed to optimize insertion and deletion, slow at indexing and searching.
- **Doubly linked list** has nodes that also reference the previous node.
- **Circularly linked list** is simple linked list whose **tail**, the last node, references the **head**, the first node.
- **Stack**, commonly implemented with linked lists but can be made from arrays too.
  - Stacks are **last in, first out** (LIFO) data structures.
  - Made with a linked list by having the head be the only place for insertion and removal.
- **Queues**, too can be implemented with a linked list or an array.
  - Queues are a **first in, first out** (FIFO) data structure.
  - Made with a doubly linked list that only removes from head and adds to tail.

#### Time Complexity
- Indexing:         Linked Lists: `O(n)`
- Search:           Linked Lists: `O(n)`
- Optimized Search: Linked Lists: `O(n)`
- Append:           Linked Lists: `O(1)`
- Prepend:          Linked Lists: `O(1)`
- Insertion:        Linked Lists: `O(n)`


### <a id="hash"></a> Hash Table or Hash Map
#### Definition
- Stores data with key value pairs.
- **Hash functions** accept a key and return an output unique only to that specific key.
  - This is known as **hashing**, which is the concept that an input and an output have a one-to-one correspondence to map information.
  - Hash functions return a unique address in memory for that data.

#### What you need to know
- Designed to optimize searching, insertion, and deletion.
- **Hash collisions** are when a hash function returns the same output for two distinct inputs.
  - All hash functions have this problem.
  - This is often accommodated for by having the hash tables be very large.
- Hashes are important for associative arrays and database indexing.

#### Time Complexity
- Indexing:         Hash Tables: `O(1)`
- Search:           Hash Tables: `O(1)`
- Insertion:        Hash Tables: `O(1)`


### <a id="binary-tree"></a> Binary Tree
#### Definition
- Is a tree like data structure where every node has at most two children.
  - There is one left and right child node.

#### What you need to know
- Designed to optimize searching and sorting.
- A **degenerate tree** is an unbalanced tree, which if entirely one-sided, is essentially a linked list.
- They are comparably simple to implement than other data structures.
- Used to make **binary search trees**.
  - A binary tree that uses comparable keys to assign which direction a child is.
  - Left child has a key smaller than its parent node.
  - Right child has a key greater than its parent node.
  - There can be no duplicate node.
  - Because of the above it is more likely to be used as a data structure than a binary tree.

#### Time Complexity
- Indexing:  Binary Search Tree: `O(log n)`
- Search:    Binary Search Tree: `O(log n)`
- Insertion: Binary Search Tree: `O(log n)`


# <a id="algorithms"></a> Algorithms
## <a id="algorithm-basics"></a> Algorithm Basics
### Recursive Algorithms
#### Definition
- An algorithm that calls itself in its definition.
  - **Recursive case** a conditional statement that is used to trigger the recursion.
  - **Base case** a conditional statement that is used to break the recursion.

#### What you need to know
- **Stack level too deep** and **stack overflow**.
  - If you've seen either of these from a recursive algorithm, you messed up.
  - It means that your base case was never triggered because it was faulty or the problem was so massive you ran out of alloted memory.
  - Knowing whether or not you will reach a base case is integral to correctly using recursion.
  - Often used in Depth First Search


### Iterative Algorithms
#### Definition
- An algorithm that is called repeatedly but for a finite number of times, each time being a single iteration.
  - Often used to move incrementally through a data set.

#### What you need to know
- Generally you will see iteration as loops, for, while, and until statements.
- Think of iteration as moving one at a time through a set.
- Often used to move through an array.

#### Recursion Vs. Iteration
- The differences between recursion and iteration can be confusing to distinguish since both can be used to implement the other. But know that,
  - Recursion is, usually, more expressive and easier to implement.
  - Iteration uses less memory.
- **Functional languages** tend to use recursion. (i.e. Haskell)
- **Imperative languages** tend to use iteration. (i.e. Ruby)
- Check out this [Stack Overflow post](http://stackoverflow.com/questions/19794739/what-is-the-difference-between-iteration-and-recursion) for more info.

#### Pseudo Code of Moving Through an Array
```
Recursion                         | Iteration
----------------------------------|----------------------------------
recursive method (array, n)       | iterative method (array)
  if array[n] is not nil          |   for n from 0 to size of array
    print array[n]                |     print(array[n])
    recursive method(array, n+1)  |
  else                            |
    exit loop                     |
```

### Greedy Algorithms
#### Definition
- An algorithm that, while executing, selects only the information that meets a certain criteria.
- The general five components, taken from [Wikipedia](http://en.wikipedia.org/wiki/Greedy_algorithm#Specifics):
  - A candidate set, from which a solution is created.
  - A selection function, which chooses the best candidate to be added to the solution.
  - A feasibility function, that is used to determine if a candidate can be used to contribute to a solution.
  - An objective function, which assigns a value to a solution, or a partial solution.
  - A solution function, which will indicate when we have discovered a complete solution.

#### What you need to know
- Used to find the expedient, though non-optimal, solution for a given problem.
- Generally used on sets of data where only a small proportion of the information evaluated meets the desired result.
- Often a greedy algorithm can help reduce the Big O of an algorithm.

#### Pseudo Code of a Greedy Algorithm to Find Largest Difference of any Two Numbers in an Array.
```
greedy algorithm (array)
  var largest difference = 0
  var new difference = find next difference (array[n], array[n+1])
  largest difference = new difference if new difference is > largest difference
  repeat above two steps until all differences have been found
  return largest difference
```

This algorithm never needed to compare all the differences to one another, saving it an entire iteration.

## <a id="search-algorithms"></a>Search Algorithms
### <a id="breadth-first-search"></a>Breadth First Search
#### Definition
- An algorithm that searches a tree (or graph) by searching levels of the tree first, starting at the root.
  - It finds every node on the same level, most often moving left to right.
  - While doing this it tracks the children nodes of the nodes on the current level.
  - When finished examining a level it moves to the left most node on the next level.
  - The bottom-right most node is evaluated last (the node that is deepest and is farthest right of it's level).

#### What you need to know
- Optimal for searching a tree that is wider than it is deep.
- Uses a queue to store information about the tree while it traverses a tree.
  - Because it uses a queue it is more memory intensive than **depth first search**.
  - The queue uses more memory because it needs to stores pointers

#### Time Complexity
- Search: Breadth First Search: O(V + E)
- E is number of edges
- V is number of vertices

### <a id="depth-first-search"></a>Depth First Search
#### Definition
- An algorithm that searches a tree (or graph) by searching depth of the tree first, starting at the root.
  - It traverses left down a tree until it cannot go further.
  - Once it reaches the end of a branch it traverses back up trying the right child of nodes on that branch, and if possible left from the right children.
  - When finished examining a branch it moves to the node right of the root then tries to go left on all it's children until it reaches the bottom.
  - The right most node is evaluated last (the node that is right of all it's ancestors).

#### What you need to know
- Optimal for searching a tree that is deeper than it is wide.
- Uses a stack to push nodes onto.
  - Because a stack is LIFO it does not need to keep track of the nodes pointers and is therefore less memory intensive than breadth first search.
  - Once it cannot go further left it begins evaluating the stack.

#### Time Complexity
- Search: Depth First Search: O(|E| + |V|)
- E is number of edges
- V is number of vertices


#### Breadth First Search Vs. Depth First Search
- The simple answer to this question is that it depends on the size and shape of the tree.
  - For wide, shallow trees use Breadth First Search
  - For deep, narrow trees use Depth First Search

#### Nuances
  - Because BFS uses queues to store information about the nodes and its children, it could use more memory than is available on your computer. (But you probably won't have to worry about this.)
  - If using a DFS on a tree that is very deep you might go unnecessarily deep in the search. See [xkcd](http://xkcd.com/761/) for more information.
  - Breadth First Search tends to be a looping algorithm.
  - Depth First Search tends to be a recursive algorithm.


## <a id="sorting-algorithms"></a>Sorting Algorithms

### <a id="selection-sort"></a>Selection Sort
#### Definition
- A comparison based sorting algorithm.
  - Starts with the cursor on the left, iterating left to right
  - Compares the left side to the right, looking for the smallest known item
    - If the left is smaller than the item to the right it continues iterating
    - If the left is bigger than the item to the right, the item on the right becomes the known smallest number
    - Once it has checked all items, it moves the known smallest to the cursor and advances the cursor to the right and starts over
  - As the algorithm processes the data set, it builds a fully sorted left side of the data until the entire data set is sorted
- Changes the array in place.

#### What you need to know
- Inefficient for large data sets.
- Very simple to implement.

#### Time Complexity
- Best Case Sort: `O(n^2)`
- Average Case Sort: `O(n^2)`
- Worst Case Sort: `O(n^2)`

#### Space Complexity
- Worst Case: `O(1)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/9/94/Selection-Sort-Animation.gif)

[(source: Wikipedia, _Selection Sort_)](https://en.wikipedia.org/wiki/Selection_sort)

### <a id="insertion-sort"></a>Insertion Sort
#### Definition
- A comparison based sorting algorithm.
  - Iterates left to right comparing the current cursor to the previous item.
  - If the cursor is smaller than the item on the left it swaps positions and the cursor compares itself again to the left hand side until it is put in its sorted position.
  - As the algorithm processes the data set, the left side becomes increasingly sorted until it is fully sorted.
- Changes the array in place.

#### What you need to know
- Inefficient for large data sets, but can be faster for than other algorithms for small ones.
- Although it has an `O(n^2)` time complexity, in practice it is slightly less since its comparison scheme only requires checking place if it is smaller than its neighbor.

#### Time Complexity
- Best Case: `O(n)`
- Average Case: `O(n^2)`
- Worst Case: `O(n^2)`

#### Space Complexity
- Worst Case: `O(n)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/0/0f/Insertion-sort-example-300px.gif)

[(source: Wikipedia, _Insertion Sort_)](https://en.wikipedia.org/wiki/Insertion_sort)

### <a id="merge-sort"></a>Merge Sort
#### Definition
- A divide and conquer algorithm.
  - Recursively divides entire array by half into subsets until the subset is one, the base case.
  - Once the base case is reached results are returned and sorted ascending left to right.
  - Recursive calls are returned and the sorts double in size until the entire array is sorted.

#### What you need to know
- This is one of the fundamental sorting algorithms.
- Know that it divides all the data into as small possible sets then compares them.

#### Time Complexity
- Worst Case: `O(n log n)`
- Average Case: `O(n log n)`
- Best Case: `O(n)`

#### Space Complexity
- Worst Case: `O(1)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e6/Merge_sort_algorithm_diagram.svg/400px-Merge_sort_algorithm_diagram.svg.png)

[(source: Wikipedia, _Merge Sort_)](https://en.wikipedia.org/wiki/Merge_sort)

### <a id="quick-sort"></a>Quicksort
#### Definition
- A divide and conquer algorithm
  - Partitions entire data set in half by selecting a random pivot element and putting all smaller elements to the left of the element and larger ones to the right.
  - It repeats this process on the left side until it is comparing only two elements at which point the left side is sorted.
  - When the left side is finished sorting it performs the same operation on the right side.
- Computer architecture favors the quicksort process.
- Changes the array in place.

#### What you need to know
- While it has the same Big O as (or worse in some cases) many other sorting algorithms it is often faster in practice than many other sorting algorithms, such as merge sort.

#### Time Complexity
- Worst Case: `O(n^2)`
- Average Case: `O(n log n)`
- Best Case: `O(n log n)`

#### Space Complexity
- Worst Case: `O(log n)`

#### Visualization
![#](https://upload.wikimedia.org/wikipedia/commons/6/6a/Sorting_quicksort_anim.gif)

[(source: Wikipedia, _Quicksort_)](https://en.wikipedia.org/wiki/Quicksort)

#### Merge Sort Vs. Quicksort
- Quicksort is likely faster in practice, but merge sort is faster on paper.
- Merge Sort divides the set into the smallest possible groups immediately then reconstructs the incrementally as it sorts the groupings.
- Quicksort continually partitions the data set by a pivot, until the set is recursively sorted.

# Data Structure Basics

### **Array**
#### Definition:
- Stores data elements based on an sequential, most commonly 0 based, index.
- Based on [tuples](http://en.wikipedia.org/wiki/Tuple) from set theory.
- They are one of the oldest, most commonly used data structures.

#### What you need to know:
- Optimal for indexing; bad at searching, inserting, and deleting (except at the end).
- **Linear arrays**, or one dimensional arrays, are the most basic.
  - Are static in size, meaning that they are declared with a fixed size.
- **Dynamic arrays** are like one dimensional arrays, but have reserved space for additional elements.
  - If a dynamic array is full, it copies its contents to a larger array.
- **Multi dimensional arrays** nested arrays that allow for multiple dimensions such as an array of arrays providing a 2 dimensional spacial representation via x, y coordinates.

#### Time Complexity:
- Indexing:         Linear array: O(1),      Dynamic array: O(1)
- Search:           Linear array: O(n),      Dynamic array: O(n)
- Optimized Search: Linear array: O(log n), Dynamic array: O(log n)
- Insertion:        Linear array: n/a        Dynamic array: O(n)


### **Linked List**
#### Definition:
- Stores data with **nodes** that point to other nodes.
  - Nodes, at its most basic it has one datum and one reference (another node).
  - A linked list _chains_ nodes together by pointing one node's reference towards another node.

#### What you need to know:
- Designed to optimize insertion and deletion, slow at indexing and searching.
- **Doubly linked list** has nodes that also reference the previous node.
- **Circularly linked list** is simple linked list whose **tail**, the last node, references the **head**, the first node.
- **Stack**, commonly implemented with linked lists but can be made from arrays too.
  - Stacks are **last in, first out** (LIFO) data structures.
  - Made with a linked list by having the head be the only place for insertion and removal.
- **Queues**, too can be implemented with a linked list or an array.
  - Queues are a **first in, first out** (FIFO) data structure.
  - Made with a doubly linked list that only removes from head and adds to tail.

#### Time Complexity:
- Indexing:         Linked Lists: O(n)
- Search:           Linked Lists: O(n)
- Optimized Search: Linked Lists: O(n)
- Insertion:        Linked Lists: O(1)


### **Hash Table or Hash Map**
#### Definition:
- Stores data with key value pairs.
- **Hash functions** accept a key and return an output unique only to that specific key.
  - This is known as **hashing**, which is the concept that an input and an output have a one-to-one correspondence to map information.
  - Hash functions return a unique address in memory for that data.

#### What you need to know:
- Designed to optimize searching, insertion, and deletion.
- **Hash collisions** are when a hash function returns the same output for two distinct inputs.
  - All hash functions have this problem.
  - This is often accommodated for by having the hash tables be very large.
- Hashes are important for associative arrays and database indexing.

#### Time Complexity:
- Indexing:         Hash Tables: O(1)
- Search:           Hash Tables: O(1)
- Insertion:        Hash Tables: O(1)


### **Binary Tree**
#### Definition:
- Is a tree like data structure where every node has at most two children.
  - There is one left and right child node.

#### What you need to know:
- Designed to optimize searching and sorting.
- A **degenerate tree** is an unbalanced tree, which if entirely one-sided is a essentially a linked list.
- They are comparably simple to implement than other data structures.
- Used to make **binary search trees**.
  - A binary tree that uses comparable keys to assign which direction a child is.
  - Left child has a key smaller than it's parent node.
  - Right child has a key greater than it's parent node.
  - There can be no duplicate node.
  - Because of the above it is more likely to be used as a data structure than a binary tree.

#### Time Complexity:
- Indexing:  Binary Search Tree: O(log n)
- Search:    Binary Search Tree: O(log n)
- Insertion: Binary Search Tree: O(log n)


## Search Basics
### **Breadth First Search**
#### Definition:
- An algorithm that searches a tree (or graph) by searching levels of the tree first, starting at the root.
  - It finds every node on the same level, most often moving left to right.
  - While doing this it tracks the children nodes of the nodes on the current level.
  - When finished examining a level it moves to the left most node on the next level.
  - The bottom-right most node is evaluated last (the node that is deepest and is farthest right of it's level).

#### What you need to know:
- Optimal for searching a tree that is wider than it is deep.
- Uses a queue to store information about the tree while it traverses a tree.
  - Because it uses a queue it is more memory intensive than **depth first search**.
  - The queue uses more memory because it needs to stores pointers

#### Time Complexity:
- Search: Breadth First Search: O(V + E)
- E is number of edges
- V is number of vertices

### **Depth First Search**
#### Definition:
- An algorithm that searches a tree (or graph) by searching depth of the tree first, starting at the root.
  - It traverses left down a tree until it cannot go further.
  - Once it reaches the end of a branch it traverses back up trying the right child of nodes on that branch, and if possible left from the right children.
  - When finished examining a branch it moves to the node right of the root then tries to go left on all it's children until it reaches the bottom.
  - The right most node is evaluated last (the node that is right of all it's ancestors).

#### What you need to know:
- Optimal for searching a tree that is deeper than it is wide.
- Uses a stack to push nodes onto.
  - Because a stack is LIFO it does not need to keep track of the nodes pointers and is therefore less memory intensive than breadth first search.
  - Once it cannot go further left it begins evaluating the stack.

#### Time Complexity:
- Search: Depth First Search: O(|E| + |V|)
- E is number of edges
- V is number of vertices


#### Breadth First Search Vs. Depth First Search
- The simple answer to this question is that it depends on the size and shape of the tree.
  - For wide, shallow trees use Breadth First Search
  - For deep, narrow trees use Depth First Search

#### Nuances:
  - Because BFS uses queues to store information about the nodes and its children, it could use more memory than is available on your computer. (But you probably won't have to worry about this.)
  - If using a DFS on a tree that is very deep you might go unnecessarily deep in the search. See [xkcd](http://xkcd.com/761/) for more information.
  - Breadth First Search tends to be a looping algorithm.
  - Depth First Search tends to be a recursive algorithm.


## Efficient Sorting Basics
### **Merge Sort**
#### Definition:
- A comparison based sorting algorithm
  - Divides entire dataset into groups of at most two.
  - Compares each number one at a time, moving the smallest number to left of the pair.
  - Once all pairs sorted it then compares left most elements of the two leftmost pairs creating a sorted group of four with the smallest numbers on the left and the largest ones on the right.
  - This process is repeated until there is only one set.

#### What you need to know:
- This is one of the most basic sorting algorithms.
- Know that it divides all the data into as small possible sets then compares them.

#### Time Complexity:
- Best Case Sort: Merge Sort: O(n)
- Average Case Sort: Merge Sort: O(n log n)
- Worst Case Sort: Merge Sort: O(n log n)

### **Quicksort**
#### Definition:
- A comparison based sorting algorithm
  - Divides entire dataset in half by selecting the middle element and putting all smaller elements to the left of the element and larger ones to the right.
  - It repeats this process on the left side until it is comparing only two elements at which point the left side is sorted.
  - When the left side is finished sorting it performs the same operation on the right side.
- Computer architecture favors the quicksort process.

#### What you need to know:
- While it has the same Big O as (or worse in some cases) many other sorting algorithms it is often faster in practice than many other sorting algorithms, such as merge sort.
- Know that it halves the data set by the average continuously until all the information is sorted.

#### Time Complexity:
- Best Case Sort: Merge Sort: O(n)
- Average Case Sort: Merge Sort: O(n log n)
- Worst Case Sort: Merge Sort: O(n^2)

### **Bubble Sort**
#### Definition:
- A comparison based sorting algorithm
  - It iterates left to right comparing every couplet, moving the smaller element to the left.
  - It repeats this process until it no longer moves an element to the left.

#### What you need to know:
- While it is very simple to implement, it is the least efficient of these three sorting methods.
- Know that it moves one space to the right comparing two elements at a time and moving the smaller on to left.

#### Time Complexity:
- Best Case Sort: Merge Sort: O(n)
- Average Case Sort: Merge Sort: O(n^2)
- Worst Case Sort: Merge Sort: O(n^2)

#### Merge Sort Vs. Quicksort
- Quicksort is likely faster in practice.
- Merge Sort divides the set into the smallest possible groups immediately then reconstructs the incrementally as it sorts the groupings.
- Quicksort continually divides the set by the average, until the set is recursively sorted.

## Basic Types of Algorithms
### **Recursive Algorithms**
#### Definition:
- An algorithm that calls itself in its definition.
  - **Recursive case** a conditional statement that is used to trigger the recursion.
  - **Base case** a conditional statement that is used to break the recursion.

#### What you need to know:
- **Stack level too deep** and **stack overflow**.
  - If you've seen either of these from a recursive algorithm, you messed up.
  - It means that your base case was never triggered because it was faulty or the problem was so massive you ran out of alloted memory.
  - Knowing whether or not you will reach a base case is integral to correctly using recursion.
  - Often used in Depth First Search


### **Iterative Algorithms**
#### Definition:
- An algorithm that is called repeatedly but for a finite number of times, each time being a single iteration.
  - Often used to move incrementally through a data set.

#### What you need to know:
- Generally you will see iteration as loops, for, while, and until statements.
- Think of iteration as moving one at a time through a set.
- Often used to move through an array.

#### Recursion Vs. Iteration
- The differences between recursion and iteration can be confusing to distinguish since both can be used to implement the other. But know that,
  - Recursion is, usually, more expressive and easier to implement.
  - Iteration uses less memory.
- **Functional languages** tend to use recursion. (i.e. Haskell)
- **Imperative languages** tend to use iteration. (i.e. Ruby)
- Check out this [Stack Overflow post](http://stackoverflow.com/questions/19794739/what-is-the-difference-between-iteration-and-recursion) for more info.

#### Pseudo Code of Moving Through an Array (this is why iteration is used for this)
```
Recursion                         | Iteration
----------------------------------|----------------------------------
recursive method (array, n)       | iterative method (array)
  if array[n] is not nil          |   for n from 0 to size of array
    print array[n]                |     print(array[n])
    recursive method(array, n+1)  |
  else                            |
    exit loop                     |
```
### **Greedy Algorithm**
#### Definition:
- An algorithm that, while executing, selects only the information that meets a certain criteria.
- The general five components, taken from [Wikipedia](http://en.wikipedia.org/wiki/Greedy_algorithm#Specifics):
  - A candidate set, from which a solution is created.
  - A selection function, which chooses the best candidate to be added to the solution.
  - A feasibility function, that is used to determine if a candidate can be used to contribute to a solution.
  - An objective function, which assigns a value to a solution, or a partial solution.
  - A solution function, which will indicate when we have discovered a complete solution.

#### What you need to know:
- Used to find the expedient, though non-optimal, solution for a given problem.
- Generally used on sets of data where only a small proportion of the information evaluated meets the desired result.
- Often a greedy algorithm can help reduce the Big O of an algorithm.

#### Pseudo Code of a Greedy Algorithm to Find Largest Difference of any Two Numbers in an Array.
```
greedy algorithm (array)
  var largest difference = 0
  var new difference = find next difference (array[n], array[n+1])
  largest difference = new difference if new difference is > largest difference
  repeat above two steps until all differences have been found
  return largest difference
```

This algorithm never needed to compare all the differences to one another, saving it an entire iteration.




Python3 reference for interview coding problems/light competitive programming. Contributions welcome!

## How

I built this cheatsheet while teaching myself Python3 for various interviews and leetcoding for fun after not using Python for about a decade. This cheetsheet only contains code that I didn't know but needed to use to solve a specific coding problem. I did this to try to get a smaller high frequency subset of Python vs a comprehensive list of all methods. Additionally, the act of recording the syntax and algorithms helped me store it in memory and as a result I almost never actually referenced this sheet. Hopefully it helps you in your efforts or inspires you to build your own and best of luck!


## Why

The [rule of least power](https://en.wikipedia.org/wiki/Rule_of_least_power)

I choose Python3 despite being more familiar with Javascript, Java, C++ and Golang for interviews as I felt Python had the combination of the most standard libraries available as well as syntax that resembles psuedo code, therefore being the most expressive. Python and Java both have the most examples but Python wins in this case due to being much more concise. I was able to get myself reasonably prepared with Python syntax in six weeks of practice. After picking up Python I have timed myself solving the same exercises in Golang and Python. Although I prefer Golang, I find that I can complete Python examples in half the time even accounting for +50% more bugs (approximately) that I tend to have in Python vs Go. This is optimizing for solved interview questons under pressure, when performance is considered then Go/C++ does consistently perform 1/10 the time of Python. In some rare cases algorithms that time out in Python that I can get away with in C++/Go on Leetcode. 


[Language Mechanics](#language-mechanics)

1. [Literals](#literals)
1. [Loops](#loops)
1. [Strings](#strings)
1. [Slicing](#slicing)
1. [Tuples](#tuple)
1. [Sort](#sort)
1. [Hash](#hash)
1. [Set](#set)
1. [List](#list)
1. [Dict](#dict)
1. [Binary Tree](#binarytree)
1. [heapq](#heapq)
1. [lambda](#lambda)
1. [zip](#zip)
1. [Random](#random)
1. [Constants](#constants)
1. [Ternary Condition](#ternary)
1. [Bitwise operators](#bitwise-operators)
1. [For Else](#for-else)
1. [Modulo](#modulo)
1. [any](#any)
1. [all](#all)
1. [bisect](#bisect)
1. [math](#math)
1. [iter](#iter)
1. [map](#map)
1. [filter](#filter)
1. [reduce](#reduce)
1. [itertools](#itertools)
1. [regular expression](#regular-expression)
1. [Types](#types)
1. [Grids](#grids)

[Collections](#collections)
1. [Deque](#deque)
1. [Counter](#counter)
1. [Default Dict](#default-dict)

[Algorithms](#algorithms)


1. [General Tips](#general-tips)
1. [Binary Search](#binary-search)
1. [Topological Sort](#topological-sort)
1. [Sliding Window](#sliding-window)
1. [Tree Tricks](#tree-tricks)
1. [Binary Search Tree](#binary-search-tree)
1. [Anagrams](#anagrams)
1. [Dynamic Programming](#dynamic-programming)
1. [Cyclic Sort](#cyclic-sort)
1. [Quick Sort](#quick-sort)
1. [Merge Sort](#merge-sort)
1. [Merge K Sorted Arrays](#merge-arrays)
1. [Linked List](#linked-list)
1. [Convert Base](#convert-base)
1. [Parenthesis](#parenthesis)
1. [Max Profit Stock](#max-profit-stock)
1. [Shift Array Right](#shift-array-right)
1. [Continuous Subarrays with Sum k ](#continuous-subarrays-with-sum-k)
1. [Events](#events)
1. [Merge Meetings](#merge-meetings)
1. [Trie](#trie)
1. [Kadane's Algorithm - Max subarray sum](#kadane)
1. [Union Find/DSU](#union-find)
1. [Fast Power](#fast-power)
1. [Fibonacci Golden](#fibonacci-golden)
1. [Basic Calculator](#basic-calculator)
1. [Reverse Polish](#reverse-polish)
1. [Resevior Sampling](#resevior-sampling)
1. [Candy Crush](#candy-crush)

# Language Mechanics

## Literals

```python
255, 0b11111111, 0o377, 0xff # Integers (decimal, binary, octal, hex)
123.0, 1.23                  # Float
7 + 5j, 7j                   # Complex 
'a', '\141', '\x61'          # Character (literal, octal, hex)
'\n', '\\', '\'', '\"'       # Newline, backslash, single quote, double quote
"string\n"                   # String of characters ending with newline 
"hello"+"world"              # Concatenated strings
True, False                  # bool constants, 1 == True, 0 == False 
[1, 2, 3, 4, 5]              # List 
['meh', 'foo', 5]            # List
(2, 4, 6, 8)                 # Tuple, immutable
{'name': 'a', 'age': 90}     # Dict
'a', 'e', 'i', 'o', 'u'}     # Set
None                         # Null var
```

## Loops

Go through all elements
```python
i = 0
while i < len(str):
  i += 1
```

equivalent
```python
for i in range(len(message)):
  print(i)
```

Get largest number index from right
```python
while i > 0 and nums [i-1] >= nums[i]:
  i -= 1
```

Manually reversing
```python
l, r = i, len(nums) - 1
while l < r:
  nums[l], nums[r] = nums[r], nums[l]
  l += 1
  r -= 1
```

Go past the loop if we are clever with our boundry
```python
for i in range(len(message) + 1):
  if i == len(message) or message[i] == ' ':
```

Fun with Ranges - range(start, stop, step)
```python
for a in range(0,3): # 0,1,2
for a in reversed(range(0,3)) # 2,1,0
for i in range(3,-1,-1) # 3,2,1,0
for i in range(len(A)//2): # A = [0,1,2,3,4,5]
  print(i) # 0,1,2 
  print(A[i]) # 0,1,2
  print(~i) # -1,-2,-3
  print(A[~i]) # 5,4,3
```

## Strings

```python
str1.find('x')          # find first location of char x and return index
str1.rfind('x')         # find first int location of char x from reverse
```

Parse a log on ":"
```python
l = "0:start:0"
tokens = l.split(":")
print(tokens) # ['0', 'start', '0']
```

Reverse works with built in split, [::-1] and " ".join()
```python
# s = "the sky  is blue"
def reverseWords(self, s: str) -> str:  
  wordsWithoutWhitespace = s.split() # ['the', 'sky', 'is', 'blue']
  reversedWords = wordsWithoutWhitespace[::-1] # ['blue', 'is', 'sky', 'the']        
  final = " ".join(reversedWords) # blue is sky the
```

Manual split based on isalpha()
```python
def splitWords(input_string) -> list: 
  words = [] # 
  start = length = 0
  for i, c in enumerate(input_string):
    if c.isalpha():
      if length == 0:
        start = i                    
        length += 1
      else:
        words.append(input_string[start:start+length])
        length = 0
  if length > 0:
    words.append(input_string[start:start+length])
  return words
```

Test type of char
```python
def rotationalCipher(input, rotation_factor):
  rtn = []
  for c in input:
    if c.isupper():
      ci = ord(c) - ord('A')
      ci = (ci + rotation_factor) % 26
      rtn.append(chr(ord('A') + ci))
    elif c.islower():
      ci = ord(c) - ord('a')
      ci = (ci + rotation_factor) % 26
      rtn.append(chr(ord('a') + ci))
    elif c.isnumeric():
      ci = ord(c) - ord('0')
      ci = (ci + rotation_factor) % 10
      rtn.append(chr(ord('0') + ci))
    else:
      rtn.append(c)
  return "".join(rtn)  
```

AlphaNumberic
```python
isalnum()
```

Get charactor index
```python
print(ord('A')) # 65
print(ord('B')-ord('A')+1) # 2
print(chr(ord('a') + 2)) # c
```

Replace characters or strings
```python
def isValid(self, s: str) -> bool:
  while '[]' in s or '()' in s or '{}' in s:
    s = s.replace('[]','').replace('()','').replace('{}','')
  return len(s) == 0
```

Insert values in strings
```python
txt3 = "My name is {}, I'm {}".format("John",36) # My name is John, I'm 36
```

Multiply strings/lists with *, even booleans which map to True(1) and False(0)
```python
'meh' * 2 # mehmeh
['meh'] * 2 # ['meh', 'meh']
['meh'] * True #['meh']
['meh'] * False #[]
```

Find substring in string
```python
txt = "Hello, welcome to my world."
x = txt.find("welcome")  # 7
```

startswith and endswith are very handy
```python
str = "this is string example....wow!!!"
str.endswith("!!") # True
str.startswith("this") # True
str.endswith("is", 2, 4) # True
```

Python3 format strings
```python
name = "Eric"
profession = "comedian"
affiliation = "Monty Python"
message = (
     f"Hi {name}. "
     f"You are a {profession}. "
     f"You were in {affiliation}."
)
message
'Hi Eric. You are a comedian. You were in Monty Python.'
```

Print string with all chars, useful for debugging
```python
print(repr("meh\n"))     # 'meh\n'
```

## Slicing

Slicing [intro](https://stackoverflow.com/questions/509211/understanding-slice-notation)

```python
                +---+---+---+---+---+---+
                | P | y | t | h | o | n |
                +---+---+---+---+---+---+
Slice position: 0   1   2   3   4   5   6
Index position:   0   1   2   3   4   5
p = ['P','y','t','h','o','n']
p[0] 'P' # indexing gives items, not lists
alpha[slice(2,4)] # equivalent to p[2:4]
p[0:1] # ['P'] Slicing gives lists
p[0:5] # ['P','y','t','h','o'] Start at beginning and count 5
p[2:4] = ['t','r'] # Slice assignment  ['P','y','t','r','o','n']
p[2:4] = ['s','p','a','m'] # Slice assignment can be any size['P','y','s','p','a','m','o','n']
p[4:4] = ['x','y'] # insert slice ['P','y','t','h','x','y','o','n'] 
p[0:5:2] # ['P', 't', 'o'] sliceable[start:stop:step]
p[5:0:-1] # ['n', 'o', 'h', 't', 'y']
```

Go through num and get combinations missing a member

```python
numList = [1,2,3,4]
for i in range(len(numList)): 
    newList = numList[0:i] + numList[i+1:len(numList)]
    print(newList) # [2, 3, 4], [1, 3, 4], [1, 2, 4], [1, 2, 3]
```

## Tuple

Collection that is ordered and unchangable

```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[1]) # banana
```

Can be used with Dicts

```python
def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
    d = defaultdict(list)
    for w in strs:
        key = tuple(sorted(w))
        d[key].append(w)
    return d.values()
```

## Sort

sorted(iterable, key=key, reverse=reverse)

Sort sorts alphabectically, from smallest to largest

```python
print(sorted(['Ford', 'BMW', 'Volvo'])) # ['BMW', 'Ford', 'Volvo']
nums = [-4,-1,0,3,10]
print(sorted(n*n for n in nums)) # [0,1,9,16,100]
```

```python
cars = ['Ford', 'BMW', 'Volvo']
cars.sort() # returns None type
cars.sort(key=lambda x: len(x) ) # ['BMW', 'Ford', 'Volvo']
print(sorted(cars, key=lambda x:len(x))) # ['BMW', 'Ford', 'Volvo']
```

Sort key by value, even when value is a list
```python
meh = {'a':3,'b':0,'c':2,'d':-1}
print(sorted(meh, key=lambda x:meh[x])) # ['d', 'b', 'c', 'a']
meh = {'a':[0,3,'a'],'b':[-2,-3,'b'],'c':[2,3,'c'],'d':[-2,-2,'d']}
print(sorted(meh, key=lambda x:meh[x])) # ['b', 'd', 'a', 'c']
```

```python
def merge_sorted_lists(arr1, arr2): # built in sorted does Timsort optimized for subsection sorted lists
    return sorted(arr1 + arr2)
```

Sort an array but keep the original indexes
```python
self.idx, self.vals = zip(*sorted([(i,v) for i,v in enumerate(nums)], key=lambda x:x[1]))
```

Sort by tuple, 2nd element then 1st ascending
```python
a = [(5,10), (2,20), (2,3), (0,100)]
test = sorted(a, key = lambda x: (x[1],x[0])) 
print(test) # [(2, 3), (5, 10), (2, 20), (0, 100)]
test = sorted(a, key = lambda x: (-x[1],x[0])) 
print(test) # [(0, 100), (2, 20), (5, 10), (2, 3)]
```

Sort and print dict values by key
```python
ans = {-1: [(10, 1), (3, 3)], 0: [(0, 0), (2, 2), (7, 4)], -3: [(8, 5)]}
for key, value in sorted(ans.items()): print(value)
# [(8, 5)]
# [(10, 1), (3, 3)]
# [(0, 0), (2, 2), (7, 4)]

# sorted transforms dicts to lists
sorted(ans) # [-3, -1, 0]
sorted(ans.values()) # [[(0, 0), (2, 2), (7, 4)], [(8, 5)], [(10, 1), (3, 3)]]
sorted(ans.items()) # [(-3, [(8, 5)]), (-1, [(10, 1), (3, 3)]), (0, [(0, 0), (2, 2), (7, 4)])]
# Or just sort the dict directly
[ans[i] for i in sorted(ans)]
# [[(8, 5)], [(10, 1), (3, 3)], [(0, 0), (2, 2), (7, 4)]]
```

## Hash

```python
for c in s1: # Adds counter for c
  ht[c] = ht.get(c, 0) + 1 # ht[a] = 1, ht[a]=2, etc
```

## Set

```python
a = 3
st = set()
st.add(a) # Add to st
st.remove(a) # Remove from st
st.discard(a) # Removes from set with no error
st.add(a) # Add to st
next(iter(s)) # return 3 without removal
st.pop() # returns 3
```

```python
s = set('abc') # {'c', 'a', 'b'}
s |= set('cdf') # {'f', 'a', 'b', 'd', 'c'} set s with elements from new set
s &= set('bd') # {'d', 'b'} only elements from new set
s -= set('b') # {'d'} remove elements from new set
s ^= set('abd') # {'a', 'b'} elements from s or new but not both
```

## List

Stacks are implemented with Lists. Stacks are good for parsing and graph traversal

```python
test = [0] * 100 # initialize list with 100 0's
```

2D
```python
rtn.append([])
rtn[0].append(1) # [[1]]               
```

List Comprehension
```python
number_list = [ x for x in range(20) if x % 2 == 0]
print(number_list) # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

Reverse a list
```python
ss = [1,2,3]
ss.reverse()
print(ss) #3,2,1
```

Join list
```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]
list3 = list1 + list2 # ['a', 'b', 'c', 1, 2, 3]
```

## Dict

Hashtables are implemented with dictionaries

```python
d = {'key': 'value'}         # Declare dict{'key': 'value'}
d['key'] = 'value'           # Add Key and Value
{x:0 for x in {'a', 'b'}}    # {'a': 0, 'b': 0} declare through comprehension 
d['key'])                    # Access value
d.items()                    # Items as tuple list dict_items([('key', 'value')])
if 'key' in d: print("meh")  # Check if value exists
par = {}
par.setdefault(1,1)          # returns 1, makes par = { 1 : 1 }
par = {0:True, 1:False}
par.pop(0)                   # Remove key 0, Returns True, par now {1: False}
for k in d: print(k)         # Iterate through keys
```

Create Dict of Lists that match length of list to count votes
```python
votes = ["ABC","CBD","BCA"]
rnk = {v:[0] * len(votes[0]) for v in votes[0]} 
print(rnk) # {'A': [0, 0, 0], 'B': [0, 0, 0], 'C': [0, 0, 0]}
```
## Tree

1. A [tree](https://www.geeksforgeeks.org/some-theorems-on-trees/) is an undirected [graph](https://www.cs.sfu.ca/~ggbaker/zju/math/trees.html) in which any two vertices are
connected by exactly one path.
1. Any connected graph who has n nodes with n-1 edges is a tree.
1. The degree of a vertex is the number of edges connected to the vertex.
1. A leaf is a vertex of degree 1. An internal vertex is a vertex of degree at least 2.
1. A [path graph](https://en.wikipedia.org/wiki/Path_graph) is a tree with two or more vertices with no branches, degree of 2 except for leaves which have degree of 1

1. Any two vertices in G can be connected by a unique simple path.
1. G is acyclic, and a simple cycle is formed if any edge is added to G.
1. G is connected and has no cycles.
1. G is connected but would become disconnected if any single edge is removed from G.


## BinaryTree


DFS Pre, In Order, and Post order Traversal

- Preorder
  - encounters roots before leaves
  - Create copy
- Inorder
  - flatten tree back to original sequence
  - Get values in non-decreasing order in BST
- Post order
  - encounter leaves before roots
  - Helpful for deleting

Recursive
```python
"""
     1
    / \
   2   3
  / \
 4   5
"""
# PostOrder 4 5 2 3 1  (Left-Right-Root)
def postOrder(node):
  if node is None:
    return
  postorder(node.left)
  postorder(node.right)
  print(node.value, end=' ')
```

Iterative PreOrder
```python
# PreOrder  1 2 4 5 3 (Root-Left-Right)
def preOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node.right, False))
        stack.append((node.left, False))
        stack.append((node, True))
```

Iterative InOrder
```python
# InOrder   4 2 5 1 3 (Left-Root-Right)
def inOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node.right, False))
        stack.append((node, True))
        stack.append((node.left, False))
```

Iterative PostOrder
```python
# PostOrder 4 5 2 3 1  (Left-Right-Root)
def postOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node, True))
        stack.append((node.right, False))
        stack.append((node.left, False))
```

Iterative BFS(LevelOrder)
```python
from collections import deque

#BFS levelOrder 1 2 3 4 5 
def levelOrder(tree_root):
  queue = deque([tree_root])
  while queue:
    node = queue.popleft()
    if node:
        print(node.value, end=' ')
        queue.append(node.left)
        queue.append(node.right)

def levelOrderStack(tree_root):
    stk = [(tree_root, 0)]
    rtn = []
    while stk:
        node, depth = stk.pop()
        if node:
            if len(rtn) < depth + 1:
                rtn.append([])
            rtn[depth].append(node.value)            
            stk.append((node.right, depth+1))
            stk.append((node.left, depth+1))
    print(rtn)
    return True     

def levelOrderStackRec(tree_root):
    rtn = []
        
    def helper(node, depth):
        if len(rtn) == depth:
            rtn.append([])
        rtn[depth].append(node.value)
        if node.left:
            helper(node.left, depth + 1)
        if node.right:
            helper(node.right, depth + 1)
            
    helper(tree_root, 0)
    print(rtn)
    return rtn
```

Traversing data types as a graph, for example BFS
```python
def removeInvalidParentheses(self, s: str) -> List[str]:
    rtn = []
    v = set()
    v.add(s)
    if len(s) == 0: return [""]
    while True:
        for n in v:
            if self.isValid(n):
                rtn.append(n)
        if len(rtn) > 0: break
        level = set()
        for n in v:
            for i, c in enumerate(n):
                if c == '(' or c == ')':
                    sub = n[0:i] + n[i + 1:len(n)]
                    level.add(sub)
        v = level
    return rtn
```

Reconstructing binary trees
1. Binary tree could be constructed from preorder and inorder traversal
1. Inorder traversal of BST is an array sorted in the ascending order

Convert tree to array and then to balanced tree
```python
def balanceBST(self, root: TreeNode) -> TreeNode:
    self.inorder = []
    
    def getOrder(node):
        if node is None:
            return
        getOrder(node.left)
        self.inorder.append(node.val)
        getOrder(node.right)

    # Get inorder treenode ["1,2,3,4"]
    getOrder(root)
    
    # Convert to Tree
    #        2
    #       1 3
    #          4
    def bst(listTree):
        if not listTree:
            return None
        mid = len(listTree) // 2
        root = TreeNode(listTree[mid])
        root.left = bst(listTree[:mid])
        root.right = bst(listTree[mid+1:])
        return root

    return bst(self.inorder)
```

## Graph

Build an [adjecency graph](https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/representing-graphs) from edges list
```python
# N = 6, edges = [[0,1],[0,2],[2,3],[2,4],[2,5]]
graph = [[] for _ in range(N)]
for u,v in edges:
    graph[u].append(v)
    graph[v].append(u)
# [[1, 2], [0], [0, 3, 4, 5], [2], [2], [2]]
```

Build adjecency graph from traditional tree
```python
adj = collections.defaultdict(list)
def dfs(node):
    if node.left:
        adj[node].append(node.left)
        adj[node.left].append(node)
        dfs(node.left)
    if node.right:
        adj[node].append(node.right)
        adj[node.right].append(node)
        dfs(node.right)
dfs(root)
```

Traverse Tree in graph notation
```python
# [[1, 2], [0], [0, 3, 4, 5], [2], [2], [2]]
def dfs(node, par=-1):
    for nei in graph[node]:
        if nei != par:
            res = dfs(nei, node)
dfs(0) # 1->2->3->4->5
```

## Heapq
```
      1
     / \
    2   3
   / \ / \
  5  6 8  7
```

[Priority Queue](https://realpython.com/python-heapq-module/#data-structures-heaps-and-priority-queues) 
1. Implemented as complete binary tree, which has all levels as full excepted deepest
1. In a heap tree the node is smaller than its children

```python
def maximumProduct(self, nums: List[int]) -> int:
  l = heapq.nlargest(3, nums)
  s = heapq.nsmallest(3, nums)
  return max(l[0]*l[1]*l[2],s[0]*s[1]*l[0])
```

Heap elements can be tuples, heappop() frees the smallest element (flip sign to pop largest)
```python
def kClosest(self, points: List[List[int]], K: int) -> List[List[int]]:
    heap = []
    for p in points:
        distance = sqrt(p[0]* p[0] + p[1]*p[1])
        heapq.heappush(heap,(-distance, p))
        if len(heap) > K:
            heapq.heappop(heap)            
    return ([h[1] for h in heap])
```

nsmallest can take a lambda argument
```python
def kClosest(self, points: List[List[int]], K: int) -> List[List[int]]:    
    return heapq.nsmallest(K, points, lambda x: x[0]*x[0] + x[1]*x[1])
```

The key can be a function as well in nsmallest/nlargest
```python
def topKFrequent(self, nums: List[int], k: int) -> List[int]:
    count = Counter(nums)
    return heapq.nlargest(k, count, count.get)
```

Tuple sort, 1st/2nd element. increasing frequency then decreasing order
```python
def topKFrequent(self, words: List[str], k: int) -> List[str]:
    freq = Counter(words)
    return heapq.nsmallest(k, freq.keys(), lambda x:(-freq[x], x))
```

## Lambda

Can be used with (list).sort(), sorted(), min(), max(), (heapq).nlargest,nsmallest(), map()

```python
# a=3,b=8,target=10
min((b,a), key=lambda x: abs(target - x)) # 8
```

```python
>>> ids = ['id1', 'id2', 'id30', 'id3', 'id22', 'id100']
>>> print(sorted(ids)) # Lexicographic sort
['id1', 'id100', 'id2', 'id22', 'id3', 'id30']
>>> sorted_ids = sorted(ids, key=lambda x: int(x[2:])) # Integer sort
>>> print(sorted_ids)
['id1', 'id2', 'id3', 'id22', 'id30', 'id100']
```

```python
trans = lambda x: list(al[i] for i in x) # apple, a->0..
print(trans(words[0])) # [0, 15, 15, 11, 4]
```

Lambda can sort by 1st, 2nd element in tuple
```python
sorted([('abc', 121),('bbb',23),('abc', 148),('bbb', 24)], key=lambda x: (x[0],x[1]))
# [('abc', 121), ('abc', 148), ('bbb', 23), ('bbb', 24)]
```

## Zip

Combine two dicts or lists
```python
s1 = {2, 3, 1}
s2 = {'b', 'a', 'c'}
list(zip(s1, s2)) # [(1, 'a'), (2, 'c'), (3, 'b')]
```

Traverse in Parallel
```python
letters = ['a', 'b', 'c']
numbers = [0, 1, 2]
for l, n in zip(letters, numbers):
  print(f'Letter: {l}') # a,b,c
  print(f'Number: {n}') # 0,1,2
```

Empty in one list is ignored
```python
letters = ['a', 'b', 'c']
numbers = []
for l, n in zip(letters, numbers):
  print(f'Letter: {l}') #
  print(f'Number: {n}') #
```

Compare characters of alternating words
```python
for a, b in zip(words, words[1:]):
    for c1, c2 in zip(a,b):
        print("c1 ", c1, end=" ")
        print("c2 ", c2, end=" ") 
```

Passing in [*](https://stackoverflow.com/questions/29139350/difference-between-ziplist-and-ziplist/29139418) unpacks a list or other iterable, making each of its elements a separate argument. 

```python
a = [[1,2],[3,4]]
test = zip(*a)
print(test) # (1, 3) (2, 4)
matrix = [[1,2,3],[4,5,6],[7,8,9]]
test = zip(*matrix)
print(*test) # (1, 4, 7) (2, 5, 8) (3, 6, 9)
```

Useful when rotating a matrix
```python
# matrix = [[1,2,3],[4,5,6],[7,8,9]]
matrix[:] = zip(*matrix[::-1]) # [[7,4,1],[8,5,2],[9,6,3]]
```

Iterate through chars in a list of strs
```python
strs = ["cir","car","caa"]
for i, l in enumerate(zip(*strs)):
    print(l)  
    # ('c', 'c', 'c')
    # ('i', 'a', 'a')
    # ('r', 'r', 'a')
```

Diagonals can be traversed with the help of a list

```python
"""
[[1,2,3],
 [4,5,6],
 [7,8,9],
 [10,11,12]]
"""
def printDiagonalMatrix(self, matrix: List[List[int]]) -> bool:
    R = len(matrix)
    C = len(matrix[0])
    
    tmp = [[] for _ in range(R+C-1)]
    
    for r in range(R):
        for c in range(C):
            tmp[r+c].append(matrix[r][c])
    
    for t in tmp:
        for n in t:
            print(n, end=' ')            
        print("")
"""
 1,
 2,4
 3,5,7
 6,8,10
 9,11
 12
"""
```

## Random

```Python
for i, l in enumerate(shuffle):
  r = random.randrange(0+i, len(shuffle))
  shuffle[i], shuffle[r] = shuffle[r], shuffle[i]
return shuffle
```

Other random generators
```Python
import random
ints = [0,1,2]
random.choice(ints) # 0,1,2
random.choices([1,2,3],[1,1,10]) # 3, heavily weighted
random.randint(0,2) # 0,1, 2
random.randint(0,0) # 0
random.randrange(0,0) # error
random.randrange(0,2) # 0,1
```

## Constants

```Python
max = float('-inf')
min = float('inf')
```

## Ternary

a if condition else b
```Python
test = stk.pop() if stk else '#'
```

## Bitwise Operators
```python
'0b{:04b}'.format(0b1100 & 0b1010) # '0b1000' and
'0b{:04b}'.format(0b1100 | 0b1010) # '0b1110' or 
'0b{:04b}'.format(0b1100 ^ 0b1010) # '0b0110' exclusive or
'0b{:04b}'.format(0b1100 >> 2)     # '0b0011' shift right
'0b{:04b}'.format(0b0011 << 2)     # '0b1100' shift left
```

## For Else

Else condition on for loops if break is not called

```python
for w1, w2 in zip(words, words[1:]): #abc, ab
    for c1, c2 in zip(w1, w2):
        if c1 != c2:
            adj[c1].append(c2)
            degrees[c2] += 1
            break
    else: # nobreak
        if len(w1) > len(w2):
            return ""   # Triggers since ab should be before abc, not after
```

## Modulo

```python
for n in range(-8,8):
    print n, n//4, n%4
    
 -8 -2 0
 -7 -2 1
 -6 -2 2
 -5 -2 3

 -4 -1 0
 -3 -1 1
 -2 -1 2
 -1 -1 3

  0  0 0
  1  0 1
  2  0 2
  3  0 3

  4  1 0
  5  1 1
  6  1 2
  7  1 3
```

## Any

if any element of the iterable is True
```python
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

## All
```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

## Bisect

* bisect.bisect_left returns the leftmost place in the sorted list to insert the given element
* bisect.bisect_right returns the rightmost place in the sorted list to insert the given element

```python
import bisect
bisect.bisect_left([1,2,3,4,5], 2)  # 1
bisect.bisect_right([1,2,3,4,5], 2) # 2
bisect.bisect_left([1,2,3,4,5], 7)  # 5
bisect.bisect_right([1,2,3,4,5], 7) # 5
```

Insert x in a in sorted order. This is equivalent to a.insert(bisect.bisect_left(a, x, lo, hi), x) assuming that a is already sorted. Search is binary search O(logn) and insert is O(n)

```python
import bisect
l = [1, 3, 7, 5, 6, 4, 9, 8, 2]
result = []
for e in l:
    bisect.insort(result, e)
print(result) # [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

```python
li1 = [1, 3, 4, 4, 4, 6, 7] # [1, 3, 4, 4, 4, 5, 6, 7]
bisect.insort(li1, 5) # 
```

Bisect can give two ends of a range, if the array is sorted of course
```python
s = bisect.bisect_left(nums, target)
e = bisect.bisect(nums, target) -1
if s <= e:
    return [s,e]
else:
    return [-1,-1]
```

## Math

Calulate power

```python
# (a ^ b) % p. 
d = pow(a, b, p) 
```

Division with remainder
```python
divmod(8, 3) # (2, 2)
divmod(3, 8) #  (0, 3)
```

## eval

Evaluates an expression
```python
x = 1
print(eval('x + 1'))
```

## Iter

Creates iterator from container object such as list, tuple, dictionary and set

```python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)
print(next(myit)) # apple
print(next(myit)) # banana
```

## Map

map(func, *iterables)

```python
my_pets = ['alfred', 'tabitha', 'william', 'arla']
uppered_pets = list(map(str.upper, my_pets)) # ['ALFRED', 'TABITHA', 'WILLIAM', 'ARLA']
my_strings = ['a', 'b', 'c', 'd', 'e']
my_numbers = [1,2,3,4,5]
results = list(map(lambda x, y: (x, y), my_strings, my_numbers)) # [('a', 1), ('b', 2), ('c', 3), ('d', 4), ('e', 5)]
```

```python
A1 = [1, 4, 9]
''.join(map(str, A1))
```

## Filter

filter(func, iterable)

```python
scores = [66, 90, 68, 59, 76, 60, 88, 74, 81, 65]
over_75 = list(filter(lambda x: x>75, scores)) # [90, 76, 88, 81]
```

```python
scores = [66, 90, 68, 59, 76, 60, 88, 74, 81, 65]
def is_A_student(score):
    return score > 75
over_75 = list(filter(is_A_student, scores)) # [90, 76, 88, 81]
```

```python
dromes = ("demigod", "rewire", "madam", "freer", "anutforajaroftuna", "kiosk")
palindromes = list(filter(lambda word: word == word[::-1], dromes)) # ['madam', 'anutforajaroftuna']
```

Get degrees == 0 from list
```python
stk = list(filter(lambda x: degree[x]==0, degree.keys()))
```

## Reduce

reduce(func, iterable[, initial]) 
where initial is optional

```python
numbers = [3, 4, 6, 9, 34, 12]
result = reduce(lambda x, y: x+y, numbers) # 68
result = reduce(lambda x, y: x+y, numbers, 10) #78
```

## itertools

[itertools.accumulate(iterable[, func]) –> accumulate object](https://www.geeksforgeeks.org/python-itertools-accumulate/)

```python
import itertools
data = [3, 4, 6, 2, 1, 9, 0, 7, 5, 8]
list(itertools.accumulate(data)) # [3, 7, 13, 15, 16, 25, 25, 32, 37, 45]
list(accumulate(data, max))  # [3, 4, 6, 6, 6, 9, 9, 9, 9, 9]
cashflows = [1000, -90, -90, -90, -90]  # Amortize a 5% loan of 1000 with 4 annual payments of 90
list(itertools.accumulate(cashflows, lambda bal, pmt: bal*1.05 + pmt)) [1000, 960.0, 918.0, 873.9000000000001, 827.5950000000001]
for k,v in groupby("aabbbc")    # group by common letter
    print(k)                    # a,b,c
    print(list(v))              # [a,a],[b,b,b],[c,c]
```

## Regular Expression

RE module allows regular expressions in python

```python
def removeVowels(self, S: str) -> str:
    return re.sub('a|e|i|o|u', '', S)
```

## Types

from typing import List, Set, Dict, Tuple, Optional
[cheat sheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

## Grids

Useful helpful function
```python
R = len(grid)
C = len(grid[0])

def neighbors(r, c):
    for nr, nc in ((r,c-1), (r,c+1), (r-1, c), (r+1,c)):
        if 0<=nr<R and 0<=nc<C:
            yield nr, nc

def dfs(r,c, index):
    area = 0
    grid[r][c] = index
    for x,y in neighbors(r,c):
        if grid[x][y] == 1:
            area += dfs(x,y, index)
    return area + 1
```

# Collections

Stack with appendleft() and popleft()

## Deque

```python
from collections import deque
deq = deque([1, 2, 3])
deq.appendleft(5)
deq.append(6)
deq
deque([5, 1, 2, 3, 6])
deq.popleft()
5
deq.pop()
6
deq
deque([1, 2, 3])
```

## Counter

```python
from collections import Counter
count = Counter("hello") # Counter({'h': 1, 'e': 1, 'l': 2, 'o': 1})
count['l'] # 2
count['l'] += 1
count['l'] # 3
```

Get counter k most common in list of tuples
```python
# [1,1,1,2,2,3]
# Counter  [(1, 3), (2, 2)]
def topKFrequent(self, nums: List[int], k: int) -> List[int]:
    if len(nums) == k:
        return nums
    return [n[0] for n in Counter(nums).most_common(k)] # [1,2]
```

elements() lets you walk through each number in the Counter
```python
def intersect(self, nums1: List[int], nums2: List[int]) -> List[int]:
    c1 = collections.Counter(nums1) # [1,2,2,1]
    c2 = collections.Counter(nums2) # [2,2]
    dif = c1 & c2                   # {2:2}
    return list(dif.elements())     # [2,2]
```

operators work on Counter
```python
c = Counter(a=3, b=1)
d = Counter(a=1, b=2)
c + d # {'a': 4, 'b': 3}
c - d # {'a': 2}
c & d # {'a': 1, 'b': 1}
c | d # {'a': 3, 'b': 2}
c = Counter(a=2, b=-4)
+c # {'a': 2}
-c # {'b': 4}
```

## Default Dict

```python
d={}
print(d['Grapes'])# This gives Key Error
from collections import defaultdict
d = defaultdict(int) # set default
print(d['Grapes']) # 0, no key error
d = collections.defaultdict(lambda: 1)
print(d['Grapes']) # 1, no key error
```

```python
from collections import defaultdict
dd = defaultdict(list)
dd['key'].append(1) # defaultdict(<class 'list'>, {'key': [1]})
dd['key'].append(2) # defaultdict(<class 'list'>, {'key': [1, 2]})
```

# Algorithms

## General Tips

* Get all info
* Debug example, is it a special case?
* Brute Force
  * Get to brute-force solution as soon as possible. State runtime and then optimize, don't code yet
* Optimize
  * Look for unused info
  * Solve it manually on example, then reverse engineer thought process
  * Space vs time, hashing
  * BUDS (Bottlenecks, Unnecessary work, Duplication)
* Walk through approach
* Code
* Test
  * Start small
  * Hit edge cases

## Binary Search

```python
def firstBadVersion(self, n):
    l, r = 0, n
    while l < r:
        m = l + (r-l) // 2
        if isBadVersion(m):
            r = m
        else:
            l = m + 1
    return l
```

```python
"""
12345678 
FFTTTTTT
"""
def mySqrt(self, x: int) -> int:
  def condition(value, x) -> bool:
    return value * value > x

  if x == 1:
    return 1

  left, right = 1, x
  while left < right:
    mid = left + (right-left) // 2
    if condition(mid, x):
      right = mid
    else:
      left = mid + 1

  return left - 1
```
[binary search](https://leetcode.com/discuss/general-discussion/786126/python-powerful-ultimate-binary-search-template-solved-many-problems)

## Binary Search Tree

Use values to detect if number is missing
```python
def isCompleteTree(self, root: TreeNode) -> bool:
    self.total = 0
    self.mx = float('-inf')
    def dfs(node, cnt):
        if node:
            self.total += 1
            self.mx = max(self.mx, cnt)
            dfs(node.left, (cnt*2))
            dfs(node.right, (cnt*2)+1)
    dfs(root, 1)
    return self.total == self.mx
```

Get a range sum of values
```python
def rangeSumBST(self, root: TreeNode, L: int, R: int) -> int:
    self.total = 0
    def helper(node):
        if node is None:
            return 0
        if L <= node.val <= R:
            self.total += node.val
        if node.val > L:
            left = helper(node.left)  
        if node.val < R:
            right = helper(node.right)
    helper(root)
    return self.total
```

Check if valid
```python
def isValidBST(self, root: TreeNode) -> bool:
    if not root:
        return True
    stk = [(root, float(-inf), float(inf))]
    while stk:
        node, floor, ceil = stk.pop()
        if node:
            if node.val >= ceil or node.val <= floor:
                return False
            stk.append((node.right, node.val, ceil))
            stk.append((node.left, floor, node.val))
    return True
```

## Topological Sort

[Kahn's algorithm](https://www.geeksforgeeks.org/all-topological-sorts-of-a-directed-acyclic-graph/), detects cycles through degrees and needs all the nodes represented to work 

1. Initialize vertices as unvisited
1. Pick vertex with zero indegree, append to result, decrease indegree of neighbors 
1. Now repeat for neighbors, resulting list is sorted by source -> dest

If cycle, then degree of nodes in cycle will not be 0 since there
is no origin

```python
def canFinish(self, numCourses: int, prerequisites: List[List[int]]) -> bool:
    # Kahns algorithm, topological sort
    adj = collections.defaultdict(list)
    degree = collections.Counter()
    
    for dest, orig in prerequisites:
        adj[orig].append(dest)
        degree[dest] += 1
    
    bfs = [c for c in range(numCourses) if degree[c] == 0]
    
    for o in bfs:
        for d in adj[o]:
            degree[d] -= 1
            if degree[d] == 0:
                bfs.append(d)

    return len(bfs) == numCourses
```

```python
def alienOrder(self, words: List[str]) -> str:
    nodes = set("".join(words))
    adj = collections.defaultdict(list)
    degree = collections.Counter(nodes)
    
    for w1, w2 in zip(words, words[1:]):
        for c1, c2 in zip(w1, w2):
            if c1 != c2:
                adj[c1].append(c2)
                degree[c2] += 1
                break
        else:
            if len(w1) > len(w2):
                return ""
    
    stk = list(filter(lambda x: degree[x]==1, degree.keys()))
    
    ans = []
    while stk:
        node = stk.pop()
        ans.append(node)
        for nei in adj[node]:
            degree[nei] -= 1
            if degree[nei] == 1:
                stk.append(nei)
    
    return "".join(ans) * (set(ans) == nodes)
```

## Sliding Window

1. Have a counter or hash-map to count specific array input and keep on increasing the window toward right using outer loop.
1. Have a while loop inside to reduce the window side by sliding toward right. Movement will be based on constraints of problem.
1. Store the current maximum window size or minimum window size or number of windows based on problem requirement.

### Typical Problem Clues:
1. Get min/max/number of satisfied sub arrays
1. Return length of the subarray with max sum/product
1. Return max/min length/number of subarrays whose sum/product equals K

Can require [2 or 3 pointers to solve](https://medium.com/algorithms-and-leetcode/magic-solution-to-leetcode-problems-sliding-window-algorithm-891e3d60bf89)

```python
    def slidingWindowTemplate(self, s: str):
        #init a collection or int value to save the result according the question.
        rtn = []
        
        # create a hashmap to save the Characters of the target substring.
        # (K, V) = (Character, Frequence of the Characters)
        hm = {}

        # maintain a counter to check whether match the target string as needed
        cnt = collections.Counter(s)

        # Two Pointers: begin - left pointer of the window; end - right pointer of the window if needed
        l = r = 0

        # loop at the begining of the source string
        for r, c in enumerate(s): 
            
            if c in hm:
                l = max(hm[c]+1, l) # +/- 1 or set l to index, max = never move l left 

            # update hm
            hm[c] = r

            # increase l pointer to make it invalid/valid again
            while cnt == 0: # counter condition
                cnt[c] += 1  # modify counter if needed
    
            # Save result / update min/max after loop is valid
            rtn = max(rtn, r-l+1)

        return rtn
```

```python
def fruits_into_baskets(fruits):
  maxCount, j = 0, 0
  ht = {}

  for i, c in enumerate(fruits):
    if c in ht:
      ht[c] += 1
    else:
      ht[c] = 1

    if len(ht) <= 2:
      maxCount = max(maxCount, i-j+1)
    else:
      jc = fruits[j]
      ht[jc] -= 1
      if ht[jc] <= 0:
        del ht[jc]
      j += 1  

  return maxCount
```

## Greedy

Make the optimal [choice](https://brilliant.org/wiki/greedy-algorithm/) at each step. 

[Increasing Triplet Subsequence](https://leetcode.com/problems/increasing-triplet-subsequence/), true if i < j < k
```python
def increasingTriplet(self, nums: List[int]) -> bool:
    l = m = float('inf')
    
    for n in nums:
        if n <= l:
            l = n
        elif n <= m:
            m = n
        else:
            return True
    
    return False
```

## Tree Tricks

Bottom up solution with arguments for min, max

```python
def maxAncestorDiff(self, root: TreeNode) -> int:
    if not root:
        return 0
    self.ans = 0
    def dfs(node, minval, maxval):
        if not node:
            self.ans = max(self.ans, abs(maxval - minval))
            return
        dfs(node.left, min(node.val, minval), max(node.val, maxval))
        dfs(node.right, min(node.val, minval), max(node.val, maxval))
    dfs(root, float('inf'), float('-inf'))
    return self.ans
```

Building a path through a tree 
```python
def binaryTreePaths(self, root: TreeNode) -> List[str]:
    rtn = []
    if root is None: return []
    stk = [(root, str(root.val))]
    while stk:
        node, path = stk.pop()
        if node.left is None and node.right is None:
            rtn.append(path)
        if node.left:
            stk.append((node.left, path + "->" + str(node.left.val)))
        if node.right:
            stk.append((node.right, path + "->" + str(node.right.val)))
    return rtn
```

Using return value to sum
```python
def diameterOfBinaryTree(self, root: TreeNode) -> int:
    self.mx = 0
    def dfs(node):
        if node:
            l = dfs(node.left)
            r = dfs(node.right)
            total = l + r
            self.mx = max(self.mx, total) 
            return max(l, r) + 1
        else:
            return 0
    dfs(root)
    return self.mx
```

Change Tree to Graph
```python
def distanceK(self, root: TreeNode, target: TreeNode, K: int) -> List[int]:
    adj = collections.defaultdict(list)
    
    def dfsa(node):
        if node.left:
            adj[node].append(node.left)
            adj[node.left].append(node)
            dfsa(node.left)
        if node.right:
            adj[node].append(node.right)
            adj[node.right].append(node)
            dfsa(node.right)
            
    dfsa(root)
    
    def dfs(node, prev, d):
        if node:
            if d == K:
                rtn.append(node.val)
            else:
                for nei in adj[node]:
                    if nei != prev:
                        dfs(nei, node, d+1)
                
    rtn = []
    dfs(target, None, 0)
    return rtn
```

## Anagrams

Subsection of sliding window, solve with Counter Dict

i.e.
abc   =   bca   !=  eba
111       111       111

```python
def isAnagram(self, s: str, t: str) -> bool:
    sc = collections.Counter(s)
    st = collections.Counter(t)
    if sc != st:
        return False
    return True
```

Sliding Window version (substring)

```python
def findAnagrams(self, s: str, p: str) -> List[int]:
    cntP = collections.Counter(p)
    cntS = collections.Counter()
    P = len(p)
    S = len(s)
    if P > S:
        return []
    ans = []
    for i, c in enumerate(s):
        cntS[c] += 1
        if i >= P:
            if cntS[s[i-P]] > 1:
                cntS[s[i-P]] -= 1
            else:
                del cntS[s[i-P]]
        if cntS == cntP:
            ans.append(i-(P-1))
    return ans
```



## Dynamic Programming

1. [dynamic programming](https://leetcode.com/discuss/general-discussion/458695/Dynamic-Programming-Patterns)

```python
def coinChange(self, coins: List[int], amount: int) -> int:
  MAX = float('inf')
  dp =  [MAX] * (amount + 1)
  dp[0] = 0
  for c in coins:
    for a in range(c, amount+1):    
      dp[a] =  min(dp[a], dp[a-c]+1)      
  return dp[amount] if dp[amount] != MAX else -1
```

Classic DP grid, longest common subsequence
```python
def longestCommonSubsequence(self, text1: str, text2: str) -> int:
    Y = len(text2)+1
    X = len(text1)+1
    dp = [[0] * Y for _ in range(X)]
    # [[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0]]
    for i, c in enumerate(text1):
        for j, d in enumerate(text2):
            if c == d:
                dp[i + 1][j + 1] = 1 + dp[i][j]  
            else:
                dp[i + 1][j + 1] = max(dp[i][j + 1], dp[i + 1][j])
    return dp[-1][-1]
# [[0,0,0,0],[0,1,1,1],[0,1,1,1],[0,1,2,2],[0,1,2,2],[0,1,2,3]]
# abcde
# "ace"
```



## Cyclic Sort

1. Useful algo when sorting in place

```python
# if my number is equal to my index, i+1 
# if my number is equal to this other number, i+1 (dups)
# else swap
def cyclic_sort(nums):
  i = 0
  while i < len(nums):
    j = nums[i] - 1
    if nums[i] != nums[j]:
      nums[i], nums[j] = nums[j], nums[i]  
    else:
      i += 1
  return nums
```

## Quick Sort

1. Can be modified for divide in conquer problems

```python
def quickSort(array):
	def sort(arr, l, r):
		if l < r:
			p = part(arr, l, r)
			sort(arr, l, p-1)
			sort(arr, p+1, r)

	def part(arr, l, r):
		pivot = arr[r]
		a = l
		for i in range(l,r):
			if arr[i] < pivot:
				arr[i], arr[a] = arr[a], arr[i]
				a += 1
		arr[r], arr[a] = arr[a], arr[r]
		return a

	sort(array, 0, len(array)-1)
	return array
```

## Merge Sort

```python
from collections import deque 
def mergeSort(array):
    def sortArray(nums):
        if len(nums) > 1:
            mid = len(nums)//2
            l1 = sortArray(nums[:mid])
            l2 = sortArray(nums[mid:])
            nums = sort(l1,l2)
        return nums
    
    def sort(l1,l2):
        result = []
        l1 = deque(l1)
        l2 = deque(l2)
        while l1 and l2:
            if l1[0] <= l2[0]:
                result.append(l1.popleft())
            else:
                result.append(l2.popleft())
        result.extend(l1 or l2)
        return result
	return sortArray(array)
```

## Merge Arrays

Merge K sorted Arrays with a heap
```python
def mergeSortedArrays(self, arrays):   
    return list(heapq.merge(*arrays))
```

Or manually with heappush/heappop. 

```python
class Solution:
def mergeSortedArrays(self, arrays):
    pq = []
    for i, arr in enumerate(arrays):
        pq.append((arr[0], i, 0))
    heapify(pq)

    res = []
    while pq:
        num, i, j = heappop(pq)
        res.append(num)
        if j + 1 < len(arrays[i]):
            heappush(pq, (arrays[i][j + 1], i, j + 1))
    return res
```

Merging K Sorted Lists

```python
def mergeKLists(self, lists: List[ListNode]) -> ListNode:
    prehead = ListNode()
    heap = []
    for i in range(len(lists)):
        node = lists[i]
        while node:
            heapq.heappush(heap, node.val)
            node = node.next 
    node = prehead
    while len(heap) > 0:
        val = heapq.heappop(heap)
        node.next = ListNode()
        node = node.next 
        node.val = val
    return prehead.next
```


## Linked List

1. Solutions typically require 3 pointers: current, previous and next
1. Solutions are usually made simplier with a prehead or dummy head node you create and then add to. Then return dummy.next

Reverse:
```python
def reverseLinkedList(head):
    prev, node  = None, head
    while node:
        node.next, prev, node = prev, node, node.next
    return prev
```

Reversing is easier if you can modify the values of the list
```python
def reverse(head):
  node = head
  stk = []
  while node:
    if node.data % 2 == 0:
      stk.append(node)
    if node.data % 2 == 1 or node.next is None:
      while len(stk) > 1:
        stk[-1].data, stk[0].data = stk[0].data, stk[-1].data
        stk.pop(0)
        stk.pop(-1)
      stk.clear()
    node = node.next
  return head
```
Merge:
```python
def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
    dummy = ListNode(-1)
    
    prev = dummy
    
    while l1 and l2:
        if l1.val < l2.val:
            prev.next = l1
            l1 = l1.next 
        else:
            prev.next = l2
            l2 = l2.next 
        prev = prev.next 
    
    prev.next = l1 if l1 is not None else l2 
    
    return dummy.next 
```

## Convert Base

1. Typically two steps. A digit modulo step and a integer division step by the next base then reverse the result or use a deque()

Base 10 to 16, or any base by changing '16' and index
```python
def toHex(self, num: int) -> str:
  rtn = []
  index = "0123456789abcdef"
  if num == 0: return '0'
  if num < 0: num += 2 ** 32
  while num > 0:
    digit = num % 16
    rtn.append(index[digit])
    num = num // 16
  return "".join(rtn[::-1])
```

## Parenthesis

1. Count can be used if simple case, otherwise stack. [Basic Calculator](#basic-calculator) is an extension of this algo

```python
def isValid(self, s) -> bool:
  cnt = 0
  for c in s:
    if c == '(':
      cnt += 1
    elif c == ')':
      cnt -= 1
      if cnt < 0:
        return False
  return cnt == 0
```

Stack can be used if more complex 
```python
def isValid(self, s: str) -> bool:
  stk = []
  mp = {")":"(", "}":"{", "]":"["}
    for c in s:
      if c in mp.values():
        stk.append(c)
      elif c in mp.keys():
        test = stk.pop() if stk else '#'
        if mp[c] != test:
          return False
  return len(stk) == 0
```

Or must store parenthesis index for further modification

```python
def minRemoveToMakeValid(self, s: str) -> str:
  rtn = list(s)
  stk = []
  for i, c in enumerate(s):
    if c == '(':
      stk.append(i)
    elif c == ')':
      if len(stk) > 0:
        stk.pop()
      else:
        rtn[i] = ''
  while stk:
    rtn[stk.pop()] = ''
  return "".join(rtn)
```

## Max Profit Stock

Infinite Transactions, [base formula](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/discuss/75924/Most-consistent-ways-of-dealing-with-the-series-of-stock-problems)
```python
def maxProfit(self, prices: List[int]) -> int:
    t0, t1 = 0, float('-inf')
    for p in prices:
        t0old = t0
        t0 = max(t0, t1 + p)
        t1 = max(t1, t0old - p)
    return t0
```

Single Transaction, t0 (k-1) = 0
```python
def maxProfit(self, prices: List[int]) -> int:
    t0, t1 = 0, float('-inf')
    for p in prices:
        t0 = max(t0, t1 + p)
        t1 = max(t1, - p)
    return t0
```

K Transactions
```python
t0 = [0] * (k+1)
t1 = [float(-inf)] * (k+1)
for p in prices:
    for i in range(k, 0, -1):
        t0[i] = max(t0[i], t1[i] + p)
        t1[i] = max(t1[i], t0[i-1] - p)
return t0[k]
```

## Shift Array Right
Arrays can be shifted right by reversing the whole string, and then reversing 0,k-1 and k,len(str)
```python
def rotate(self, nums: List[int], k: int) -> None:
    def reverse(l, r, nums):
        while l < r:
            nums[l], nums[r] = nums[r], nums[l]
            l += 1
            r -= 1
    if len(nums) <= 1: return
    k = k % len(nums)
    reverse(0, len(nums)-1, nums)
    reverse(0, k-1, nums)
    reverse(k, len(nums)-1, nums)
```

## Continuous Subarrays with Sum k 

The total number of continuous subarrays with sum k can be found by hashing the continuous sum per value and adding the count of continuous sum - k

```python
def subarraySum(self, nums: List[int], k: int) -> int:
    mp = {0: 1} 
    rtn, total = 0, 0
    for n in nums:
        total += n
        rtn += mp.get(total - k, 0)
        mp[total] = mp.get(total, 0) + 1
    return rtn
```

## Events

Events pattern can be applied when to many interval problems such as 'Find employee free time between meetings' and 'find peak population' when individual start/ends
are irrelavent and sum start/end times are more important

```python
def employeeFreeTime(self, schedule: '[[Interval]]') -> '[Interval]':
    events = []
    for e in schedule:
        for m in e:
            events.append((m.start, 1))
            events.append((m.end, -1))
    events.sort()
    itv = []
    prev = None
    bal = 0
    for t, c in events:
        if bal == 0 and prev is not None and t != prev:
            itv.append(Interval(prev, t))
        bal += c
        prev = t
    return itv
```

## Merge Meetings

Merging a new meeting into a list

```python
def insert(self, intervals: List[List[int]], newInterval: List[int]) -> List[List[int]]:
    bisect.insort(intervals, newInterval)
    merged = [intervals[0]]
    for i in intervals:
        ms, me = merged[-1]
        s, e = i
        if me >= s:
            merged[-1] = (ms, max(me, e))
        else:
            merged.append(i)
    return merged
```

## Trie

Good for autocomplete, spell checker, IP routing (match longest prefix), predictive text, solving word games

```python
class Trie:
    def __init__(self):
        self.root = {}
    
    def addWord(self, s: str):
        tmp = self.root 
        for c in s:
            if c not in tmp:
                tmp[c] = {}
            tmp = tmp[c]
        tmp['#'] = s # Store full word at '#' to simplify
    
    def matchPrefix(self, s: str, tmp=None):
        if not tmp: tmp = self.root 
        for c in s:
            if c not in tmp:
                return []
            tmp = tmp[c]
        
        rtn = []
        
        for k in tmp:
            if k == '#':
                rtn.append(tmp[k])
            else:
                rtn += self.matchPrefix('', tmp[k])
        return rtn
            
    def hasWord(self, s: str):
        tmp = self.root 
        for c in s:
            if c in tmp:
                tmp = tmp[c]
            else:
                return False
        return True
```

Search example with . for wildcards

```python
def search(self, word: str) -> bool:
    def searchNode(word, node):
        for i,c in enumerate(word):
            if c in node:
                node = node[c]
            elif c == '.':
                return any(searchNode(word[i+1:], node[cn]) for cn in node if cn != '$' )
            else:
                return False
        return '$' in node
    return searchNode(word, self.trie)
```

## Kadane

local_maxiumum[i] = max(A[i], A[i] + local_maximum[i-1])
[Explanation](https://medium.com/@rsinghal757/kadanes-algorithm-dynamic-programming-how-and-why-does-it-work-3fd8849ed73d)
Determine max subarray sum

```python
# input: [-2,1,-3,4,-1,2,1,-5,4]
def maxSubArray(self, nums: List[int]) -> int:
    for i in range(1, len(nums)):
        if nums[i-1] > 0:
            nums[i] += nums[i-1]
    return max(nums) # max([-2,1,-2,4,3,5,6,1,5]) = 6
```

## Union Find

[Union Find](https://www.geeksforgeeks.org/union-find/) is a useful algorithm for graph

DSU for integers
```python
class DSU:
    def __init__(self, N):
        self.par = list(range(N))

    def find(self, x): # Find Parent
        if self.par[x] != x:
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr: # If parents are equal, return False
            return False
        self.par[yr] = xr # Give y node parent of x
        return True # return True if union occured
```

DSU for strings
```python
class DSU:
    def __init__(self):
        self.par = {}

    def find(self, x):
        if x != self.par.setdefault(x, x):
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr: return
        self.par[yr] = xr
```

DSU with union by rank
```python
class DSU:
    def __init__(self, N):
        self.par = list(range(N))
        self.sz = [1] * N

    def find(self, x):
        if self.par[x] != x:
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr:
            return False
        if self.sz[xr] < self.sz[yr]:
            xr, yr = yr, xr
        self.par[yr] = xr
        self.sz[xr] += self.sz[yr]
        return True
```

## Fast Power

Fast Power, or Exponential by [squaring](https://en.wikipedia.org/wiki/Exponentiation_by_squaring) allows calculating squares in logn time (x^n)*2 = x^(2*n)
```python
def myPow(self, x: float, n: int) -> float:
    if n < 0:
        n *= -1
        x = 1/x
    ans = 1        
    while n > 0:
        if n % 2 == 1:
            ans = ans * x
        x *= x
        n = n // 2
    return ans
```

## Fibonacci Golden

Fibonacci can be calulated with [Golden Ratio](https://demonstrations.wolfram.com/GeneralizedFibonacciSequenceAndTheGoldenRatio/)

```python
def fib(self, N: int) -> int:
    golden_ratio = (1 + 5 ** 0.5) / 2
    return int((golden_ratio ** N + 1) / 5 ** 0.5)
```

## Basic Calculator

A calculator can be simulated with stack

```python
class Solution:
    def calculate(self, s: str) -> int:
        s += '$'
        def helper(stk, i):
            sign = '+'
            num = 0
            while i < len(s):
                c = s[i]
                if c == " ":
                    i += 1
                    continue
                elif c.isdigit():
                    num = num * 10 + int(c)
                    i += 1
                elif c == '(':
                    num, i = helper([], i+1)
                else:
                    if sign == '+':
                        stk.append(num)
                    if sign == '-':
                        stk.append(-num)
                    if sign == '*':
                        stk.append(stk.pop() * num)
                    if sign == '/':
                        stk.append(int(stk.pop() / num))
                    i += 1
                    num = 0
                    if c == ')':
                        return sum(stk), i
                    sign = c
            return sum(stk)
        return helper([],0)
```

## Reverse Polish

```python
class Solution:
    def evalRPN(self, tokens: List[str]) -> int:
        stk = []
        while tokens:
            c = tokens.pop(0)
            if c not in '+-/*':
                stk.append(int(c))
            else:
                a = stk.pop()
                b = stk.pop()
                if c == '+':
                    stk.append(a + b)
                if c == '-':
                    stk.append(b-a)
                if c == '*':
                    stk.append(a * b)
                if c == '/':
                    stk.append(int(b / a))
        return stk[0]
```

## Resevior Sampling

Used to sample large unknown populations. Each new item added has a 1/count chance of being selected

```python
def __init__(self, nums):
    self.nums = nums
def pick(self, target):
    res = None
    count = 0
    for i, x in enumerate(self.nums):
        if x == target:
            count += 1
            chance = random.randint(1, count)
            if chance == 1:
                res = i
    return res
```

## String Subsequence

Can find the min number of subsequences of strings in some source through binary search and a dict of the indexes of the source array

```python
def shortestWay(self, source: str, target: str) -> int:
    ref = collections.defaultdict(list)
    for i,c in enumerate(source):
        ref[c].append(i)
    
    ans = 1
    i = -1
    for c in target:
        if c not in ref:
            return -1
        offset = ref[c]
        j = bisect.bisect_left(offset, i)
        if j == len(offset):
            ans += 1
            i = offset[0] + 1
        else:
            i = offset[j] + 1
            
    return ans
```

## Candy Crush

Removing adjacent duplicates is much more effective with a stack
```python
def removeDuplicates(self, s: str, k: int) -> str:
    stk = []
    for c in s:
        if stk and stk[-1][0] == c:
            stk[-1][1] += 1
            if stk[-1][1] >= k:
                stk.pop()
        else:
            stk.append([c, 1])
    ans = []
    for c in stk:
        ans.extend([c[0]] * c[1])
    return "".join(ans)
```

## Dutch Flag

[Dutch National Flag Problem](https://en.wikipedia.org/wiki/Dutch_national_flag_problem) proposed by [Edsger W. Dijkstra](https://en.wikipedia.org/wiki/Edsger_W._Dijkstra)


```python
def sortColors(self, nums: List[int]) -> None:
    """
    Do not return anything, modify nums in-place instead.
    """
    # for all idx < p0 : nums[idx < p0] = 0
    # curr is an index of element under consideration
    p0 = curr = 0
    # for all idx > p2 : nums[idx > p2] = 2
    p2 = len(nums) - 1

    while curr <= p2:
        if nums[curr] == 0:
            nums[p0], nums[curr] = nums[curr], nums[p0]
            p0 += 1
            curr += 1
        elif nums[curr] == 2:
            nums[curr], nums[p2] = nums[p2], nums[curr]
            p2 -= 1
        else:
            curr += 1
```



## Authors

* **Lichen Ma** - *compiling information* 



## Acknowledgments

* **Leetcode** - *content belongs to respective creators*


## Quick Access Links 
### LeetCode 
- [LeetCode - CheatSheet](#leetcode---cheatsheet)
	- [Getting Started](#getting-started)
		- [Prerequisites](#prerequisites)
	- [Built With](#built-with)
	- [Authors](#authors)
	- [Acknowledgments](#acknowledgments)
	- [Quick Access Links](#quick-access-links)
		- [LeetCode](#leetcode)
- [1-Two Sum](#1-two-sum)
	- [Brute Force](#brute-force)
	- [One Pass Hash Table](#one-pass-hash-table)
- [2-Add Two Numbers](#2-add-two-numbers)
	- [Elementary Math Solution](#elementary-math-solution)
- [3-Substring No Repeat](#3-substring-no-repeat)
	- [Brute Force](#brute-force-1)
	- [Sliding Window](#sliding-window)
	- [Sliding Window Optimized](#sliding-window-optimized)
- [4-Median of Two Sorted Arrays](#4-median-of-two-sorted-arrays)
	- [Recursive Approach](#recursive-approach)
- [5-Longest Palindromic Substring](#5-longest-palindromic-substring)
	- [Longest Common Substring](#longest-common-substring)
	- [Brute Force](#brute-force-2)
	- [Dynamic Programming](#dynamic-programming)
	- [Expand Around Center](#expand-around-center)
	- [Manacher's Algorithm](#manachers-algorithm)
- [6-ZigZag Conversion](#6-zigzag-conversion)
	- [Sort by Row](#sort-by-row)
	- [Visit by Row](#visit-by-row)
- [7-Reverse Integer](#7-reverse-integer)
	- [Pop and Push Digits and Check Before Overflow](#pop-and-push-digits-and-check-before-overflow)
- [8-String to Integer (atoi)](#8-string-to-integer-atoi)
	- [ASCII Conversion](#ascii-conversion)
- [9-Palindrome Number](#9-palindrome-number)
	- [Revert Half of the Number](#revert-half-of-the-number)
- [10-Regular Expression Matching](#10-regular-expression-matching)
	- [Recursion](#recursion)
	- [Dynamic Programming](#dynamic-programming-1)
	- [Non-Recursive](#non-recursive)
- [11-Container with the Most Water](#11-container-with-the-most-water)
	- [Brute Force](#brute-force-3)
	- [Two Pointer Approach](#two-pointer-approach)
- [12-Integer To Roman](#12-integer-to-roman)
	- [String Array](#string-array)
- [13-Roman to Integer](#13-roman-to-integer)
	- [Character Array](#character-array)
- [14-Longest Common Prefix](#14-longest-common-prefix)
	- [Horizontal Scanning](#horizontal-scanning)
	- [Vertical Scanning](#vertical-scanning)
	- [Divide and Conquer](#divide-and-conquer)
	- [Binary Search](#binary-search)
	- [Further Thoughts](#further-thoughts)
- [15-3Sum](#15-3sum)
	- [Sorted Array](#sorted-array)
- [16-3Sum Closest](#16-3sum-closest)
	- [3 Pointers](#3-pointers)
- [17-Letter Combinations of a Phone Number](#17-letter-combinations-of-a-phone-number)
	- [Backtracking](#backtracking)
	- [First In First Out (FIFO) Queue](#first-in-first-out-fifo-queue)
- [18-4Sum](#18-4sum)
	- [Sorted Array](#sorted-array-1)
- [19-Remove Nth Node From End of List](#19-remove-nth-node-from-end-of-list)
	- [Two Pass Algorithm](#two-pass-algorithm)
	- [One Pass Algorithm](#one-pass-algorithm)
- [20-Valid Parentheses](#20-valid-parentheses)
	- [Counting method](#counting-method)
	- [Stacks](#stacks)
- [21-Merge Two Sorted Lists](#21-merge-two-sorted-lists)
	- [Recursive](#recursive)
	- [Non-Recursive](#non-recursive-1)
- [22-Generate Parentheses](#22-generate-parentheses)
	- [Brute Force](#brute-force-4)
	- [Backtracking](#backtracking-1)
	- [Closure Number](#closure-number)
- [23-Merge k Sorted Lists](#23-merge-k-sorted-lists)
	- [Brute Force](#brute-force-5)
- [146-LRU Cache](#146-lru-cache)




<br><br><br><br><br>
***
<br><br><br>

<a name="twoSum"></a>
# 1-Two Sum 

Given an array of integers, return **indices** of the two numbers such that they add up to a specific target.
You may assume that each input would have **exactly one solution**, and you may not use the same element twice.

Example:
```
Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```

<br><br>
<a name="twoSumBruteForce"></a>
## Brute Force 

```java 
public int[] twoSum(int[] nums, int target) {
	for (int i=0; i<nums.size; i++){
		for (int j=i+1;j<nums.length;j++){
			if (nums[j]==target-nums[i]){
				return new int[] {i,j};
			}
		}
	}
	throw new IllegalArgumentException("No two sum solution");
} 
```
**Complexity Analysis** 
```
* Time complexity:   O(n^2)       we have a nested loop 
* Space complexity:  O(1) 	  we do not allocate any additional memory
```
<a name="twoSumOnePassHashTable"></a>
## One Pass Hash Table 

```java 
public int[] twoSum(int[] nums, int target) {
	Map<Integer, Integer> map = new HashMap<>();
	for(int i=0; i<nums.length; i++){
		int complement=target-nums[i];
		if (map.containsKey(complement)){
			return new int[] {map.get(complement),i};
		}
		map.put(nums[i],i);
	}
	throw new IllegalArgumentException("No two sum solution"); 
}
```
**Complexity Analysis**
```
* Time complexity:   O(n)		each lookup in the hash table only requires O(1) time
* Space complexity:  O(n)		we require additional space for the hash table which stores at most n
```

<br><br><br>
***
<a name="addTwoNumbers"></a>
# 2-Add Two Numbers 

Given two non-empty linked lists representing two non-negative integers with the digits stored in 
reverse order and each node containing a single digit, add the two numbers and return as a linked list

Example: 
```
Input (2 -> 4 -> 3) + (5 -> 6 -> 4) 
Output 7 -> 0 -> 8 

342 + 465 = 807
```


<br><br>
<a name="addTwoNumbersElementaryMath"></a>
## Elementary Math Solution

```java 
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) { val = x; }
 * }
 */



class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode dummyHead= new ListNode(0); 
        ListNode p=l1, q=l2, curr=dummyHead; 
        int carry=0; 
        while (p!=null||q!=null){
            int x= (p!=null) ? p.val :0; //if (p!=null) then x contains p.val
            int y= (q!=null) ? q.val :0;
            int sum=carry+x+y;
            carry=sum/10;
            curr.next=new ListNode(sum%10);
            curr=curr.next; 
            if (p!=null) p=p.next; 
            if (q!=null) q=q.next; 
        }
        if (carry>0){
            curr.next= new ListNode(carry);
        }
        return dummyHead.next; 
    }
}
```

**Complexity analysis** 
```
* Time Complexity:  O(max(m,n))         depends on the lengths of the two linked lists 
* Space Complexity: O(max(m,n))		the maximum length of the new list is max(m,n)+1
```


<br><br><br>
***
<a name="substringNoRepeat"></a>
# 3-Substring No Repeat 

Longest Substring Without Repeating Characters 

Given a string find the length of the longest substring without repeating characters. 

```
Example
Input: 		"abcabcbb"
Output:		3
Explanation:	The answer is "abc", with the length of 3
```
```
Example 2
Input:		"bbbbb"
Output:		1
Explanation:	The answer is "b", with the length of 1
```
```
Example 3
Input:		"pwwkew"
Output:		3
Explanation: 	The answer is "wke", with the length of 3. Note that the answer must be a substring
		"pwke" is a subsequence and not a substring 
```

<br><br>
<a name="substringNoRepeatBruteForce"></a>
## Brute Force 

*Algorithm* 


Suppose we have a function "boolean allUnique(String substring)" which returns true if all the
characters in the substring are unique and false otherwise. We can iterate through all the possible 
substrings of the given string s and call the function allUnique. If it turns out to be true, then we 
update our answer of the maximum length of substring without duplicate characters. 

To enumerate all substrings of a given string we enumerate the start and end indices of them. Suppose
the start and end indices are i and j respectively. Then we have 0 <= i <= j <= n. Thus using two 
nested loops with i from 0 to n-1 and j from i+1 to n, we can enumerate all the substrings of s

To check if one string has duplicate characters we can use a set. We iterate through all the 
characters in the string and put them into the set one by one. Before putting one character, we check
if the set already contains it. If so we return false and after the loop we return true.


```java 
public class Solution {
    public int lengthOfLongestSubstring(String s) {
        int n = s.length();
        int ans = 0;
        for (int i = 0; i < n; i++)
            for (int j = i + 1; j <= n; j++)
                if (allUnique(s, i, j)) ans = Math.max(ans, j - i);
        return ans;
    }

    public boolean allUnique(String s, int start, int end) {
        Set<Character> set = new HashSet<>();
        for (int i = start; i < end; i++) {
            Character ch = s.charAt(i);
            if (set.contains(ch)) return false;
            set.add(ch);
        }
        return true;
    }
}
```

**Complexity Analysis** 

```
* Time Complexity:   O(n^3)		Verifying if characters in   [i,j) are unique requires us to scan all of
					them which would cost O(j-i) time. 

					For a given i, the sum of time costed by each j -> [i+1,n] is 
					"Summation from i+1 to n O(j-1)"

					Thus, the sum of all the time consumption is: 
					O(summation from 0 to n-1(summation from j=i+1 to n (j-1))) 
					O(summation from i=0 to n-1(1+n-i)(n-i)/2)) = O(n^3)


					*Note that the sum of all numbers up to n 1+2+3+...+n = n(n+1)/2


* Space Complexity:  O(min(n,m))	We require O(k) space for checking a substring has no duplicate 
					characters, where k is the size of the set. The size of the Set is 
					upper bounded by the size of the string n amd the size of the charset
					or alphabet m 
				
				
```

<br><br>
<a name="substringNoRepeatSlidingWindow"></a>
## Sliding Window 

A sliding window is an abstract concept commonly used in array/string problems. A window is a range of 
elements in the array/string which usually defined by the start and end indices
```
Ex. [i,j) left-closed, right-open
```
A sliding window is a window that slides its two boundaries in a certain direction, for example if we
slide \[i,j) to the right by 1 element, then it becomes \[i+1, j+1) - left closed, right open.



Sliding Window approach, whenever we are looking at a section on an array usual to perform calculations
we don't need to completely recalculate everything for every section of the array. Usually we can use
the value obtained from another section of the array to determine something about this section of the 
array. For example if we are calculating the sum of sections of an array we can use the previously 
calculated value of a section to determine the sum of an adjacent section in the array. 
```
Ex. 1 2 3 4 5 6 7 8 
```
If we calculate the first section of four values we get 1+2+3+4 = 10 , then to calculate the next section
2+3+4+5 we can just take our first section (window_sum) and perform the operation: 
```
window_sum-first entry + last entry = 10-1+5= 14
```
So essentially for the window sliding technique we use what we know about an existing window to 
determine properties for another window. 

<br><br>
*Algorithm*

In the brute force approach, we repeatedly check a substring to see if it has duplicate characters but
this is unnecessary. If a substring from index i to j-1 is already checked to have no duplicate 
characters we only need to check if s[j] is already in the substring. 

To check if a character is already in the substring we can scan the substring which leads to an O(n^2)
algorithm but we can improve on this runtime using a HashSet as a sliding window to check if a 
character exists in the current set O(1). 

We use a HashSet to store the characters in the current window \[i,j) and then we slide the index j to
the right, if it is not in the HashSet, we slide j further until s[j] is already in the HashSet. At
this point we found the maximum size of substrings without duplicate characters starting with index i.
If we do this for all i, then we obtain our answer. 


```java 
public class Solution {
    public int lengthOfLongestSubstring(String s) {
        int n = s.length();
        Set<Character> set = new HashSet<>();
        int ans = 0, i = 0, j = 0;
        while (i < n && j < n) {
            // try to extend the range [i, j]
            if (!set.contains(s.charAt(j))){
                set.add(s.charAt(j++));
                ans = Math.max(ans, j - i);
            }
            else {
                set.remove(s.charAt(i++));
            }
        }
        return ans;
    }
}
```

**Complexity Analysis**
```
Time complexity:	O(2n)=O(n)	Worst case each character will be visited twice by i and j

Space complexity: 	O(min(m,n))	Same as the brute force method, we need O(k) space for the 
					sliding window where k is the size of the set. The size of the
					set is bounded by the size of the string n and the size of the
					charset/alphabet m
```


<br><br>
<a name="substringNoRepeatOptimized"></a>
## Sliding Window Optimized 

The previously discussed sliding window approach requires at most 2n steps and this could in fact be
optimized even further to require only n steps. Instead of using a set to tell if a character exists or
not, we could define a mapping of the characters to its index. Then we can skip the characters 
immediately when we found a repeated character 

If s[j] has a duplicate in the range \[i , j) with index j', we don't need to increase i little be little
we can just skip all the elements in the range \[i , j'] and let i be j'+1 directly 

```java 
public class Solution {
    public int lengthOfLongestSubstring(String s) {
        int n = s.length(), ans = 0;
        Map<Character, Integer> map = new HashMap<>(); // current index of character
        // try to extend the range [i, j]
        for (int j = 0, i = 0; j < n; j++) {
            if (map.containsKey(s.charAt(j))) {
                i = Math.max(map.get(s.charAt(j)), i);
            }
            ans = Math.max(ans, j - i + 1);
            map.put(s.charAt(j), j + 1);
        }
        return ans;
    }
}
```

<br><br><br>
***
<a name="medianofTwoSortedArrays"></a>
# 4-Median of Two Sorted Arrays 

There are two sorted arrays num1 and num2 of size m and n respectively. Find the median of the two 
sorted arrays. The overall run time complexity should be O(log (m+n)). You may assume nums1 and nums2
cannot be both empty. 

```
Example 

nums1 = [1, 3] 
nums2 = [2]

The median is 2.0
```

```
Example 2

nums1= [1, 2] 
nums2= [3, 4] 

The median is (2+3)/2 = 2.5
```


<br><br>
<a name="medianofTwoSortedArraysRecursiveApproach"></a>
## Recursive Approach

In statistics the median is used for dividing a set into two equal length subsets with one set being
always greater than the other set. To approach this problem first we cut A into two parts at a random
position i: 

```
         left_A                |           right_A 

  A[0], A[1], ... , A[i-1]         A[i], A[i+1], ... , A[m-1]
```

Since A has m elements, there are m+1 kinds of cutting as i can range from 0-m. We can also see that
left_A is empty when i is zero and right_A is empty when i=m

```
len(left_A) = i and len(right_A)= m-i
```

We can similarly cut B into two parts at a random position j: 

```
	left_B			|	right_B

  B[0], B[1], ... , B[j-1]	   B[j], B[j+1], ... , B[n-1]
```
  
Now if we put left_A and left_B into one set and put right_A and right_B into another set and name 
them left_part and right_part, then we get

```
	left_part		|	right_part
  A[0], A[1], ... , A[i-1]	  A[i], A[i+1], ... , A[m-1]
  B[0], B[1], ... , B[j-1]	  B[j], B[j+1], ... , B[n-1]
```

If we can ensure that 
1. the len(left_part) = len(right_part)
2. max(left_part) <= min(right_part)

then we divide all the elements in {A,B} into two parts with equal length and one part is always
greater than the other. Then 

```
median= (max(left_part)+min(right_part))/2
```
To ensure these two conditions, we need to ensure: 
1. i+j= m-i+n-j (or: m-i+n-j+1) if n>m, we just need to set i=0~m, j= (m+n+1)/2 - i
2. B\[j-1]<=A\[i] and A\[i-1]<=B\[j]

So, all we need to do is search for i in \[0,m] to find an object i such that 
B\[j-1]<=A\[i] and A\[i-1]<=B\[j] where j=(m+n+1)/2 -i

Then we perform a binary search following the steps described below: 

1) Set imin=0, imax=0, then start searching in \[imin, imax]
2) Set i=(imin+imax)/2 , j=(m+n+1)/2 - i
3) Now we have len(left_part) = len(right_part) and there are only 3 more situations which we may 
   encounter: 
   
```
   - B[j-1] <= A[i] and A[i-1]<=B[j] 
     This means that we have found the object i, so we can stop searching

   - B[j-1] > A[i]
     Means A[i] is too small, we must adjust i to get B[j-1]<=A[i] so we increase i because this will
     cuase j to be decreased. We cannot decrease i because when i is decreased, j will be increased
     so B[j-1] is increased and A[i] is decreased (B[j-1]<= A[i] will never be satisfied)

   - A[i-1] > B[j] 
     Means A[i-1] is too big and thus we must decrease i to get A[i-1]<=B[j]. In order to do that we 
     must adjust the searching range to [imin, i-1] so we set imax=i-1 and go back to step 2
```
When the object i is found, then the media is: 

 max(A\[i-1],B\[j-1]), when m+n is odd
(max(A\[i-1],B\[j-1])+min(A\[i],B\[j]))/2, when m+n is even

Next is to consider the edge values i=0, i=m, j=0, j=n where A\[i-1], B\[j-1], A\[i], B\[j] may not exist

```java 
class Solution {
	public double findMedianSortedArrays(int[] A, int[] B) {
		int m=A.length;
		int n=B.length;
		if (m>n) {   	//ensuring that m<=n
			int[] temp=A; A=B; B=temp;
			int tmp=m; m=n; n=tmp;
		}
		int iMin=0, iMax=m, halfLen=(m+n+1)/2;
		while (iMin<=iMax) {
			int i=(iMin+iMax)/2
			int j= halfLen - i;
			if (i<iMax && B[j-1] > A[i]){
				iMin=i+1; //i is too small
			}
			else if (i>iMin && A[i-1]>B[j]) {
				iMax=i-1; //i is too big
			}
			else{ //we have found the object i 
				int maxLeft=0; 
				if (i==0) {
					maxLeft=B[j-1];
				}
				else if (j==0){
					maxLeft=A[i-1];
				}
				else{
					maxLeft=Math.max(A[i-1], B[j-1]);
				}

				if ((m+n)%2 ==1) {
					return maxLeft;
				}

				int minRIght=0;
				if (i==m) {
					minRight=B[j];
				}
				else if (j==n) {
					minRight=A[i];
				}
				else {
					minRight=Math.min(B[j], A[i]);
				}

				return (maxLeft+minRight)/2.0;
			}
		}
		return 0.0;
	}
}
```

**Complexity Analysis**

```
Time Complexity: O(log(min(m,n)))	At first the searching range is [0,m] and the length of this 
					searching range will be reduced by half after each loop so we
					only need log(m) loops. Since we do constant operations in 
					each loop the time complexity is O(log(m) and since m<=n the
					time complexity is O(log(min(m,n))

Space Complexity: O(1)			We only need constant memory to store 9 local variables so the
					space complexity is O(1)
```


<br><br><br>
***
<a name="longestPalindromicSubstring"></a>
# 5-Longest Palindromic Substring

Given a string s, find the longest palindromic substring in s. You may assume that the maximum length
of s is 1000. 

```
Example 1: 

Input: "babad" 
Output: "bab" 

Note: "aba" is also a valid answer 
```

```
Example 2: 

Input: "cbbd"
Output: "bb" 
```

<br><br>
<a name="longestPalindromicSubstringLongestCommonSubstring"></a>
## Longest Common Substring

Some people will be tempted to come up with this quick solution which is unforunately flawed, "reverse
S and become S'. Find the longest common substring between S and S' and that will be the longest
palindromic substring." This will work with some examples but there are some cases where the longest
common substring is not a valid palindrome. 

	Ex. S="abacdfgdcaba", S'="abacdgfdcaba" 	

	The longest common substring between S and S' is "abacd" and clearly this is not a valid 
	palindrome

We can solve this problem however by checking if the substring's indices are the same as the reversed
substring's original indices each time we find a longest common substring. If it is, then we attempt
to update the longest palindrome found so far, if not we skip this and find the next candidate

**Complexity Analysis**
```
Time Complexity: O(n^2) 
Space Complexity: O(n^2) 
```
<br><br>
<a name="longestPalindromicSubstringBruteForce"></a>
## Brute Force 

The obvious brute force solution is to pick all possible starting and ending position for a substring 
and verify if it is a palindrome 

**Complexity Analysis**
```
Time Complexity: O(n^3)		If n is the length of the input string, there are a total of 
				(n 2) = n(n-1)/2 substrings and since verifying each substring takes 
				O(n) time, the run time complexity is O(n^3)

Space Complexity: O(1) 
```
<br><br>
<a name="longestPalindromicSubstringDynamicProgramming"></a>
## Dynamic Programming 

We can improve on the brute force solution by avoid some unnecessary re-computation while validating 
palidromes. Consider the word "ababa", if we already know that "bab" is a palindrome then we can 
determine that ababa is a palindrome by noticing that the two left and right letters connected to bab
are the same. 

This yields a straight forward dynamic programming solution where we initialize the one and two letters
palindromes and then work our way up finding all three letters palindromes and so on.

**Complexity Analysis**
```
Time Complexity: 	O(n^2)	

Space Complexity: 	O(n^2)	Using O(n^2) space to store the table 
```
<br><br>
<a name="longestPalindromicSubstringExpandAroundCenter"></a>
## Expand Around Center

This approach allows us to solve this problem in O(n^2) time using only constant space complexity. We
observe that a palindrome mirrors around its enter and therefore a palindrome can be expanded from its
center and there are only 2n-1 such centers (for palindromes with an even number of letters like 
"abba" its center is in between two letters).

```java 
public String longestPalindrome(String s) {
	if (s==null || s.length() < 1) return "";     //edge case 
	int start=0, end=0;
	for (int i=0; i<s.length(); i++) {
		int len1=expandAroundCenter(s,i,i);
		int len2=expandAroundCenter(s,i,i+1);
		int len=Math.max(len1,len2);
		if (len>end-start) {
			start= i-(len-1)/2;
			end=i+len/2
		}
	}
	return s.substring(start,end+1);
}

private int expandAroundCenter(String s, int left, int right) {
	int L=left, R=right;
	while(L>=0 && R<s.length() && s.charAt(L)==s.charAt(R)) {
		L--;
		R++;
	}
	return R-L-1;
}
```

<br><br>
<a name="longestPalindromicSubstringManacherAlgorithm"></a>
## Manacher's Algorithm 

There is an O(n) algorithm called Manacher's algorithm, however, it is a non-trivial algorithm and no 
one would expect you to come up with this algorithm in a 45 minute coding session


<br><br><br>
***
<a name="zigZagConversion"></a>
# 6-ZigZag Conversion 

The string "PAYPALISHIRING" is written in a zigzag pattern on a given number of rows like this: 
```
P   A   H   N
A P L S I I G
Y   I   R
```
And then read line by line: "PAHNAPLSIIGYIR". Write a code that will take a string and make this 
conversion given a number of rows: 

```
string convert(string s, int numRows);
```

```
Example 1: 

Input: s="PAYPALISHIRING", numRows=3
Output: "PAHNAPLSIIGYIR"
```

```
Example 2:

Input: s="PAYPALISHIRING", numRows=4
Output: "PINALSIGYAHRPI"

Explanation:

P           I          N
A       L   S      I   G
Y   A       H   R
P           I
```

<br><br>
<a name="zigZagConversionSortbyRow"></a>
## Sort by Row 

By iterating through the string from left to right we can easily determine which row in the Zig-Zag
pattern that a character belongs to

<br><br>
*Algorithm*

We can use min(numRows,len(s)) lists to represent the non-empty rows of the Zig-Zag Pattern. 
Iterate through s from left to right appending each character to the appropriate row. The appropriate
row can be tracked using two variables: the current row and the current direction. 

The current direction only changes when we moved to the topmost row or moved down to the bottommost 
row 

```java
class Solution {
	public String convert(String s, int numRows) {
		if (numRows==1) return s;		//if there is only one row return string

		List<StringBuilder> rows=new ArrayList<>();
		for (int i=0; i<Math.min(numRows, s.length()); i++){
			rows.add(new StringBuilder());
		}
		int curRow=0;
		boolean goingDown=false;

		for(char c: s.toCharArray()) {
			rows.get(curRow).append(c);
			if (curRow==0 || curRow==numRows-1) {
				goingDown=!goingDown;
			}
			curRow+=goingDown ? 1 : -1;
		}	

		StringBuilder ret= new StringBuilder();
		for(StringBuilder row:rows) {
			ret.append(row);
		}
		return ret.toString();
	}
}
```

**Complexity Analysis**

```
Time Complexity:  O(n)	where n==len(s)
Space Complexity: O(n)
```

<br><br>
<a name="zigZagConversionVisitbyRow"></a>
## Visit by Row

Visit the characters in the same order as reading the Zig-Zag pattern line by line

<br><br>
*Algorithm*

Visit all characters in row 0 first, then row 1, then row 2, and so on.
For all whole numbers k, 
	* characters in row 0 are located at indexes  k\*(2\*numRows-2)
	* characters in row numRows -1 are located at indexes  k\*(2\*numRows-2)+ numRows -1 
	* characters in inner row i are located at indexes  k\*(2\*numRows-2)+i and (k+1)(2\*numRows-2)-i

```java
class Solution {
	public String convert(String s, int numRows) {
		if (numRows==1) return s; 

		StringBuilder ret=new StringBuilder();
		int n=s.length();
		int cycleLen= 2* numRows -2;

		for (int i=0; i<numRows; i++) {
			for (int j=0; j+1<n; j+= cycleLen) {
				ret.append(s.charAt(j+i));
				if (i!=0 && i!=numROws-1 && j+cycleLen-i<n) {
					ret.append(s.charAt(j+cycleLen-i));
				}
			}
			return ret.toString();
		}
	}
}
```

**Complexity Analysis**
```
Time Complexity: O(n)	where n==len(s) Each index is visited once

Space Complexity: O(n) 	C++ implementation can achieve O(1) if the return string is not considered 
			extra space
```


<br><br><br>
***
<a name="reverseInteger"></a>
# 7-Reverse Integer 

Given a 32- bit signed integer, reverse digits of an integer. 

```
Example 1: 

Input: 123
Output: 321
```

```
Example 2: 

Input: -123
Output: -321
```

```
Example 3: 

Input: 120 
Output: 21
```

For the purpose of this problem assume that your function returns 0 when the reversed integer overflows

<br><br>
<a name="reverseIntegerPopandPush"></a>
## Pop and Push Digits and Check Before Overflow 

We can build up the reverse integer one digit at and time and before doing so we can check whether or
not appedning another digit would cause overflow 

<br><br>
*Algorithm*

Reversing an integer can be done similarly to reversing a string. We want to repeatedly "pop" the last
digit off of x and push it to the back of the rev so that in the end rev is the reverse of x. 

To push and pop digits without the help of some auxiliar stack/array we can use math 

```
//pop operation: 
pop = x%10; 
x/=10;

//push operation:
temp=rev*10+pop;
rev =temp;
```

This statement is dangerous however as the statement temp=rev\*10+pop may cause an overflow and luckily
it is easy to check beforehand whether or not this statement would cause an overflow. 

1. If temp=rev\*10+pop causes an overflow, then rev>=INTMAX/10
2. If rev> INTMAX/10, then temp=rev\*10+pop is guaranteed to overflow
3. if rev==INTMAX/10, then temp=rev\*10 + pop will overflow if an only if pop>7

```java
class Solution {
	public int reverse(int x) {
		int rev=0; 
		while (x!=0) {
			int pop=x%10;
			x/=10;
			if (rev>Integer.MAX_VALUE/10||(rev==Integer.MAX_VALUE/10 && pop>7)) return 0;
			if (rev<Integer.MIN_VALUE/10||(rev==Integer.MIN_VALUE/10 && pop<-8)) return 0;
			rev=rev*10 +pop;
		}
		return rev;
	}
}
```

**Complexity Analysis**
```
Time Complexity:  O(log(x))	There are roughly log10(x) digits in x 
Space Complexity: O(1)
```


<br><br><br>
***
<a name="stringtoInteger"></a>
# 8-String to Integer (atoi)

Implement atoi which converts a string to an integer 

The function first discards as many whitespace characters as necessary until the first non-whitespace
character is found. Then, starting from this character, takes an optional initial plus or minus sign
followed by as many numerical digits as possible and interprets them as a numerical value. 

The string can contain additional characters after those that form the integral number, which are 
ignored and have no effect on the behavior of this function. 

If the first sequence of non-whitespace characters in str is not a valid integral number, or if no such
sequence exits because either str is empty or it contains only whitespace characters, no conversion is
performed. 

If no valid conversion could be performed a zero value is returned 

Note: 
* only the space character ' ' is considered as whitespace character 
* assume we are dealing with an environment which could only store integers within the 32-bit signed integer range: [-2^31, 2^31-1]. If the numerical value is out of the range of representable values, INT_MAX (2^31-1) or INT_MIN (-2^31) is returned

```
	Example 1: 

	Input: "42"
	Output: 42
```

```
	Example 2: 

	Input: "      -42" 
	Output: -42
```

```
	Example 3:

	Input: "4193 with words "
	Output: 4193
```

```
	Example 4: 
	
	Input: "words and 987"
	Output: 0
```

```
	Example 5:
	
	Input: "-91283472332"
	Output: -2147483648 	//out of the range of a 32-bit signed integer so INT_MIN is returned
```


<br><br>
<a name="stringtoIntegerASCII"></a>
## ASCII Conversion

Recognize that ASCII characters are actually numbers and 0-9 digits are numbers starting from decimal
48 (0x30 hexadecimal) 

```
	'0' is 48
	'1' is 49
	...
	'9' is 57
```
So to get the value of any character digit you can just remove the '0' 

```
	'1' - '0' => 1
	49  -  48 => 1
```

```java
public int myAtoi(String str) {
	int index=0, sign=1, total=0;
	
	//1. Empty string 
	if (str.length() ==0) return 0;

	//2. Remove Spaces 
	while(str.charAt(index)==' ' && index < str.length())
		index++;
	
	//3. Handle signs 
	if (str.charAt(index)=='+' || str.charAt(index)=='-'){
		sign= str.charAt(index) == '+' ? 1:-1;
		index++;
	}

	//4. COnvert number and avoid overflow
	while(index<str.length()){
		int digit= str.charAt(index) - '0'; 
		if (digit<0||digit>9) break;

		//check if total will overflow after 10 times and add digit
		if (Integer.MAX_VALUE/10 < total || Integer.MAX_VALUE/10 == total 
		    && Integer.MAX_VALUE%10<digit) {    
		    return sign==1 ? Integer.MAX_VALUE : Integer.MIN_VALUE;
		}
		total= 10* total+digit;
		index++;
	}
	return total*sign;
}
```


<br><br><br>
***
<a name="palindromeNumber"></a>
# 9-Palindrome Number


Determines whether an interger is a palindrome. An integer is a palindrome when it reads the same 
backward as forward. 

```
Example 1: 

Input: 121
Output: true
```

```
Example 2: 

Input: -121
Output: false 
Explanation: 	From left to right, it reads -121, meanwhile from right to left it becomes 121- . 
		Therefore it is not a palindrome
```

```
Example 3: 

Input: 10 
Output: false 
Explanation: 	Reads 01 from right to left. Therefore it is not a palindrome
```


<br><br>
<a name="palindromeNumberRevertHalf"></a>
## Revert Half of the Number

A first idea which may come to mind is to convert the number into a string and check if the string is a
palindrome but this would require extra non-constant space for creating the string not allowed by the 
problem description 

Second idea would be reverting the number itself and comparing the number with the original number, if
they are the same then the number is a palindrome, however if the reversed number is larger than 
int.MAX we will hit integer overflow problem. 

To avoid the overflow issue of the reverted number, what if we only revert half of the int number? The
reverse of the last half of the palindrome should be the same as the first half of the number if the 
number is a palindrome. 

If the input is 1221, if we can revert the last part of the number "1221" from "21" to "12" and compare
it with the first half of the number "12", since 12 is the same as 12, we know that the number is a 
palindrome. 

<br><br>
*Algorithm* 

At the very beginning we can deal with some edge cases. All negative numbers are not palindrome and 
numbers ending in zero can only be a palindrome if the first digit is also 0 (only 0 satisfies this 
property) 

Now let's think about how to revert the last half of the number. For the number 1221 if we do 1221%10 
we get the last digit 1. To get the second last digit we divide the number by 10 1221/10=122 and then
we can get the last digit again by doing a modulus by 10, 122%10=2. If we multiply the last digit by 
10 and add the second last digit 1\*10+2=12 which gives us the reverted number we want. COntinuing this
process would give us the reverted number with more digits. 

Next is how do we know that we've reached the half of the number? 
Since we divided the number by 10 and multiplied the reversed number by 10 when the original number is
less than the reversed number, it means we've gone through half of the number digits. 

```java
class Solution {
    public boolean isPalindrome(int x) {
        if (x<0 || (x%10==0 && x!=0)) {
            return false;
        }
        
        int revertedNumber=0;
        while (x>revertedNumber){
            revertedNumber=x%10+revertedNumber*10;
            x/=10;
        }
        //when the length is an odd number, we can get rid of the middle digit by 
        //revertedNumber/10
        
        //For example when the input is 12321, at the end of the while loop we get x=12, 
        //revertedNumber=123, since the middle digit doesn't matter in a palindrome we can
        //simply get rid of it 
        
        return x==revertedNumber||x==revertedNumber/10;
    }
}
```


<br><br><br>
***
<a name="regularExpressionMatching"></a>
# 10-Regular Expression Matching

Given an input string (s) and a pattern (p), implement regular expression matching with support for '.'
and '*'

```
	'.' Matches any single character
	'*' Matches zero or more of the preceding element 
```
The matching should cover the entire input string (not partial) 

Note: 
* s could be empty and contains only lower case letters a-z
* p could be empty and contains only lower case letters a-z and characters like . or * 

```
Example 1: 

Input:
	s="aa" 
	p="a" 
	Output: false 
	Explanation: 	"a" does not match the entire string "aa" 
```

```
Example 2: 

Input: 
	s="aa"
	p="a*" 
	Output: true 
	Explanation: 	'*' means zero of more of the preceding element, 'a'. Therefore, by repeating
			'a' once it becomes "aa"
```

```
Example 3: 

Input: 
	s="ab" 
	p=".*" 
	Output: true 
	Explanation: 	'.*' means "zero or more (*) of any character (.)"
```

```
Example 4: 

Input: 
	s="aab" 
	p="c*a*b" 
	Output: true
	Explanation: 	c can be repeated 0 times, a can be repeated 1 time. Therefore it matches 
			"aab" 
```

```
Example 5: 

Input: 
	s="mississippi" 
	p="mis*is*p*."
	Output: false 
```

<br><br>
<a name="regularExpressionMatchingRecursion"></a>
## Recursion

If there were no Kleene stars (the * wildcard characters for regular expressions), the problem would 
be easier- we simply check from left to right if each character of the text matches the pattern. When
a star is present we may need to check for may different suffixes of the text and see if they match
the rest of the pattern. A recursive solution is a straightforward way to represent this relationship

```java
class Solution {
	public boolean isMatch(String text, String pattern) {
		if (pattern.isEmpty()) return text.isEmpty(); 
		
		boolean first_match=(!text.isEmpty() && 
				    (pattern.charAt(0)==text.charAt(0) || pattern.charAt(0)=='.'));

		if (pattern.length()>=2 && pattern.charAt(1) =='*'){
			return (isMatch(text,pattern.substring(2))||
			       (first_match && isMatch(text.substring(1),pattern)));
		
		//note: pattern.substring(2) returns all of the characters after index 2 of pattern
		}
		else {
			return first_match && isMatch(text.substring(1), pattern.substring(1));
		}
		
	}
}
```

**Complexity Analysis**

```
Time Complexity: 	Let T, P be the lengths of the text and the pattern respectively. In the worst
			case, a call to match(text[i:],pattern[2j:]) will be made (i+j i) times, and 
			strings of the order O(T-i) and O(P-2*j) will be made. Thus the complexity has
			the order: 

			summation from i=0 to T * summation from j=0 to P/2 * (i+j i) O(T+P-i-2j).

			We can show that this is bounded by O((T+P)2^(T+P/2))

Space Complexity:	For every call to match, we will create those strings as described above 
			possibly creating duplicates. If memory is not freed, this will also take a
			total of O((T+P)2^(T+P/2)) space even though there are only order O(T^2+P^2) 
			unique suffixes of P and T that are actually required 
```

<br><br>
<a name="regularExpressionMatchingDynamicProgramming"></a>
## Dynamic Programming

As the problem has an optimal substructure, it is natural to cache intermediate results. We ask the 
question dp(i,j): does text[i:] and pattern[j:] match? We can describe our answer in terms of answers
to questions involving smaller strings

<br><br>
*Algorithm* 

We proceed with the same recursion as in Approach 1, except because calls will only ever be made to 
match(text[i:], pattern[j:]), we use dp(i,j) to handle those calls instead, saving us expensive 
string-building operations and allowing us to cache the intermediate results 


**Java Top-Down Variation**

```java
enum Result {
	TRUE, FALSE
	
}

class Solution {
	Result[][] memo; 

	public boolean isMatch(String text, String pattern) { 
		memo=new Result[text.length() +1][pattern.length() +1];
		return dp(0,0,text,pattern);
	}

	public boolean dp(int i, int j, String text, String pattern) {
		if (memo[i][j]!=null) {
			return memo[i][j]==Result.TRUE;
		}
		boolean ans; 
		if (j==pattern.length()){
			ans=i==text.length();
		}
		else {
			boolean first_match=(i<text.length() && (pattern.charAt(j) == text.charAt(i) ||
					     patter.charAt(j) == '.'));

			if (j+1<pattern.length() && pattern.charAt(j+1)=='*'){
				ans=(dp(i,j+1,text,pattern)||first_match&& dp(i+1,j,text,pattern));
			}
			else {
				ans=first_match && dp(i+1, j+1, text, pattern); 
			}
		}
		memo[i][j]=ans? Result.TRUE: Result.FALSE; 
		return ans; 
	}
}
```

**Complexity Analysis**

```
Time Complexity: 	Let T, P be the lengths of the text and the pattern respectively. The work 
			for every call to dp(i,j) for i=0,...,T; j=0,...,P is done once and it is O(1) 				work. Hence the time complexity is O(TP)

Space Complexity:	The only memory we use is the O(TP) boolean entries in our cache. Hence, the 
			space complexity is O(TP) 
```

<br><br>
<a name="regularExpressionMatchingNonRecursive"></a>
## Non-Recursive

The recursive programming solutions are pretty confusing so this implementation uses 2D arrays and 
Dynamic Programming 


The logic works as follows: 
```
1. If p.charAt(j) == s.charAt(i) : dp[i][j] = dp[i-1][j-1]; 
2. If p.charAt(j) == '.' : dp[i][j] = dp[i-1][j-1]; 
3. If p.charAt(j) == '*': 
	
	Subconditions
	1. If p.charAt(j-1)!= s.charAt(i):dp[i][j]=dp[i][j-2]  	//in this case a* only counts as empty
	2. If p.charAt(i-1)== s.charAt(i) or p.charAt(i-1) == '.': 
		
		dp[i][j] = dp[i-1][j]	//in this case a* counts as multiple a 
	     or dp[i][j] = dp[i][j-1]	//in this case a* counts as single a 
	     or dp[i][j] = dp[i][j-2]	//in this case a* counts as empty 
```

```java
public boolean isMatch(String s, String p) {
	if (s==null || p==null){
		return false;
	}
	boolean[][] dp=new boolean[s.length()+1][p.length()+1];
	dp[0][0]=true; 
	for (int i=0;i<p.length(); i++){
		if (p.charAt(i)=='*' && dp[0][i-1]){
			dp[0][i+1]=true; 
		}
	}
	for (int i=0;i<s.length();i++){
		for (int j=0;j<p.length();j++){
			if (p.charAt(j)=='.'){
				dp[i+1][j+1]=dp[i][j];
			}
			if (p.charAt(j)==s.charAt(i)){
				dp[i+1][j+1]=dp[i][j];
			}
			if (p.charAt(j)=='*'){
				if (p.charAt(j-1)!=s.charAt(i) && p.charAt(j-1) !='.'){
					dp[i+1][j+1]=dp[i+1][j-1];
				}
				else{
					dp[i+1][j+1]=(dp[i+1][j] || dp[i][j+1] || dp[i+1][j-1]);
				}
			}
		}
	}
	return dp[s.length()][p.length()];
}
```


<br><br><br>
***
<a name="containerwiththeMostWater"></a>
# 11-Container with the Most Water 

Given n non negative integers a1,a2, ... , an where each represents a point at coordinate (i, ai). n 
vertical lines are drawn such that the two endpoints of line i is at (i, ai) and (i, 0). Find two 
lines, which together with x-axis forns a container such that the container contains the most water. 

```Example: The array [1,8,6,2,5,4,8,3,7] would have a max area of water which is 49. 

		      ^		    ^
	 These two values form the container which could hold water at a max height of 7, these values
	 are also 7 array indexes apart from each other so it could hold water at a max width of 7. The
	 area of water which could be held is thus 7 x 7 = 49
```


<a name="containerwiththeMostWaterBruteForce"></a>
## Brute Force

In this case we simply consider the area for every possible pair of the lines and find out the maximum
area out of those. 

```
public class Solution {
	public int maxArea(int[] height) {
		int maxarea=0; 
		for (int i=0; i<height.length; i++){
			for (int j=i+1;j<height.length;j++){
				maxarea=Math.max(maxarea, Math.min(height[i],height[j])*(j-i));
			}
		}
		return maxarea;
	}
}
```

**Complexity Analysis**
```
Time complexity: 	O(n^2) 	Calculating the area for all n(n-1)/2 height pairs 
Space complexity: 	O(1) 	Constant extra space is used 
```

<br><br>
<a name="containerwiththeMostWaterTwoPointer"></a>
## Two Pointer Approach

The intuition behind this approach is that the area formed between the lines will always be limited by 
the height of the shorter line. Further, the farther the lines, the more will be the area obtained. 

We take two pointers, one at the beginning and one at the end of the array constituting the length of 
the lines. Further, we maintain a variable maxarea to store the maximum area obtained till now. At 
every step, we find out the area formed between them, update maxarea and move the pointer pointing to 
the shorter line towards the other end by one step. 

Initially we consider the area constituting the exterior most lines. Now to maximize the area we need
to consider the area between the lines of larger lengths. If we try to move the pointer at the longer
line inwards, we won't gain any increase in area, since it is limited by the shorter line. But moving
the shorter line's pointer could turn out to be benefical, as per the same argument, despite the 
reduction in width. This is done since a relatively longer line obtained by moving the shorter line's 
pointer might overcome the reduction in area caused by the width reduction. 

```java
public class Solution {
	public int maxArea(int[] height) {
		int maxarea=0, l=0, r=height.length-1; 
		while (l<r){
			maxarea=Math.max(maxarea,Math.min(height[l],height[r])*(r-l));
			if (height[l]<height[r]){
				l++;
			}
			else{
				r--;
			}
		}
		return maxarea; 
	}
}
```

**Complexity Analysis**
```
Time complexity: 	O(n) 	Single pass
Space complexity: 	O(1) 	Constant space is used 
```

<br><br><br>
***
<a name="integertoRoman"></a>
# 12-Integer To Roman 

Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M
```
Symbol		Value 
I		1
V		5
X		10
L		50
C		100
D		500
M		1000
```

For example, two is written as II in Roman numeral, just two one's added together. Twelve is written as
XII which is simply X + II. The number twenty seven is written as XXVII, which is XX + V + II. 

Roman numerals are usually written largest to smallest from left to right. However, the numeral for 
four is not IIII. Instead, the number four is written as IV. Because the one is before the five we 
subtract it making four. The same principle applies to the number nine which is written as IX. There 
are six instances where subtraction is used: 

* I can be placed before V (5) and X (10) to make 4 and 9 
* X can be placed before L (50) and C(100) to make 40 and 90 
* C can be placed before D (500) and M(1000) to make 400 and 900

Given an integer, convert it to a roman numeral, input is guaranteed to be within the range from 
1 to 3999

```
Example 1: 

Input: 3 
Output: "III" 
```

```
Example 2: 

Input: 4
Output: "IV" 
```

```
Example 3: 

Input: 9 
Output: "IX" 
```

```
Example 4: 

Input: 58 
Output: "LVIII" 
Explanation: L=50, V=5, III=3
```

```
Example 5: 

Input: 1994
Output: "MCMXCIV"
Explanation: M=1000, CM=900, XC=90 and IV=4 
```

<a name="integertoRomanStringArray"></a>
## String Array

```java
public static String intToRoman(int num) { 
	
	String M[]={"", "M", "MM", "MMM"};
	//represents 1000, 2000, and 3000 since we know the number is in the range 1 to 3999
	
	String C[]={"", "C", "CC", "CCC", "CD", "D", "DC", "DCC", "DCCC", "CM"};
	//represents 0, 100,  200,   300,  400, 500,  600,   700,    800,  900

	String X[]={"", "X", "XX", "XXX", "XL", "L", "LX", "LXX", "LXXX", "XC"};
	//represents 0,  10,   20,    30,   40,  50,   60,    70,     80,   90

	String I[]={"", "I", "II", "III", "IV", "V", "VI", "VII", "VIII", "IX"}; 
	//represents 0,   1,    2,     3,    4,  5,    6,     7,      8,    9

	return M[num/1000] + C[(num%1000)/100] + X[(num%100)/10] + I[num%10]; 
} 
```

<br><br><br>
***
<a name="romantoInteger"></a>
# 13-Roman to Integer

Roman numerals are represented by seven different symbols I, V, X, L, C, D and M 
```
Symbol 		Value 
I		1
V		5
X		10 
L		50
C		100
D		500
M		1000
```

For example, two is written as II in Roman numeral, just two one's added together. Twelve is written as
XII which is simply X + II. The number twenty seven is written as XXVII, which is XX + V + II. 

Roman numerals are usually written largest to smallest from left to right. However, the numeral for 
four is not IIII. Instead, the number four is written as IV. Because the one is before the five we 
subtract it making four. The same principle applies to the number nine which is written as IX. There 
are six instances where subtraction is used: 

* I can be placed before V (5) and X (10) to make 4 and 9 
* X can be placed before L (50) and C(100) to make 40 and 90 
* C can be placed before D (500) and M(1000) to make 400 and 900

Given an integer, convert it to a roman numeral, Input is guaranteed to be within the range from 
1 to 3999

```
Example 1: 
	
Input: "III" 
Output: 3 
```

```
Example 2: 

Input: "IV" 
Output: 4
```

```
Example 3: 

Input: "IX" 
Output: 9 
```

```
Example 4: 

Input: "LVIII" 
Output: 58 
Explanation: L=50, V=5, III=3
```

```
Example 5: 

Input: "MCMXCIV" 
Output: 1994
Explanation: M=1000, CM=900, XC=90 and IV=4
```
<br><br>
<a name="romantoIntegerCharacterArray"></a>
## Character Array

```java
class Solution {
	public int romanToInt(String s) {
		Map<Character, Integer> map = new HashMap(); 
		map.put('I', 1); 
		map.put('V', 5); 
		map.put('X', 10); 
		map.put('L', 50); 
		map.put('C', 100); 
		map.put('D', 500); 
		map.put('M', 1000); 

		char[] sc= s.toCharArray(); 
		int total= map.get(sc[0]); 
		int pre=map.get(sc[0]); 
		for (int i=1; i<sc.length; i++) {
			int curr=map.get(sc[i]); 
			if (curr<=pre) {
				total= total + curr; 
			}
			else {
				total=total+curr -2*pre; 
			}
			pre=curr; 
		}
		return total; 
	}

}
```

<br><br><br>
***
<a name="longestCommonPrefix"></a>
# 14-Longest Common Prefix

Write a function to find the longest common prefix string amongst an array of strings. If there is no 
common prefix, return an empty string ""

```
Example 1: 

Input: ["flower", "flow", "flight"]
Output: "fl"
```

```
Example 2: 

Input: ["dog", "racecar", "car"] 
Output: ""

Explanation: There is no common prefix among the input strings 
```

*Note:* 
All given inputs are in lowercase letters a-z

<br><br>
<a name="longestCommonPrefixHorizontalScanning"></a>
## Horizontal Scanning

<br>
*Intuition:* 

For a start we will describe a simple way of find the longest prefix shared by a set of strings 
LCP(S1 ... Sn).We will use the observation that: 
```
LCP(S1 ... Sn) = LCP(LCP(LCP(S1, S2), S3), ... Sn) 
```

<br><br>
*Algorithm:*

To employ this idea, the algorithm iterates through the strings [S1 ... Sn]. finding at each iteration
i the longest common prefix of strings LCP(S1 ... Si). When LCP(S1 ... Si) is an empty string, the 
algorithm ends. Otherwise after n iterations, the algorithm returns LCP(S1 ... Sn) 

```

Example: 

{leets, leetcode, leet, leeds}
   \       /      
  LCP{1,2} = leets
  	     leetcode
	     leet 

	 	\	{leets, leetcode, leet, leeds}
		 \ 			   /

		 LCP{1,3} = leet
		 	    leet
			    leet

			      \          {leets, leetcode, leet, leeds}
			       \ 				  /
			       LCP{1,4}   leet
			       		  leeds
					  lee

				LCP{1,4} = "lee"
```

```java
public String longestCommon Prefix(String[] strs){
	if (strs.length==0){
		return ""; 
	}
	String prefix=strs[0]; 
	for (int i=1; i<strs.length; i++) {
		while (strs[i].indexOf(prefix) != 0) {
			prefix=prefix.substring(0, prefix.length() -1);
			if (prefix.isEmpty()) {
				return "";
			}
		}
		return prefix; 
	}
}
```

**Complexity Analysis**
```
Time complexity: 	O(S)	Where S is the sum of all characters in all strings. In the worse case
				all n strings are the same. The algorithm compares the string S1 with 
				the other strings [S2 ... Sn]. There are S character comparisons where
				S is the sum of all characters in the input array 

Space complexity: 	O(1) 	We only used constant extra space 
```


<br><br>
<a name="longestCommonPrefixVerticalScanning"></a>
## Vertical Scanning

Imagine a very short string is at the end of the array. The above approach will still do S comparisons.
One way to optimize this case is to do vertical scanning. We compare characters from top to bottom on
the same column (same character index of the strings) before moving on to the next column. 


```java
public String longestCommonPrefix(String[] strs) {
	if (strs==null || strs.length==) return ""; 
	for (int i=0; i<strs[0].length(); i++){
		char c=strs[0].charAt(i); 
		for (int j=1; j<strs.length; j++) {
			if (i==strs[j].length() || strs[j].charAt(i)!=c){
				return strs[0].substring(0,i);
			}
		}
	}
	return strs[0]; 
}
```

**Complexity Analysis**

```
Time complexity: 	O(S) 	Where S is the sum of all characters in all strings. In the worst case
				there will be n equal strings with length m and the algorithm performs
				S=n*m character comparisons. Even the worst case is still the same as 
				Approach 1, in the best case there are at most n*minLen comparisons 
				where minLen is the length of the shortest string in the array. 

Space complexity: 	O(1)	We only used constant extra space
```

<br><br>
<a name="longestCommonPrefixDivideandConquer"></a>
## Divide and Conquer

The idea of the algorithm comes from the associative property of LCP operation. We notice that: 
LCP(S1 ... Sn) = LCP(LCP(S1 ... Sk), LCP(Sk+1 ... Sn)), where LCP(S1 ... Sn) is the longest common
prefix in a set of strings [S1 ... Sn], 1<k<n 

<br><br>
*Algorithm* 

To apply the previous observation, we use the divide and conquer technique, where we split the 
LCP(Si ... Sj) problem into two subproblems LCP(Si ... Smid) and LCP(Smid+1 ... Sj), where mid is 
(i+j)/2. We use their solutions lcpLeft and lcpRight to construct the solution of the main problem 
LCP(Si ... Sj). To accomplish this we compare one by one the characters of lcpLeft and lcpRight till 
there is no character match. The found common prefix of lcpLeft and lcpRight is the solution of the 
LCP(Si ... Sj) 


```
				{leetcode, leet, lee, le} 

				    /                \   
Divide 			{leetcode, leet}            {lee, le} 

Conquer				|			 | 

			     {leet} 		        {le} 

			         \                      /

				 	   {le} 

	Searching for the longest common prefix (LCP) in dataset {leetcode, leet, lee, le} 
```

```java
public String longestCommonPrefix(String[] strs) { 

	if (strs == null || strs.length ==0) return "";
		return longestCommonPrefix(strs, 0, strs.length-1); 

}

private String longestCommonPrefix(String[] strs, int l, int r) { 
	if (l==r) {
		return strs[l];
	}
	else {
		int mid=(l+r)/2; 
		String lcpLeft= longestCommonPrefix(strs,l, mid); 
		String lcpRight= longestCommonPrefix(strs,mid+1;r); 
		return commonPrefix(lcpLeft,lcpRight);
	}
}

String commonPrefix(String left, String right) {
	int min=Math.min(left.length(), right.length()); 
	for (int i=0; i<min; i++) {
		if (left.charAt(i) !=right.charAt(i) ){
			return left.substring(0, i);
		}
	}
	return left.substring(0, min);
}
```

**Complexity Analysis**

In the worst case we have n equal strings with length m

```
Time Complexity: O(S)		where S is the number of all characters in the array, S=m*n so time
				complexity is 2*T(n/2)+O(m). Therefore time complexity is O(S). In the
				best case the algorithm performs O(minLen * n) comparisons, where
				minLen is the shortest string of the array 

Space Complexity: O(m*log(n))	There is a memory overhead since we sotre recursive call in the 
				execution stack. There are log(n) recursive calls, each store needs m
				space to store the result so space complexity is O(m*log(n))
```

<br><br>
<a name="longestCommonPrefixBinarySearch"></a>
## Binary Search

The idea is to apply binary search method to find the string with maximum value L, which is common 
prefix of all the strings. The algorithm searches the space in the interval (0 ... minLen), where 
minLen is minimum string length and the maximum possible common prefix. Each time search space is 
divided in two equal parts, one of them is discarded because it is sure that it doesn't contain the 
solution. There are two possible cases: 

* S[1...mid] is not a common string. This means that for each j>i, S[1...j] is not a common string and we discard the second half of the search space
* S [1...mid] is common string. This means that for each i<j, S[1...i] is a common string and we discard the first half of the search space, because we try to find longer common prefix 

```
 				{leets, leetcode, leetc, leeds} 

						|
					      
					     "leets"
					    /        \
					 "lee"      "ts"

					     midpoint 
				
				"lee" in "leetcode" : yes
				"lee" in "leetc" : yes
				"lee" in "leeds" : yes

						|

					     "leets"
					     /     \
					  "lee"    "ts"
					    |      /   \

					  "lee"   "t"   "s"
					        
						   midpoint


						   "leet" in "leetcode" : yes
						   "leet" in "leetc" : yes 
						   "leet" in "leeds" : no

						   LCP= "lee" 
```

```java
public String longestCommonPrefix(String[] strs) {
	if (strs==null || strs.length==0)
		return "";
	int minLen=Integer.MAX_VALUE; 
	for (String str: strs)
		minLen=Math.min(minLen, str.length());
	int low=1; 
	int high=min Len; 
	while (low<=high) {
		int middle=(low+high)/2;
		if (isCommonPrefix(strs, middle)
			low=middle+1;
		else 
			high=middle-1;
	}
	return strs[0].substring(0, (low + high)/2);
} 

private boolean isCommonPrefix(String[] strs, int len) {
	String str1=strs[0].substring(0,len);
	for (int i=1; i<strs.length; i++)
		if (!strs[i].startsWith(str1))
			return false;
	return true;
}
```

**Complexity Analysis

In the worst case we have n equal strings with length m 

```
	Time complexity: 	O(S * log(n)), where S is the sum of all characters in all strings. The
				algorithm makes log(n) iterations, for each of them there are S=m*n 
				comparisons, which gives in total O(S * log(n)) time complexity

	Space complexity: 	O(1). We only used constant extra space 
```
<br><br>
<a name="longestCommonPrefixFurtherThoughts"></a>
## Further Thoughts 

Considering a slightly different problem: 
```
	Given a set of keys S= [S1, S2 ... Sn], find the longest common prefix among a string q and S.
	This LCP query will be called frequently
```
We coule optimize LCP queries by storing the set of keys S in a Trie. See this for [Trie 
implementation](#trie). In a Trie, each node descending from the root represents a common prefix of some keys. But we need to 
find the longest common prefix of a string q and all key strings. This means that we have to find the
deepest path from the root, which satisfies the following conditions 

* it is a prefix of query string q
* each node along the path must contain only one child element. Otherwise the found path will not be a
  common prefix among all strings
* the path doesn't comprise of nodes which are marked as end of key. Otherwise the path couldn't be a
  prefix of a key which is shorter than itself

<br><br>
*Algorithm* 

The only question left is how to find the deepest path in the Trie, that fulfills the requirements 
above. The most effective way is to build a trie from {S1 ... Sn] strings. Then find the prefix of 
query string q in the Trie. We traverse the Trie from the root, till it is impossible to continue the
path in the Trie because one of the conditions above is not satisfied. 


```
Searching for the longest common prefix of string "le" in a Trie from dataset {lead, leet}

			Root

			 1

	l   ===========>  \  l

			     2

	e   ===============>   \ e

LCP "le" FOUND	=============>   3   

			     a	/  \ e    End of Key "lee" 
				     
			      6      4

			 d  /	       \ t
				        
END OF KEY "lead"	  7		 5   End of key "leet"
```



```
public String longestCommonPrefix(String q, String[] strs) {
    if (strs == null || strs.length == 0)
         return "";  
    if (strs.length == 1)
         return strs[0];
    Trie trie = new Trie();      
    for (int i = 1; i < strs.length ; i++) {
        trie.insert(strs[i]);
    }
    return trie.searchLongestPrefix(q);
}

class TrieNode {

    // R links to node children
    private TrieNode[] links;

    private final int R = 26;

    private boolean isEnd;

    // number of children non null links
    private int size;    
    public void put(char ch, TrieNode node) {
        links[ch -'a'] = node;
        size++;
    }

    public int getLinks() {
        return size;
    }
    //assume methods containsKey, isEnd, get, put are implemented as it is described
   //in  https://leetcode.com/articles/implement-trie-prefix-tree/)
}

public class Trie {

    private TrieNode root;

    public Trie() {
        root = new TrieNode();
    }

//assume methods insert, search, searchPrefix are implemented
    private String searchLongestPrefix(String word) {
        TrieNode node = root;
        StringBuilder prefix = new StringBuilder();
        for (int i = 0; i < word.length(); i++) {
            char curLetter = word.charAt(i);
            if (node.containsKey(curLetter) && (node.getLinks() == 1) && (!node.isEnd())) {
                prefix.append(curLetter);
                node = node.get(curLetter);
            }
            else
                return prefix.toString();

         }
         return prefix.toString();
    }
}
```

**Complexity Analysis**
```
In the worst case query q has length m and is equal to all n strings of the array 

Time Complexity:   O(S)   where S is the number of all characters in the array, LCP query O(m) 
  			  Trie build has O(S) time complexity. To find the common prefix of q 
			  in the Trie takes in the worst O(m). 

Space complexity:  O(S)   we only used additional S extra space for the Trie. 
```


<br><br><br>
***
<a name="threeSum"></a>
# 15-3Sum


Given an array "nums" of n integers, are there elements a, b, c in nums such that a+b+c=0? Find all 
unique triplets in the array which gives the sum of zero. 

Note: 

The solution set must not contain duplicate triplets 

```
Example: 

Given array nums = [-1, 0, 1, 2, -1, -4]. 

A solution set is: 
[
  [-1, 0, 1],
  [-1, -1, 2]
]
```
<br><br>
<a name="threeSumSortedArray"></a>
## Sorted Array


The method is to sort an input array and then run through all indices of a possible first element of a
triplet. For each element we make another 2Sum sweep of the remaining part of the array. Also we want
to skip elements to avoid duplicates in the answer without expending extra memory. 

```
public List<List<Integer>> threeSum(int[] num) {
    
    //Arrays.sort re-arranges the array of integers in ascending order
    //ex. [1, 2, 3, 4]

    Arrays.sort(num);
    List<List<Integer>> res = new LinkedList<>(); 
    for (int i = 0; i < num.length-2; i++) {
        if (i == 0 || (i > 0 && num[i] != num[i-1])) {
            
	    //This lets us skip some of the duplicate entries in the array
	    
	    int lo = i+1, hi = num.length-1, sum = 0 - num[i];

	    //This is for the 2 Sum sweep 

            while (lo < hi) {
                if (num[lo] + num[hi] == sum) {
                    res.add(Arrays.asList(num[i], num[lo], num[hi]));
                    while (lo < hi && num[lo] == num[lo+1]) lo++;
                    while (lo < hi && num[hi] == num[hi-1]) hi--;

		    //This lets us skip some of the duplicate entries in the array

                    lo++; hi--;
                } else if (num[lo] + num[hi] < sum) lo++;
                else hi--;

		//This allows us to optimize slightly since we know that the array is sorted
           }
        }
    }
    return res;
}
```

**Complexity Analysis**
```
Time Complexity:  O(n^2)   We go through a maximum of n elements for the first element of a triplet, 
			   and then when making a bi-directional 2Sum sweep of the remaining part of 
			   the array we also go through a maxiumum of n elements. 

Space Complexity: O(1)	   If we assume the return linked list is not extra space, then we do not 
			   allocate any significant extra space
```



<br><br><br>
***
<a name="threeSumClosest"></a>
# 16-3Sum Closest

Given an array nums of n integers and an integer target, find three integers in nums such that the sum
is closest to target. Return the sum of the three integers. You may assume that each input would have
exactly one solution. 

```
Example:

Given array nums=[-1, 2, 1, -4], and target=1.

The sum that is closest to the target is 2. (-1+2+1=2)
```

<br><br>
<a name="threeSumClosestThreePointers"></a>
## 3 Pointers

Similar to the previous 3Sum problem, we use three pointers to point to the current element, next 
element and the last element. If the sum is less than the target, it means that we need to add a larger
element so next element move to the next. If the sum is greater, it means we have to add a smaller 
element so last element move to the second last element. Keep doing this until the end. Each time 
compare the difference between sum and target, if it is less than minimum difference so far, then 
replace result with it, otherwise continue iterating. 

```
public class Solution {
		public int threeSumClosest(int[] num, int target) {
		int result=num[0] + num[1] + num[num.length-1];
		Arrays.sort(num);
		for (int i=0; i<num.length -2; i++) {
			int start= i+1, end = num.length -1;
			while (start < end) {
				int sum = num[i] + num[start] + num[end];
				if (sum > target) {
					end--;
				} else {
					start++;
				}
				if (Math.abs(sum-target) < Math.abs(result-target)) {
					result=sum;
				}
			}
		}
		return result;
	}
}
```


<br><br><br>
***
<a name="letterCombinationsofaPhoneNumber"></a>
# 17-Letter Combinations of a Phone Number 

Given a string contianing digits from 2-9 inclusive, return all possible letter combinations that the 
number could represent. 

A mapping of digit to letters (just like on the telephone buttons) is given below. Note that 1 does not
map to any letters. 

```
2 - abc 	3 - def 	4 - ghi		5 - jkl		6 - mno		7 - pqrs 	8 - tuv
				
						9 - wxyz
```


```
Example: 


Input: "23" 

Output: ["ad", "ae", "af", "bd", "be", "bf", "cd", "ce", "cf"]. 
```


*Note: The above answer is in lexicographical order but the answer can be in any order*

<br><br>
<a name="letterCombinationsofaPhoneNumberBacktracking"></a>
## Backtracking 


Backtracking is an algorithm for finding all solutions by exploring all potential candidates. If the 
solution candidate turns to not be a solution (or at least not the last one), backtracking algorithm 
discards it by making some changes on the previous step, ie *backtracks* and then tries again. 

Here is a backtrack function backtrack(combination, next_digits) which takes as arguments an ongoing 
letter combination and the next digits to check. 

* If there are no more digits to check that means the current combination is done 
* If there are still digits to check: 
	* Iterate over the letters mapping to the next available digit
	* Append the current letter to the current combination and proceed to check next digits: 


```
	  combination = combination + letter

	  backtrack(combination + letter, next_digits[1:]).
```


**Visual Representation** 

```
					
						"2 3"

						 
						  2
						
					      /   |   \
                                            
					     a    b    c
                                       

				         /        |        \

                                       
				      3           3            3

				    / | \       / | \        / | \

				   d  e  f     d  e  f      d  e  f

				
			["ad", "ae", "af", "bd", "be", "bf", "cd", "ce", "cf"]
```

```java 
class Solution {
	Map<String, String> phone = new HashMap<String, String>() {{
		put("2", "abc"); 
		put("3", "def");
		put("4", "ghi");
		put("5", "jkl"); 
		put("6", "mno");
		put("7", "pqrs");
		put("8", "tuv");
		put("9", "wxyz");
	}}; 

	List<String> output = new ArrayList<String>(); 

	public void backtrack(String combination, String next_digits) {
		
		
		//if there are no more digits to check 
		if (next_digits.length()==0) {
			
			//the combination is done 
			output.add(combination);
		}

		

		//if there are still digits to check 
		else { 
		
			//iterate over all letters which map the next available digit 
			String digit = next_digits.substring(0,1); 
			String letters = phone.get(digit);
			for (int i=0; i<letters.length(); i++) {
				String letter = phone.get(digit).substring(i, i+1);
				//append the current letter to the combination and proceed to next
				backtrack(combination + letter, next_digits.substring(1));
			}
		}

	}

	public List<String> letterCombinations(String digits) { 
		if (digits.length() !=0) {
			backtrack("", digits);
		}
		return output;
	}
}
```

**Complexity Analysis** 

```

Time Complexity: 	O(3^N * 4^M) 	where N is the number of digits in the input that maps to 3
					letters (eg. 2, 3, 4, 5, 6, 8) and M is the number of digits 
					in the input that maps to 4 letters (eg. 7, 9) and N+M is the 
					total number digits in the input 

Space Complexity: 	O(3^N * 4^M)	since one has to keep 3^N * 4^M solutions 
```



<br><br>
<a name="letterCombinationsofaPhoneNumberFIFOQueue"></a>
## First In First Out (FIFO) Queue 

This solution utilizes the Single Queue Breadth First Search (BFS) which is an algorithm for traversing
or searching tree or graph data structures. It starts at the tree root and explores all of the neighbor
nodes. 


```java 
public List<String> letterCombinations(String digits) {
	
	LinkedList<String> ans = new LinkedList<String>();
	if (digits.isEmpty()) return ans; 
	String[] mapping = new String[] {"0", "1", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tuv", {wxyz"};
	ans.add(""); 
	for (int i = 0; i<digits.length(); i++) {
		int x = Character.getNumericValue(digits.charAt(i)); 
		
		//we terminate the while loop when we encounter a new-formed string which is more than
		//the current level i 
		
		//peek retrieves the first value of the linked list
		while (ans.peek().length==i){
			
			//removes the head or the first value in the linkedlist
			String t = ans.remove(); 
			for (char s : mapping[x].toCharArray()) {
				ans.add(t+s);
				//this works because add appends to the end of the list
			}
		}
		return ans; 
	}
}
```

**Complexity Analysis**

```

Time Complexity: 	O(3^N * 4^M) 	where N is the number of digits in the input that maps to 3
					letters (eg. 2, 3, 4, 5, 6, 8) and M is the number of digits 
					in the input that maps to 4 letters (eg. 7, 9) and N+M is the 
					total number digits in the input 

Space Complexity: 	O(3^N * 4^M)	since one has to keep 3^N * 4^M solutions 
```

<br><br><br>
***
<a name="fourSum"></a>
# 18-4Sum

Given an array nums of n integers and an integer target, are there elements a, b, c, and d in nums such
that a + b + c + d = target? Find all unique quadruplets in the array which gives the sum of target



*Note:*
The solution set must not contain duplicate quadruplets 


```
Example: 


Given array nums = [1, 0, -1, 0, -2, 2], and target = 0


A solution set is: 

[
  [-1,  0, 0, 1],
  [-2, -1, 1, 2],
  [-2,  0, 0, 2]
]
```


<br><br>
<a name="fourSumSortedArray"></a>
## Sorted Array  

The idea is the same as the other numbered sum problems like 2sum and 3sum. We sort the array and then
proceed to interate through the values until we end up with a result that we are looking for. 

```java 
public class Solution {
	public List<List<Integer>> fourSum(int[] num, int target) {
		
		ArrayList<List<Integer>> ans = new ArrayList<>();
		
		if (num.length<4) {
			
			return ans;
		}
		Arrays.sort(num); 
		
		for (int i=0; i<num.length-3; i++) {   //picking the first candidate must leave room
						       //for the other values 
			
			if (num[i]+num[i+1]+num[i+2]+num[i+3]>target) {
				
				break;
				//first candidate too large, search finished
			}

			if (num[i]+num[num.length-1]+num[num.length-2]+num[num.length-3]<target) {
				
				continue;
				//first candidate too small 
			}

			if(i>0 && num[i]==num[i-1]) {
				
				continue;
				//prevents duplicate in ans list
			}
			
			for (int j=i+1; j<num.length-2; j++) {   //picking the second candidate must
								 //leave room for other values 
				
				if (num[i]+num[j]+num[j+1]+num[j+2]>target) {
					
					break;
					//second candidate too large
				}

				if (num[i]+num[j]+num[num.length-1]+num[num.length-2]<target) {
				
					continue;
					//second candidate too small
				}

				if(j>i+1 && num[j]==num[j-1]) {
					
					continue;
					//prevents duplicate results in ans list
				}

				int low=j+1, high=num.length-1;
				
				//two pointer search
				while(low<high) {
					
					int sum=num[i]+num[j]+num[low]+num[high];
					if (sum==target) {
						
						ans.add(Arrays.asList(num[i],num[j],num[low],num[high]));
						while(low<high&&num[low]==num[low+1]) {
							low++; //skipping over duplicates
						}

						while(low<high && num[high]==num[high-1] {
							high--; //skipping over duplicates 
						}
						low++;
						high--;
					}

					//moving window
					else if (sum<target) {
						low++;
					}

					else {
						high--;
					}
				}
			}
		}
		return ans;
	}
}
```






<br><br><br>
***
<a name="removeNthNodefromEndofList"></a>
# 19-Remove Nth Node From End of List 

Given a linked list, remove the n-th node from the end of the list and return its head

```
Example: 

Given linked list: 1 -> 2 -> 3 -> 4 -> 5, and n=2 


After removing the second node from the end, the linked list becomes 
		   
		   1 -> 2 -> 3 -> 5
```

**Note:**
Given n will always be valid 

**Follow up:**
Could you do this in one pass? 









<br><br>
<a name="removeNthNodefromEndofListTwoPassAlgorithm"></a>
## Two Pass Algorithm


**Intuition**

We notice that the problem could be simply reduced to another one: Remove the (L-n+1)th node from the
beginning of the list, where L is the list length. This problem is easy to solve once we found the 
list length L. 





<br><br>
**Algorithm** 

First we will add an auxiliary "dummy" node, which points to the list head. The "dummy" node is used to
simplify some corner cases such as a list with only one node or removing the head of the list. On the 
first pass, find the list length L. Then we set a pointer to the dummy node and start to move it 
through the list till it comes to the (L-n)th node. We relink next pointer of the (L-n)th node to the
(L-n+2)th node and we are done. 


```
	D -> 1 -> 2 -> 3 -> 4 -> NULL

		    |
		    v

	D -> 1 -> 2 -> 4 -> NULL
```



```java 
public ListNode removeNthFromEnd(ListNode head, int n) {
	
	ListNode dummy = new ListNode(0); 
	dummy.next = head; 
	int length =0; 
	ListNode first = head; 
	
	while (first!=null) {
		
		length++;
		first=first.next;
	}

	length -= n; 
	first = dummy;
	while (length>0) {
		
		length--;
		first=first.next;
	}
	first.next=first.next.next;
	return dummy.next; 
}
```

**Complexity Analysis** 
```
Time Complexity: 	O(L) 	The algorithm makes two traversals of the list, first to calculate the 
				list length L and second to find the (L-n)th node. There are 2L-n 
				operations and time complexity is O(L)

Space Complexity: 	O(1) 	We only used constant extra space
```





<br><br>
<a name="removeNthNodefromEndofListOnePassAlgorithm"></a>
## One Pass Algorithm

The previous algorithm could be optimized to one pass. Instead of one pointer, we could use two 
pointers. The first pointer advances the list by n+1 steps from the beginning, while the second pointer
starts from the beginning of the list. Now, both pointers are separated by exactly n nodes. We maintain
this constant gap by advancing both pointers together until the first pointer arrives past the last 
node. The second pointer will be pointing at the nth node counting from the last. We relink the next
pointer of the node referenced by the second pointer to point to the node's next next node. 



```
Maintaining N=2 nodes apart between the first and second pointer 

	D	-> 1 -> 2 -> 3 -> 4 -> 5 -> NULL

       first 	 Head 
       second 

			   


Move the first pointer N+1 steps 


			     |
			     v


	D	-> 1 -> 2 -> 3 -> 4 -> 5 -> NULL

      second     Head       First


Move the first and second pointers together until the first pointer arrives past the last node 


			     |
			     v


	D	-> 1 -> 2 -> 3 -> 4 -> 5 -> NULL
		
		 Head      Second           First

Second pointer points to the nth node counting from last so link node to the node's next next node 



				  |
				  v


	D	-> 1 -> 2 -> 3 ->   -> 5 -> NULL
	         
		 Head      Second           First
```


```java 
public ListNode removeNthFromEnd(ListNode head, int n) {
	
	ListNode dummy = new ListNode(0);
	dummy.next = head; 
	ListNode first = dummy; 
	ListNode second = dummy;
	
	//Moves the first pointer so that the first and second nodes are separated by n nodes
	
	for (int i=1; i<=n+1; i++) {
		
		first = first.next;
	}

	//Move first to the end, maintaining the gap

	while (first!=null) {

		first=first.next;
		second=second.next;
	}

	second.next=second.next.next;
	return dummy.next;
}
```



**Complexity Analysis** 

```
Time Complexity: 	O(L) 	The algorithm makes one traversal of the list of L nodes. Therefore
				time complexity is O(L)

Space Complexity: 	O(1)	Only constant extra space was used 
```







<br><br><br>
***
<a name="validParentheses"></a>
# 20-Valid Parentheses



Given a string containing just the characters '(', ')', '{', '}', '[', ']', determine if the input 
string is valid 

An input string is valid if: 

1. Open brackets must be closed by the same type of brackets 
2. Open brackets must be closed in the correct order 

Note that an empty string is also considered valid


```
Example 1: 

Input: "()"
Output: true
```


```
Example 2: 

Input: "()[]{}"
Output: true 
```


```
Example 3: 

Input: "(]"
Output: false
```


```
Example 4: 

Input: "([)]"
Output: false
```


```
Example 5: 

Input: "{[]}"
Output: true
```






<br><br>
<a name="validParenthesesCounting"></a>
## Counting method



**Intuition** 

Imagine you are writing a small compiler for your college project and one of the tasks or sub-tasks for
the compiler would be to detect if the parenthesis are in place or not. 



The algorithm we will look at in this article can be then used to process all the parenthesis in the 
program your compiler is compiling and checking if all the parenthesis are in place. This makes 
checking if a given string of parenthesis is valid or not, an important programming problem. 



The expressions that we will deal with in this problem can consist of three different types of 
parenthesis: 


- () 
- {}
- []


Before looking at how we can check if a given expression consisting of thes parenthesis is valid or 
not, let us look at a simpler version of the problem that consists of just one type of parenthesis. So,
the expressions we can encounter in this simplified version of the problem are: 


```
(((((()))))) -- VALID

()()()()     -- VALID

(((((((()    -- INVALID

((()(())))   -- VALID
```


Let's look at a simple algorithm to deal with this problem 

<br><br>

1. We process the expression one bracket at a time starting from the left 
2. Suppose we encounter an opening bracket ie. `(`, it may or may not be an invalid expression because
   there can be a matching ending bracket somewhere in the remaining part of the expression. Here, we 
   simply increment the counter keeping track of the left parenthesis till now. `left += 1`
3. If we encounter a closing bracket, this has two meanings: 
   
   - There was no matching opening bracket for this closing bracket and in that case we have an invalid
     expression. This is the case when `left==0` ie. when there are no unmatched left brackets 
     available
   
   - We had some unmatched opening bracket available to match this closing bracket. This is the case 
     when `left>0` ie. we have unmatched left brackets available 

4. If we encounter a closing bracket ie. `)` when left==0, then we have an invalid expression on our 
   hands. Else, we decrement `left` thus reducing the number of unmatched left parenthesis available.
5. Continue processing the string until all parenthesis have been processed
6. If in the end we still have an unmatched left parenthesis available, this implies an invalid 
   expression 

<br><br>

The reason we discussed this particular algorithm here is because the approach for the approach for 
the original problem derives its inspiration from this very solution. 


If we try and follow the same approach for our original problem, then it simply won't work. The reason
a simple counter based approach works above is because all the parenthesis are of the same type. So 
when we encounter a closing bracket, we simply assume a corresponding opening matching bracket 
to be available ie. if `left>0`


But in our problem, if we encounter say `]`, we don't really know if there is a corresponding opening
`[` available or not. You could say: 

> Why not maintain a separate counter for the different types of parenthesis?

This doesn't work because the relative placement of the parenthesis also matters here eg: `[{]`

<br><br> 

If we simply keep counters here, then as soon as we encounter the closing square bracket, we would 
know there is an unmatched opening square bracket available as well. But, the **closest unmatched 
opening bracket available is a curly bracket and not a square bracket and hence the counting approach
breaks here. 







<br><br>
<a name="validParenthesesStack"></a>
## Stacks 

An interesting property about a valid parenthesis expression is that a sub-expression. (Not every 
sub-expression) eg. 

```
	{ [ [ ] { } ] } ( ) ( ) 

	  ^         ^
	  |         |
```

The entire expression is valid, but sub portions of it are also valid in themselves. This lends a sort 
of a recursive structure to the problem. For example consider the expression enclosed within the 
marked parenthesis in the diagram above. The opening bracket is at index `1` and the corresponding 
closing bracket is at index `6`. 


> What if whenever we encounter a matching pair of parenthesis in the expression we simply remove it
> from the expression? 


Let's have a look at this idea below where we remove the smaller expressions one at a time from the 
overall expression and since this is a valid expression, we would be left with an empty string in the
end. 


```
The stack data structure can come in handy here in representing this recursive structure of the 
problem. We can't really process this from the inside out because we don't have an idea about the 
overall structure. But, the stack can help us process this recursively ie. from outside to inwards.
```

Lets take a look at the algorithm for this problem using stacks as the intermediate data structure. 


**Algorithm** 

1. Initialize a stack S. 
2. Process each bracket of the expression one at a time 
3. If we encounter an opening bracket, we simply push it onto the stack. This means we will process it
   later, let us simply move onto the sub-expression ahead 
4. If encounter a closing bracket, then we check the element on top of the stack. If the element at the
   top of the stack is an opening bracket `of the same type`, then we pop it off the stack and continue
   processing. Else, this implies an invalid expression 
5. In the end, if we are left with a stack still having elements, then this implies an invalid 
   expression

Lets take a look at the implementation for this algorithm



```java 
class Solution {
	
	//Hash table that takes care of the mappings
	private HashMap<Character, Character> mappings; 

	//Initialize the hash map with mappings. This simply makes the code easier to read 
	public Solution() {
		
		this.mappings = new HashMap<Character, Character>(); 
		this.mappings.put(')', '(');
		this.mappings.put('}', '{');
		this.mappings.put(']', '[');
	}

	public boolean isValid(String s) { 
		
		// Initialize a stack to be used in the algorithm
		Stack<Character> stack = new Stack<Character>();

		for (int i=0; i< s.length(); i++) {
			
			char c = s.charAt(i);

			// If the current character is a closing bracket 

			if (this.mappings.containsKey(c)) {
				
				// Get the top element of the stack. If the stack is empty, set a dummy value of '#' 
				char topElement = stack.empty() ? '#' : stack.pop();

				// If the mapping for this bracket doesn't match the stack's top element, return false. 
				if (topElement != this.mappings.get(c)) {
					return false;
				}
			} else {
				
				//If it was an opening bracket, push to the stack  
				
				stack.push(c);
			}
		}

		//If the stack still contains elements, then it is an invalid expression. 
		return stack.isEmpty();
	}
}
```

**Complexity Analysis**

```
Time Complexity: 	O(n)	We simply traverse the given string one character at a time and push 
				and pop operations on a stack take O(1) time 

Space Complexity: 	O(n)	In the worst case, when we push all opening brackets onto the stack, we
				will end up pushing all the brackets onto the stack eg (((((((((((
```


<br><br><br>
***
<a name="mergeTwoSortedLists"></a>
# 21-Merge Two Sorted Lists

Merge two sorted linked lists and return it as a new list. The new list should be made by splicing 
together the nodes of the first two lists. 


```
Example: 

Input: 1->2->4, 1->3->4
Output: 1->1->2->3->4->4
```



<br><br>
<a name="mergeTwoSortedListsRecursive"></a>
## Recursive 

```java 
class solution {
	public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
		
		if (l1 == null) return l2; 
		if (l2 == null) return l1;
		if (l1.val < l2.val) {
			
			l1.next = mergeTwoLists(l1.next, l2);
			return l1;
		} else {
			
			l2.next = mergeTwoLists(l1, l2.next);
			return l2;
		}
	}	
}
```


<br><br>
<a name="mergeTwoSortedListsNonRecursive"></a>
## Non-Recursive 

Similar approach and implemenation to the recursive solution above but a little more intuitive and 
does not require memory being held on the stack (as the recursive program runs it has to store 
variables on the stack so that when the program jumps back it is able to continue) 


As with most other linked list solutions, a dummy node is utilized and two pointers are used to keep
track of where we are in the the two linked lists. 

```java 
class solution {
	public ListNode mergeTwoLists(ListNode l1, ListNode l2) {
		
		ListNode returnNode = new ListNode(-1); 
		ListNode headNode = returnNode; 
		
		while (l1 != null && l2 != null) {
			if (l1.val <= l2.val) {
				returnNode.next = l1;
				l1 = l1.next;
			} else {
				returnNode.next = l2;
				l2 = l2.next; 
			}
			returnNode = returnNode.next;
		}

		if (l1 == null) {
			returnNode.next = l2;
		} else if (l2 == null) {
			returnNode.next = l1; 
		}

		return headNode.next; 
	}
}
```





<br><br><br>
***
<a name="generateParentheses"></a>
# 22-Generate Parentheses

Given n pairs of parentheses, write a function to generate all combinations of well-formed parentheses.


```
For example: 

Given n=3, a solution set is: 

[
  "((()))",
  "(()())".
  "(())()",
  "()(())",
  "()()()"
]
```


<br><br>
<a name="generateParenthesesBruteForce"></a>
## Brute Force 

**Intuition** 

We can generate all 2^(2n) sequences of `(` and `)` characters. Then we can check if each one is valid

<br>

**Algorithm** 

To generate all sequences, we use recursion. All sequences of length `n` is just `(` plus all sequences
of length `n-1`, and then `)` plus all sequences of length `n-1`. 

To check whether a sequence is valid, we keep track of `balance`, the net number of opening brackets 
minuts closing brackets. If it falls below zero at any time, or doesn't end in zero, the sequence is 
invalid - otherwise it is valid. 


```java 
class Solution {
	
	public List<String> generateParenthesis(int n) {
		
		List<String> combinations = new ArrayList(); 
		generateAll(new char[2*n], 0, combinations);
		return combinations;
	}

	public void generateAll(char[] current, int pos, List<String> result) {
		
		if(pos == current.length) {
			
			if (valid(current)) {
				result.add(new String(current));
			} 

		} else {
			current[pos] = '(';
			generateAll(current, pos+1, result);
			current[pos] = ')';
			generateAll(current, pos+1, result);
		
		}
	}

	public boolean valid(char[] current) {
		
		int balance = 0; 
		for (char c : current) {
			
			if(c == '(') {
				balance++;
			} else {
				balance--;
			}

			if(balance < 0) {
				return false; 
			}
		}
		return (balance == 0);
	}
}
```

**Complexity Analysis**

```
Time Complexity: 	O(2^2n * n)	For each of 2^2n sequences, we need to create an validate the 
					sequence, which takes O(n) work in the worst case 

Space Complexity: 	O(2^2n * n) 	Naively, every sequence could be valid, see Closure number for
					a tighter asymptotic bound 
```




<br><br>
<a name="generateParenthesesBacktracking"></a>
## Backtracking


**Intuition and Algorithm** 

Instead of adding `(` or `)` every time as we do in the Brute Force algorithm, let's only add them 
when we know it will remain a valid sequence. We can do this by keeping track of the number of opening
and closing brackets we have placed so far. 

We can start an opening bracket if we still have one (of `n`) left to place. And we can start a closing
bracket if it would not exceed the number of opening brackets 


```java 
class Solution {
	
	public List<String> generateParenthesis(int n) {
		
		List<String> ans = new ArrayList(); 
		backtrack(ans, "", 0, 0, n);
		return ans; 
	}

	public void backtrack(List<String> ans, String cur, int open, int close, int max){
		
		if (cur.length() == max*2) {
			ans.add(cur);
			return;
		}

		if(open < max) {
			backtrack(ans, cur + "(", open + 1, close, max);
		} 
		
		if (close < open) {
			backtrack(ans, cur + ")", open, close +1, max);
		}
	}
}
```

**Complexity Analysis** 

Our complexity analysis rests on understanding how many elements there are in `generateParenthesis(n)`.
This analysis is outside the scope of this article, but it turns out this is the nth Catalan number 
1/(n+1) (2n choose n), which is bounded asymptotically by 4^n/(n* sqrt(n)). 

```
Time Complexity: 	O((4^n)/sqrt(n))	Each valid sequence has at most n steps during the 
						backtracking procedure

Space Complexity: 	O((4^n)/sqrt(n))	As described above and using O(n) space to store the
						sequence
```

Another way to think about the runtime of backtracking algorithms on interviewers is O(b^d), where b is
the branching factor and d is the maximum depth of recursion. 

Backtracking is characterized by a number of decisions b that can be made at each level of recursion. 
If you visualize the recursion tree, this is the number of children each internal node has. You can
also think of b as standing for "base", which helps us remember that b is the base of the exponential.

If we make b decisions at each level of recursion, and we expand the recursion tree to d levels (ie. 
each path has a length of d), then we get b^d nodes. Since backtracking is exhaustive and must visit 
each of these nodes, the runtime is O(b^d)








<br><br>
<a name="generateParenthesesClosureNumber"></a>
## Closure Number



To enumerate something, generally we would like to express it as a sum of disjoint subsets that are 
easier to count. 


Consider the *closure number* of a valid parentheses sequence `s`: the least `index >= 0` so that 
`S[0], S[1], ... , S[2 * index + 1] is valid. Clearly, every parentheses sequence has a unique closure
number. We can try to enumerate them individually. 


<br><br>

**Algorithm** 

For each closure number c, we know the starting and ending brackets must be at index `0` and 
`2 * c + 1`. Then, the `2 * c` elements between must be a valid sequence, plus the rest of the elements
must be a valid sequence.



This is just some minor improvement to the backtracking solution using the fact that for all valid 
solutions the first char is always '(' and the lat char is always ')'. We initialize the starting 
string to '(' and set the recursion bottom condition to string reaching length of `2 * n - 1` - we know
that we need to append a bracket at the end. There will not be much of an improvement in the runtime
however. 


```java 
class Solution {
	public List<String> generateParenthesis(int n) {
		List<String> ans = new ArrayList(); 
		if (n==0) {
			ans.add("");
		} else {
			for (int c=0; c<n; ++c)
				for (String left: generateParenthesis(c))
					for (String right: generateParenthesis(n-1-c))
						ans.add("(" + left + ")" + right);
		}
		return ans;
	}
}
```

**Complexity Analysis** 
```
Time Complexity: 	O((4^n)/sqrt(n))

Space Complexity: 	O((4^n)/sqrt(n))
```













<br><br><br>
***
<a name="mergeKSortedLists"></a>
# 23-Merge k Sorted Lists 

Merge k sorted linked lists and return it as one sorted list. Analyze and descibe its complexity: 


```
Example: 

Input: 
[
	1 -> 4 -> 5,
	1 -> 3 -> 4,
	2 -> 6
]

Output: 1 -> 1 -> 2 -> 3 -> 4 -> 4 -> 5 -> 6
```





<br><br>
<a name="mergeKSortedLists"></a>
## Brute Force 


**Intuition and Algorithm** 

* Traverse all the linked lists and collect the values of the nodes into an array
* Sort and iterate over this array to get the proper value of nodes
* Create a new sorted linked list and extend it with the new nodes 

As for sorting you can refer to the Algorithms/Data Structures CheatSheet for more about sorting algorithms. 





<br><br><br>
***
<a name="lruCache"></a>
# 146-LRU Cache 

Design and implement a data structure for Least Recently Used (LRU) cache. It should support the following operations: `get` and `put`. 

`get(key)` - Get the value (will always be positive) of the key if the key exists in the cache, otherwise return `-1` 

`put(key, value)` - Set or insert the value if the key is not already present. When the cache reached its capacity, it should invalidate the least recently used item before inserting a new item. 

**Follow up:**
Could both of these operations be done in **O(1)** time complexity?

**Example:**
```
LRUCache cache = new LRUCache(2 /* capacity */);

cache.put(1, 1);
cache.put(2, 2);
cache.get(1); 			// returns 1 
cache.put(3, 3); 		// evicts key 2
cache.get(2);			// returns -1 (not found)
	
```



Python3 reference for interview coding problems/light competitive programming. Contributions welcome!

## How

I built this cheatsheet while teaching myself Python3 for various interviews and leetcoding for fun after not using Python for about a decade. This cheetsheet only contains code that I didn't know but needed to use to solve a specific coding problem. I did this to try to get a smaller high frequency subset of Python vs a comprehensive list of all methods. Additionally, the act of recording the syntax and algorithms helped me store it in memory and as a result I almost never actually referenced this sheet. Hopefully it helps you in your efforts or inspires you to build your own and best of luck!


## Why

The [rule of least power](https://en.wikipedia.org/wiki/Rule_of_least_power)

I choose Python3 despite being more familiar with Javascript, Java, C++ and Golang for interviews as I felt Python had the combination of the most standard libraries available as well as syntax that resembles psuedo code, therefore being the most expressive. Python and Java both have the most examples but Python wins in this case due to being much more concise. I was able to get myself reasonably prepared with Python syntax in six weeks of practice. After picking up Python I have timed myself solving the same exercises in Golang and Python. Although I prefer Golang, I find that I can complete Python examples in half the time even accounting for +50% more bugs (approximately) that I tend to have in Python vs Go. This is optimizing for solved interview questons under pressure, when performance is considered then Go/C++ does consistently perform 1/10 the time of Python. In some rare cases algorithms that time out in Python that I can get away with in C++/Go on Leetcode. 


[Language Mechanics](#language-mechanics)

1. [Literals](#literals)
1. [Loops](#loops)
1. [Strings](#strings)
1. [Slicing](#slicing)
1. [Tuples](#tuple)
1. [Sort](#sort)
1. [Hash](#hash)
1. [Set](#set)
1. [List](#list)
1. [Dict](#dict)
1. [Binary Tree](#binarytree)
1. [heapq](#heapq)
1. [lambda](#lambda)
1. [zip](#zip)
1. [Random](#random)
1. [Constants](#constants)
1. [Ternary Condition](#ternary)
1. [Bitwise operators](#bitwise-operators)
1. [For Else](#for-else)
1. [Modulo](#modulo)
1. [any](#any)
1. [all](#all)
1. [bisect](#bisect)
1. [math](#math)
1. [iter](#iter)
1. [map](#map)
1. [filter](#filter)
1. [reduce](#reduce)
1. [itertools](#itertools)
1. [regular expression](#regular-expression)
1. [Types](#types)
1. [Grids](#grids)

[Collections](#collections)
1. [Deque](#deque)
1. [Counter](#counter)
1. [Default Dict](#default-dict)

[Algorithms](#algorithms)


1. [General Tips](#general-tips)
1. [Binary Search](#binary-search)
1. [Topological Sort](#topological-sort)
1. [Sliding Window](#sliding-window)
1. [Tree Tricks](#tree-tricks)
1. [Binary Search Tree](#binary-search-tree)
1. [Anagrams](#anagrams)
1. [Dynamic Programming](#dynamic-programming)
1. [Cyclic Sort](#cyclic-sort)
1. [Quick Sort](#quick-sort)
1. [Merge Sort](#merge-sort)
1. [Merge K Sorted Arrays](#merge-arrays)
1. [Linked List](#linked-list)
1. [Convert Base](#convert-base)
1. [Parenthesis](#parenthesis)
1. [Max Profit Stock](#max-profit-stock)
1. [Shift Array Right](#shift-array-right)
1. [Continuous Subarrays with Sum k ](#continuous-subarrays-with-sum-k)
1. [Events](#events)
1. [Merge Meetings](#merge-meetings)
1. [Trie](#trie)
1. [Kadane's Algorithm - Max subarray sum](#kadane)
1. [Union Find/DSU](#union-find)
1. [Fast Power](#fast-power)
1. [Fibonacci Golden](#fibonacci-golden)
1. [Basic Calculator](#basic-calculator)
1. [Reverse Polish](#reverse-polish)
1. [Resevior Sampling](#resevior-sampling)
1. [Candy Crush](#candy-crush)

# Language Mechanics

## Literals

```python
255, 0b11111111, 0o377, 0xff # Integers (decimal, binary, octal, hex)
123.0, 1.23                  # Float
7 + 5j, 7j                   # Complex 
'a', '\141', '\x61'          # Character (literal, octal, hex)
'\n', '\\', '\'', '\"'       # Newline, backslash, single quote, double quote
"string\n"                   # String of characters ending with newline 
"hello"+"world"              # Concatenated strings
True, False                  # bool constants, 1 == True, 0 == False 
[1, 2, 3, 4, 5]              # List 
['meh', 'foo', 5]            # List
(2, 4, 6, 8)                 # Tuple, immutable
{'name': 'a', 'age': 90}     # Dict
'a', 'e', 'i', 'o', 'u'}     # Set
None                         # Null var
```

## Loops

Go through all elements
```python
i = 0
while i < len(str):
  i += 1
```

equivalent
```python
for i in range(len(message)):
  print(i)
```

Get largest number index from right
```python
while i > 0 and nums [i-1] >= nums[i]:
  i -= 1
```

Manually reversing
```python
l, r = i, len(nums) - 1
while l < r:
  nums[l], nums[r] = nums[r], nums[l]
  l += 1
  r -= 1
```

Go past the loop if we are clever with our boundry
```python
for i in range(len(message) + 1):
  if i == len(message) or message[i] == ' ':
```

Fun with Ranges - range(start, stop, step)
```python
for a in range(0,3): # 0,1,2
for a in reversed(range(0,3)) # 2,1,0
for i in range(3,-1,-1) # 3,2,1,0
for i in range(len(A)//2): # A = [0,1,2,3,4,5]
  print(i) # 0,1,2 
  print(A[i]) # 0,1,2
  print(~i) # -1,-2,-3
  print(A[~i]) # 5,4,3
```

## Strings

```python
str1.find('x')          # find first location of char x and return index
str1.rfind('x')         # find first int location of char x from reverse
```

Parse a log on ":"
```python
l = "0:start:0"
tokens = l.split(":")
print(tokens) # ['0', 'start', '0']
```

Reverse works with built in split, [::-1] and " ".join()
```python
# s = "the sky  is blue"
def reverseWords(self, s: str) -> str:  
  wordsWithoutWhitespace = s.split() # ['the', 'sky', 'is', 'blue']
  reversedWords = wordsWithoutWhitespace[::-1] # ['blue', 'is', 'sky', 'the']        
  final = " ".join(reversedWords) # blue is sky the
```

Manual split based on isalpha()
```python
def splitWords(input_string) -> list: 
  words = [] # 
  start = length = 0
  for i, c in enumerate(input_string):
    if c.isalpha():
      if length == 0:
        start = i                    
        length += 1
      else:
        words.append(input_string[start:start+length])
        length = 0
  if length > 0:
    words.append(input_string[start:start+length])
  return words
```

Test type of char
```python
def rotationalCipher(input, rotation_factor):
  rtn = []
  for c in input:
    if c.isupper():
      ci = ord(c) - ord('A')
      ci = (ci + rotation_factor) % 26
      rtn.append(chr(ord('A') + ci))
    elif c.islower():
      ci = ord(c) - ord('a')
      ci = (ci + rotation_factor) % 26
      rtn.append(chr(ord('a') + ci))
    elif c.isnumeric():
      ci = ord(c) - ord('0')
      ci = (ci + rotation_factor) % 10
      rtn.append(chr(ord('0') + ci))
    else:
      rtn.append(c)
  return "".join(rtn)  
```

AlphaNumberic
```python
isalnum()
```

Get charactor index
```python
print(ord('A')) # 65
print(ord('B')-ord('A')+1) # 2
print(chr(ord('a') + 2)) # c
```

Replace characters or strings
```python
def isValid(self, s: str) -> bool:
  while '[]' in s or '()' in s or '{}' in s:
    s = s.replace('[]','').replace('()','').replace('{}','')
  return len(s) == 0
```

Insert values in strings
```python
txt3 = "My name is {}, I'm {}".format("John",36) # My name is John, I'm 36
```

Multiply strings/lists with *, even booleans which map to True(1) and False(0)
```python
'meh' * 2 # mehmeh
['meh'] * 2 # ['meh', 'meh']
['meh'] * True #['meh']
['meh'] * False #[]
```

Find substring in string
```python
txt = "Hello, welcome to my world."
x = txt.find("welcome")  # 7
```

startswith and endswith are very handy
```python
str = "this is string example....wow!!!"
str.endswith("!!") # True
str.startswith("this") # True
str.endswith("is", 2, 4) # True
```

Python3 format strings
```python
name = "Eric"
profession = "comedian"
affiliation = "Monty Python"
message = (
     f"Hi {name}. "
     f"You are a {profession}. "
     f"You were in {affiliation}."
)
message
'Hi Eric. You are a comedian. You were in Monty Python.'
```

Print string with all chars, useful for debugging
```python
print(repr("meh\n"))     # 'meh\n'
```

## Slicing

Slicing [intro](https://stackoverflow.com/questions/509211/understanding-slice-notation)

```python
                +---+---+---+---+---+---+
                | P | y | t | h | o | n |
                +---+---+---+---+---+---+
Slice position: 0   1   2   3   4   5   6
Index position:   0   1   2   3   4   5
p = ['P','y','t','h','o','n']
p[0] 'P' # indexing gives items, not lists
alpha[slice(2,4)] # equivalent to p[2:4]
p[0:1] # ['P'] Slicing gives lists
p[0:5] # ['P','y','t','h','o'] Start at beginning and count 5
p[2:4] = ['t','r'] # Slice assignment  ['P','y','t','r','o','n']
p[2:4] = ['s','p','a','m'] # Slice assignment can be any size['P','y','s','p','a','m','o','n']
p[4:4] = ['x','y'] # insert slice ['P','y','t','h','x','y','o','n'] 
p[0:5:2] # ['P', 't', 'o'] sliceable[start:stop:step]
p[5:0:-1] # ['n', 'o', 'h', 't', 'y']
```

Go through num and get combinations missing a member

```python
numList = [1,2,3,4]
for i in range(len(numList)): 
    newList = numList[0:i] + numList[i+1:len(numList)]
    print(newList) # [2, 3, 4], [1, 3, 4], [1, 2, 4], [1, 2, 3]
```

## Tuple

Collection that is ordered and unchangable

```python
thistuple = ("apple", "banana", "cherry")
print(thistuple[1]) # banana
```

Can be used with Dicts

```python
def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
    d = defaultdict(list)
    for w in strs:
        key = tuple(sorted(w))
        d[key].append(w)
    return d.values()
```

## Sort

sorted(iterable, key=key, reverse=reverse)

Sort sorts alphabectically, from smallest to largest

```python
print(sorted(['Ford', 'BMW', 'Volvo'])) # ['BMW', 'Ford', 'Volvo']
nums = [-4,-1,0,3,10]
print(sorted(n*n for n in nums)) # [0,1,9,16,100]
```

```python
cars = ['Ford', 'BMW', 'Volvo']
cars.sort() # returns None type
cars.sort(key=lambda x: len(x) ) # ['BMW', 'Ford', 'Volvo']
print(sorted(cars, key=lambda x:len(x))) # ['BMW', 'Ford', 'Volvo']
```

Sort key by value, even when value is a list
```python
meh = {'a':3,'b':0,'c':2,'d':-1}
print(sorted(meh, key=lambda x:meh[x])) # ['d', 'b', 'c', 'a']
meh = {'a':[0,3,'a'],'b':[-2,-3,'b'],'c':[2,3,'c'],'d':[-2,-2,'d']}
print(sorted(meh, key=lambda x:meh[x])) # ['b', 'd', 'a', 'c']
```

```python
def merge_sorted_lists(arr1, arr2): # built in sorted does Timsort optimized for subsection sorted lists
    return sorted(arr1 + arr2)
```

Sort an array but keep the original indexes
```python
self.idx, self.vals = zip(*sorted([(i,v) for i,v in enumerate(nums)], key=lambda x:x[1]))
```

Sort by tuple, 2nd element then 1st ascending
```python
a = [(5,10), (2,20), (2,3), (0,100)]
test = sorted(a, key = lambda x: (x[1],x[0])) 
print(test) # [(2, 3), (5, 10), (2, 20), (0, 100)]
test = sorted(a, key = lambda x: (-x[1],x[0])) 
print(test) # [(0, 100), (2, 20), (5, 10), (2, 3)]
```

Sort and print dict values by key
```python
ans = {-1: [(10, 1), (3, 3)], 0: [(0, 0), (2, 2), (7, 4)], -3: [(8, 5)]}
for key, value in sorted(ans.items()): print(value)
# [(8, 5)]
# [(10, 1), (3, 3)]
# [(0, 0), (2, 2), (7, 4)]

# sorted transforms dicts to lists
sorted(ans) # [-3, -1, 0]
sorted(ans.values()) # [[(0, 0), (2, 2), (7, 4)], [(8, 5)], [(10, 1), (3, 3)]]
sorted(ans.items()) # [(-3, [(8, 5)]), (-1, [(10, 1), (3, 3)]), (0, [(0, 0), (2, 2), (7, 4)])]
# Or just sort the dict directly
[ans[i] for i in sorted(ans)]
# [[(8, 5)], [(10, 1), (3, 3)], [(0, 0), (2, 2), (7, 4)]]
```

## Hash

```python
for c in s1: # Adds counter for c
  ht[c] = ht.get(c, 0) + 1 # ht[a] = 1, ht[a]=2, etc
```

## Set

```python
a = 3
st = set()
st.add(a) # Add to st
st.remove(a) # Remove from st
st.discard(a) # Removes from set with no error
st.add(a) # Add to st
next(iter(s)) # return 3 without removal
st.pop() # returns 3
```

```python
s = set('abc') # {'c', 'a', 'b'}
s |= set('cdf') # {'f', 'a', 'b', 'd', 'c'} set s with elements from new set
s &= set('bd') # {'d', 'b'} only elements from new set
s -= set('b') # {'d'} remove elements from new set
s ^= set('abd') # {'a', 'b'} elements from s or new but not both
```

## List

Stacks are implemented with Lists. Stacks are good for parsing and graph traversal

```python
test = [0] * 100 # initialize list with 100 0's
```

2D
```python
rtn.append([])
rtn[0].append(1) # [[1]]               
```

List Comprehension
```python
number_list = [ x for x in range(20) if x % 2 == 0]
print(number_list) # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

Reverse a list
```python
ss = [1,2,3]
ss.reverse()
print(ss) #3,2,1
```

Join list
```python
list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]
list3 = list1 + list2 # ['a', 'b', 'c', 1, 2, 3]
```

## Dict

Hashtables are implemented with dictionaries

```python
d = {'key': 'value'}         # Declare dict{'key': 'value'}
d['key'] = 'value'           # Add Key and Value
{x:0 for x in {'a', 'b'}}    # {'a': 0, 'b': 0} declare through comprehension 
d['key'])                    # Access value
d.items()                    # Items as tuple list dict_items([('key', 'value')])
if 'key' in d: print("meh")  # Check if value exists
par = {}
par.setdefault(1,1)          # returns 1, makes par = { 1 : 1 }
par = {0:True, 1:False}
par.pop(0)                   # Remove key 0, Returns True, par now {1: False}
for k in d: print(k)         # Iterate through keys
```

Create Dict of Lists that match length of list to count votes
```python
votes = ["ABC","CBD","BCA"]
rnk = {v:[0] * len(votes[0]) for v in votes[0]} 
print(rnk) # {'A': [0, 0, 0], 'B': [0, 0, 0], 'C': [0, 0, 0]}
```
## Tree

1. A [tree](https://www.geeksforgeeks.org/some-theorems-on-trees/) is an undirected [graph](https://www.cs.sfu.ca/~ggbaker/zju/math/trees.html) in which any two vertices are
connected by exactly one path.
1. Any connected graph who has n nodes with n-1 edges is a tree.
1. The degree of a vertex is the number of edges connected to the vertex.
1. A leaf is a vertex of degree 1. An internal vertex is a vertex of degree at least 2.
1. A [path graph](https://en.wikipedia.org/wiki/Path_graph) is a tree with two or more vertices with no branches, degree of 2 except for leaves which have degree of 1

1. Any two vertices in G can be connected by a unique simple path.
1. G is acyclic, and a simple cycle is formed if any edge is added to G.
1. G is connected and has no cycles.
1. G is connected but would become disconnected if any single edge is removed from G.


## BinaryTree


DFS Pre, In Order, and Post order Traversal

- Preorder
  - encounters roots before leaves
  - Create copy
- Inorder
  - flatten tree back to original sequence
  - Get values in non-decreasing order in BST
- Post order
  - encounter leaves before roots
  - Helpful for deleting

Recursive
```python
"""
     1
    / \
   2   3
  / \
 4   5
"""
# PostOrder 4 5 2 3 1  (Left-Right-Root)
def postOrder(node):
  if node is None:
    return
  postorder(node.left)
  postorder(node.right)
  print(node.value, end=' ')
```

Iterative PreOrder
```python
# PreOrder  1 2 4 5 3 (Root-Left-Right)
def preOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node.right, False))
        stack.append((node.left, False))
        stack.append((node, True))
```

Iterative InOrder
```python
# InOrder   4 2 5 1 3 (Left-Root-Right)
def inOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node.right, False))
        stack.append((node, True))
        stack.append((node.left, False))
```

Iterative PostOrder
```python
# PostOrder 4 5 2 3 1  (Left-Right-Root)
def postOrder(tree_root):
  stack = [(tree_root, False)]
  while stack:
    node, visited = stack.pop()
    if node:
      if visited:
        print(node.value, end=' ')
      else:
        stack.append((node, True))
        stack.append((node.right, False))
        stack.append((node.left, False))
```

Iterative BFS(LevelOrder)
```python
from collections import deque

#BFS levelOrder 1 2 3 4 5 
def levelOrder(tree_root):
  queue = deque([tree_root])
  while queue:
    node = queue.popleft()
    if node:
        print(node.value, end=' ')
        queue.append(node.left)
        queue.append(node.right)

def levelOrderStack(tree_root):
    stk = [(tree_root, 0)]
    rtn = []
    while stk:
        node, depth = stk.pop()
        if node:
            if len(rtn) < depth + 1:
                rtn.append([])
            rtn[depth].append(node.value)            
            stk.append((node.right, depth+1))
            stk.append((node.left, depth+1))
    print(rtn)
    return True     

def levelOrderStackRec(tree_root):
    rtn = []
        
    def helper(node, depth):
        if len(rtn) == depth:
            rtn.append([])
        rtn[depth].append(node.value)
        if node.left:
            helper(node.left, depth + 1)
        if node.right:
            helper(node.right, depth + 1)
            
    helper(tree_root, 0)
    print(rtn)
    return rtn
```

Traversing data types as a graph, for example BFS
```python
def removeInvalidParentheses(self, s: str) -> List[str]:
    rtn = []
    v = set()
    v.add(s)
    if len(s) == 0: return [""]
    while True:
        for n in v:
            if self.isValid(n):
                rtn.append(n)
        if len(rtn) > 0: break
        level = set()
        for n in v:
            for i, c in enumerate(n):
                if c == '(' or c == ')':
                    sub = n[0:i] + n[i + 1:len(n)]
                    level.add(sub)
        v = level
    return rtn
```

Reconstructing binary trees
1. Binary tree could be constructed from preorder and inorder traversal
1. Inorder traversal of BST is an array sorted in the ascending order

Convert tree to array and then to balanced tree
```python
def balanceBST(self, root: TreeNode) -> TreeNode:
    self.inorder = []
    
    def getOrder(node):
        if node is None:
            return
        getOrder(node.left)
        self.inorder.append(node.val)
        getOrder(node.right)

    # Get inorder treenode ["1,2,3,4"]
    getOrder(root)
    
    # Convert to Tree
    #        2
    #       1 3
    #          4
    def bst(listTree):
        if not listTree:
            return None
        mid = len(listTree) // 2
        root = TreeNode(listTree[mid])
        root.left = bst(listTree[:mid])
        root.right = bst(listTree[mid+1:])
        return root

    return bst(self.inorder)
```

## Graph

Build an [adjecency graph](https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/representing-graphs) from edges list
```python
# N = 6, edges = [[0,1],[0,2],[2,3],[2,4],[2,5]]
graph = [[] for _ in range(N)]
for u,v in edges:
    graph[u].append(v)
    graph[v].append(u)
# [[1, 2], [0], [0, 3, 4, 5], [2], [2], [2]]
```

Build adjecency graph from traditional tree
```python
adj = collections.defaultdict(list)
def dfs(node):
    if node.left:
        adj[node].append(node.left)
        adj[node.left].append(node)
        dfs(node.left)
    if node.right:
        adj[node].append(node.right)
        adj[node.right].append(node)
        dfs(node.right)
dfs(root)
```

Traverse Tree in graph notation
```python
# [[1, 2], [0], [0, 3, 4, 5], [2], [2], [2]]
def dfs(node, par=-1):
    for nei in graph[node]:
        if nei != par:
            res = dfs(nei, node)
dfs(0) # 1->2->3->4->5
```

## Heapq
```
      1
     / \
    2   3
   / \ / \
  5  6 8  7
```

[Priority Queue](https://realpython.com/python-heapq-module/#data-structures-heaps-and-priority-queues) 
1. Implemented as complete binary tree, which has all levels as full excepted deepest
1. In a heap tree the node is smaller than its children

```python
def maximumProduct(self, nums: List[int]) -> int:
  l = heapq.nlargest(3, nums)
  s = heapq.nsmallest(3, nums)
  return max(l[0]*l[1]*l[2],s[0]*s[1]*l[0])
```

Heap elements can be tuples, heappop() frees the smallest element (flip sign to pop largest)
```python
def kClosest(self, points: List[List[int]], K: int) -> List[List[int]]:
    heap = []
    for p in points:
        distance = sqrt(p[0]* p[0] + p[1]*p[1])
        heapq.heappush(heap,(-distance, p))
        if len(heap) > K:
            heapq.heappop(heap)            
    return ([h[1] for h in heap])
```

nsmallest can take a lambda argument
```python
def kClosest(self, points: List[List[int]], K: int) -> List[List[int]]:    
    return heapq.nsmallest(K, points, lambda x: x[0]*x[0] + x[1]*x[1])
```

The key can be a function as well in nsmallest/nlargest
```python
def topKFrequent(self, nums: List[int], k: int) -> List[int]:
    count = Counter(nums)
    return heapq.nlargest(k, count, count.get)
```

Tuple sort, 1st/2nd element. increasing frequency then decreasing order
```python
def topKFrequent(self, words: List[str], k: int) -> List[str]:
    freq = Counter(words)
    return heapq.nsmallest(k, freq.keys(), lambda x:(-freq[x], x))
```

## Lambda

Can be used with (list).sort(), sorted(), min(), max(), (heapq).nlargest,nsmallest(), map()

```python
# a=3,b=8,target=10
min((b,a), key=lambda x: abs(target - x)) # 8
```

```python
>>> ids = ['id1', 'id2', 'id30', 'id3', 'id22', 'id100']
>>> print(sorted(ids)) # Lexicographic sort
['id1', 'id100', 'id2', 'id22', 'id3', 'id30']
>>> sorted_ids = sorted(ids, key=lambda x: int(x[2:])) # Integer sort
>>> print(sorted_ids)
['id1', 'id2', 'id3', 'id22', 'id30', 'id100']
```

```python
trans = lambda x: list(al[i] for i in x) # apple, a->0..
print(trans(words[0])) # [0, 15, 15, 11, 4]
```

Lambda can sort by 1st, 2nd element in tuple
```python
sorted([('abc', 121),('bbb',23),('abc', 148),('bbb', 24)], key=lambda x: (x[0],x[1]))
# [('abc', 121), ('abc', 148), ('bbb', 23), ('bbb', 24)]
```

## Zip

Combine two dicts or lists
```python
s1 = {2, 3, 1}
s2 = {'b', 'a', 'c'}
list(zip(s1, s2)) # [(1, 'a'), (2, 'c'), (3, 'b')]
```

Traverse in Parallel
```python
letters = ['a', 'b', 'c']
numbers = [0, 1, 2]
for l, n in zip(letters, numbers):
  print(f'Letter: {l}') # a,b,c
  print(f'Number: {n}') # 0,1,2
```

Empty in one list is ignored
```python
letters = ['a', 'b', 'c']
numbers = []
for l, n in zip(letters, numbers):
  print(f'Letter: {l}') #
  print(f'Number: {n}') #
```

Compare characters of alternating words
```python
for a, b in zip(words, words[1:]):
    for c1, c2 in zip(a,b):
        print("c1 ", c1, end=" ")
        print("c2 ", c2, end=" ") 
```

Passing in [*](https://stackoverflow.com/questions/29139350/difference-between-ziplist-and-ziplist/29139418) unpacks a list or other iterable, making each of its elements a separate argument. 

```python
a = [[1,2],[3,4]]
test = zip(*a)
print(test) # (1, 3) (2, 4)
matrix = [[1,2,3],[4,5,6],[7,8,9]]
test = zip(*matrix)
print(*test) # (1, 4, 7) (2, 5, 8) (3, 6, 9)
```

Useful when rotating a matrix
```python
# matrix = [[1,2,3],[4,5,6],[7,8,9]]
matrix[:] = zip(*matrix[::-1]) # [[7,4,1],[8,5,2],[9,6,3]]
```

Iterate through chars in a list of strs
```python
strs = ["cir","car","caa"]
for i, l in enumerate(zip(*strs)):
    print(l)  
    # ('c', 'c', 'c')
    # ('i', 'a', 'a')
    # ('r', 'r', 'a')
```

Diagonals can be traversed with the help of a list

```python
"""
[[1,2,3],
 [4,5,6],
 [7,8,9],
 [10,11,12]]
"""
def printDiagonalMatrix(self, matrix: List[List[int]]) -> bool:
    R = len(matrix)
    C = len(matrix[0])
    
    tmp = [[] for _ in range(R+C-1)]
    
    for r in range(R):
        for c in range(C):
            tmp[r+c].append(matrix[r][c])
    
    for t in tmp:
        for n in t:
            print(n, end=' ')            
        print("")
"""
 1,
 2,4
 3,5,7
 6,8,10
 9,11
 12
"""
```

## Random

```Python
for i, l in enumerate(shuffle):
  r = random.randrange(0+i, len(shuffle))
  shuffle[i], shuffle[r] = shuffle[r], shuffle[i]
return shuffle
```

Other random generators
```Python
import random
ints = [0,1,2]
random.choice(ints) # 0,1,2
random.choices([1,2,3],[1,1,10]) # 3, heavily weighted
random.randint(0,2) # 0,1, 2
random.randint(0,0) # 0
random.randrange(0,0) # error
random.randrange(0,2) # 0,1
```

## Constants

```Python
max = float('-inf')
min = float('inf')
```

## Ternary

a if condition else b
```Python
test = stk.pop() if stk else '#'
```

## Bitwise Operators
```python
'0b{:04b}'.format(0b1100 & 0b1010) # '0b1000' and
'0b{:04b}'.format(0b1100 | 0b1010) # '0b1110' or 
'0b{:04b}'.format(0b1100 ^ 0b1010) # '0b0110' exclusive or
'0b{:04b}'.format(0b1100 >> 2)     # '0b0011' shift right
'0b{:04b}'.format(0b0011 << 2)     # '0b1100' shift left
```

## For Else

Else condition on for loops if break is not called

```python
for w1, w2 in zip(words, words[1:]): #abc, ab
    for c1, c2 in zip(w1, w2):
        if c1 != c2:
            adj[c1].append(c2)
            degrees[c2] += 1
            break
    else: # nobreak
        if len(w1) > len(w2):
            return ""   # Triggers since ab should be before abc, not after
```

## Modulo

```python
for n in range(-8,8):
    print n, n//4, n%4
    
 -8 -2 0
 -7 -2 1
 -6 -2 2
 -5 -2 3

 -4 -1 0
 -3 -1 1
 -2 -1 2
 -1 -1 3

  0  0 0
  1  0 1
  2  0 2
  3  0 3

  4  1 0
  5  1 1
  6  1 2
  7  1 3
```

## Any

if any element of the iterable is True
```python
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```

## All
```python
def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```

## Bisect

* bisect.bisect_left returns the leftmost place in the sorted list to insert the given element
* bisect.bisect_right returns the rightmost place in the sorted list to insert the given element

```python
import bisect
bisect.bisect_left([1,2,3,4,5], 2)  # 1
bisect.bisect_right([1,2,3,4,5], 2) # 2
bisect.bisect_left([1,2,3,4,5], 7)  # 5
bisect.bisect_right([1,2,3,4,5], 7) # 5
```

Insert x in a in sorted order. This is equivalent to a.insert(bisect.bisect_left(a, x, lo, hi), x) assuming that a is already sorted. Search is binary search O(logn) and insert is O(n)

```python
import bisect
l = [1, 3, 7, 5, 6, 4, 9, 8, 2]
result = []
for e in l:
    bisect.insort(result, e)
print(result) # [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

```python
li1 = [1, 3, 4, 4, 4, 6, 7] # [1, 3, 4, 4, 4, 5, 6, 7]
bisect.insort(li1, 5) # 
```

Bisect can give two ends of a range, if the array is sorted of course
```python
s = bisect.bisect_left(nums, target)
e = bisect.bisect(nums, target) -1
if s <= e:
    return [s,e]
else:
    return [-1,-1]
```

## Math

Calulate power

```python
# (a ^ b) % p. 
d = pow(a, b, p) 
```

Division with remainder
```python
divmod(8, 3) # (2, 2)
divmod(3, 8) #  (0, 3)
```

## eval

Evaluates an expression
```python
x = 1
print(eval('x + 1'))
```

## Iter

Creates iterator from container object such as list, tuple, dictionary and set

```python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)
print(next(myit)) # apple
print(next(myit)) # banana
```

## Map

map(func, *iterables)

```python
my_pets = ['alfred', 'tabitha', 'william', 'arla']
uppered_pets = list(map(str.upper, my_pets)) # ['ALFRED', 'TABITHA', 'WILLIAM', 'ARLA']
my_strings = ['a', 'b', 'c', 'd', 'e']
my_numbers = [1,2,3,4,5]
results = list(map(lambda x, y: (x, y), my_strings, my_numbers)) # [('a', 1), ('b', 2), ('c', 3), ('d', 4), ('e', 5)]
```

```python
A1 = [1, 4, 9]
''.join(map(str, A1))
```

## Filter

filter(func, iterable)

```python
scores = [66, 90, 68, 59, 76, 60, 88, 74, 81, 65]
over_75 = list(filter(lambda x: x>75, scores)) # [90, 76, 88, 81]
```

```python
scores = [66, 90, 68, 59, 76, 60, 88, 74, 81, 65]
def is_A_student(score):
    return score > 75
over_75 = list(filter(is_A_student, scores)) # [90, 76, 88, 81]
```

```python
dromes = ("demigod", "rewire", "madam", "freer", "anutforajaroftuna", "kiosk")
palindromes = list(filter(lambda word: word == word[::-1], dromes)) # ['madam', 'anutforajaroftuna']
```

Get degrees == 0 from list
```python
stk = list(filter(lambda x: degree[x]==0, degree.keys()))
```

## Reduce

reduce(func, iterable[, initial]) 
where initial is optional

```python
numbers = [3, 4, 6, 9, 34, 12]
result = reduce(lambda x, y: x+y, numbers) # 68
result = reduce(lambda x, y: x+y, numbers, 10) #78
```

## itertools

[itertools.accumulate(iterable[, func]) –> accumulate object](https://www.geeksforgeeks.org/python-itertools-accumulate/)

```python
import itertools
data = [3, 4, 6, 2, 1, 9, 0, 7, 5, 8]
list(itertools.accumulate(data)) # [3, 7, 13, 15, 16, 25, 25, 32, 37, 45]
list(accumulate(data, max))  # [3, 4, 6, 6, 6, 9, 9, 9, 9, 9]
cashflows = [1000, -90, -90, -90, -90]  # Amortize a 5% loan of 1000 with 4 annual payments of 90
list(itertools.accumulate(cashflows, lambda bal, pmt: bal*1.05 + pmt)) [1000, 960.0, 918.0, 873.9000000000001, 827.5950000000001]
for k,v in groupby("aabbbc")    # group by common letter
    print(k)                    # a,b,c
    print(list(v))              # [a,a],[b,b,b],[c,c]
```

## Regular Expression

RE module allows regular expressions in python

```python
def removeVowels(self, S: str) -> str:
    return re.sub('a|e|i|o|u', '', S)
```

## Types

from typing import List, Set, Dict, Tuple, Optional
[cheat sheet](https://mypy.readthedocs.io/en/stable/cheat_sheet_py3.html)

## Grids

Useful helpful function
```python
R = len(grid)
C = len(grid[0])

def neighbors(r, c):
    for nr, nc in ((r,c-1), (r,c+1), (r-1, c), (r+1,c)):
        if 0<=nr<R and 0<=nc<C:
            yield nr, nc

def dfs(r,c, index):
    area = 0
    grid[r][c] = index
    for x,y in neighbors(r,c):
        if grid[x][y] == 1:
            area += dfs(x,y, index)
    return area + 1
```

# Collections

Stack with appendleft() and popleft()

## Deque

```python
from collections import deque
deq = deque([1, 2, 3])
deq.appendleft(5)
deq.append(6)
deq
deque([5, 1, 2, 3, 6])
deq.popleft()
5
deq.pop()
6
deq
deque([1, 2, 3])
```

## Counter

```python
from collections import Counter
count = Counter("hello") # Counter({'h': 1, 'e': 1, 'l': 2, 'o': 1})
count['l'] # 2
count['l'] += 1
count['l'] # 3
```

Get counter k most common in list of tuples
```python
# [1,1,1,2,2,3]
# Counter  [(1, 3), (2, 2)]
def topKFrequent(self, nums: List[int], k: int) -> List[int]:
    if len(nums) == k:
        return nums
    return [n[0] for n in Counter(nums).most_common(k)] # [1,2]
```

elements() lets you walk through each number in the Counter
```python
def intersect(self, nums1: List[int], nums2: List[int]) -> List[int]:
    c1 = collections.Counter(nums1) # [1,2,2,1]
    c2 = collections.Counter(nums2) # [2,2]
    dif = c1 & c2                   # {2:2}
    return list(dif.elements())     # [2,2]
```

operators work on Counter
```python
c = Counter(a=3, b=1)
d = Counter(a=1, b=2)
c + d # {'a': 4, 'b': 3}
c - d # {'a': 2}
c & d # {'a': 1, 'b': 1}
c | d # {'a': 3, 'b': 2}
c = Counter(a=2, b=-4)
+c # {'a': 2}
-c # {'b': 4}
```

## Default Dict

```python
d={}
print(d['Grapes'])# This gives Key Error
from collections import defaultdict
d = defaultdict(int) # set default
print(d['Grapes']) # 0, no key error
d = collections.defaultdict(lambda: 1)
print(d['Grapes']) # 1, no key error
```

```python
from collections import defaultdict
dd = defaultdict(list)
dd['key'].append(1) # defaultdict(<class 'list'>, {'key': [1]})
dd['key'].append(2) # defaultdict(<class 'list'>, {'key': [1, 2]})
```

# Algorithms

## General Tips

* Get all info
* Debug example, is it a special case?
* Brute Force
  * Get to brute-force solution as soon as possible. State runtime and then optimize, don't code yet
* Optimize
  * Look for unused info
  * Solve it manually on example, then reverse engineer thought process
  * Space vs time, hashing
  * BUDS (Bottlenecks, Unnecessary work, Duplication)
* Walk through approach
* Code
* Test
  * Start small
  * Hit edge cases

## Binary Search

```python
def firstBadVersion(self, n):
    l, r = 0, n
    while l < r:
        m = l + (r-l) // 2
        if isBadVersion(m):
            r = m
        else:
            l = m + 1
    return l
```

```python
"""
12345678 
FFTTTTTT
"""
def mySqrt(self, x: int) -> int:
  def condition(value, x) -> bool:
    return value * value > x

  if x == 1:
    return 1

  left, right = 1, x
  while left < right:
    mid = left + (right-left) // 2
    if condition(mid, x):
      right = mid
    else:
      left = mid + 1

  return left - 1
```
[binary search](https://leetcode.com/discuss/general-discussion/786126/python-powerful-ultimate-binary-search-template-solved-many-problems)

## Binary Search Tree

Use values to detect if number is missing
```python
def isCompleteTree(self, root: TreeNode) -> bool:
    self.total = 0
    self.mx = float('-inf')
    def dfs(node, cnt):
        if node:
            self.total += 1
            self.mx = max(self.mx, cnt)
            dfs(node.left, (cnt*2))
            dfs(node.right, (cnt*2)+1)
    dfs(root, 1)
    return self.total == self.mx
```

Get a range sum of values
```python
def rangeSumBST(self, root: TreeNode, L: int, R: int) -> int:
    self.total = 0
    def helper(node):
        if node is None:
            return 0
        if L <= node.val <= R:
            self.total += node.val
        if node.val > L:
            left = helper(node.left)  
        if node.val < R:
            right = helper(node.right)
    helper(root)
    return self.total
```

Check if valid
```python
def isValidBST(self, root: TreeNode) -> bool:
    if not root:
        return True
    stk = [(root, float(-inf), float(inf))]
    while stk:
        node, floor, ceil = stk.pop()
        if node:
            if node.val >= ceil or node.val <= floor:
                return False
            stk.append((node.right, node.val, ceil))
            stk.append((node.left, floor, node.val))
    return True
```

## Topological Sort

[Kahn's algorithm](https://www.geeksforgeeks.org/all-topological-sorts-of-a-directed-acyclic-graph/), detects cycles through degrees and needs all the nodes represented to work 

1. Initialize vertices as unvisited
1. Pick vertex with zero indegree, append to result, decrease indegree of neighbors 
1. Now repeat for neighbors, resulting list is sorted by source -> dest

If cycle, then degree of nodes in cycle will not be 0 since there
is no origin

```python
def canFinish(self, numCourses: int, prerequisites: List[List[int]]) -> bool:
    # Kahns algorithm, topological sort
    adj = collections.defaultdict(list)
    degree = collections.Counter()
    
    for dest, orig in prerequisites:
        adj[orig].append(dest)
        degree[dest] += 1
    
    bfs = [c for c in range(numCourses) if degree[c] == 0]
    
    for o in bfs:
        for d in adj[o]:
            degree[d] -= 1
            if degree[d] == 0:
                bfs.append(d)

    return len(bfs) == numCourses
```

```python
def alienOrder(self, words: List[str]) -> str:
    nodes = set("".join(words))
    adj = collections.defaultdict(list)
    degree = collections.Counter(nodes)
    
    for w1, w2 in zip(words, words[1:]):
        for c1, c2 in zip(w1, w2):
            if c1 != c2:
                adj[c1].append(c2)
                degree[c2] += 1
                break
        else:
            if len(w1) > len(w2):
                return ""
    
    stk = list(filter(lambda x: degree[x]==1, degree.keys()))
    
    ans = []
    while stk:
        node = stk.pop()
        ans.append(node)
        for nei in adj[node]:
            degree[nei] -= 1
            if degree[nei] == 1:
                stk.append(nei)
    
    return "".join(ans) * (set(ans) == nodes)
```

## Sliding Window

1. Have a counter or hash-map to count specific array input and keep on increasing the window toward right using outer loop.
1. Have a while loop inside to reduce the window side by sliding toward right. Movement will be based on constraints of problem.
1. Store the current maximum window size or minimum window size or number of windows based on problem requirement.

### Typical Problem Clues:
1. Get min/max/number of satisfied sub arrays
1. Return length of the subarray with max sum/product
1. Return max/min length/number of subarrays whose sum/product equals K

Can require [2 or 3 pointers to solve](https://medium.com/algorithms-and-leetcode/magic-solution-to-leetcode-problems-sliding-window-algorithm-891e3d60bf89)

```python
    def slidingWindowTemplate(self, s: str):
        #init a collection or int value to save the result according the question.
        rtn = []
        
        # create a hashmap to save the Characters of the target substring.
        # (K, V) = (Character, Frequence of the Characters)
        hm = {}

        # maintain a counter to check whether match the target string as needed
        cnt = collections.Counter(s)

        # Two Pointers: begin - left pointer of the window; end - right pointer of the window if needed
        l = r = 0

        # loop at the begining of the source string
        for r, c in enumerate(s): 
            
            if c in hm:
                l = max(hm[c]+1, l) # +/- 1 or set l to index, max = never move l left 

            # update hm
            hm[c] = r

            # increase l pointer to make it invalid/valid again
            while cnt == 0: # counter condition
                cnt[c] += 1  # modify counter if needed
    
            # Save result / update min/max after loop is valid
            rtn = max(rtn, r-l+1)

        return rtn
```

```python
def fruits_into_baskets(fruits):
  maxCount, j = 0, 0
  ht = {}

  for i, c in enumerate(fruits):
    if c in ht:
      ht[c] += 1
    else:
      ht[c] = 1

    if len(ht) <= 2:
      maxCount = max(maxCount, i-j+1)
    else:
      jc = fruits[j]
      ht[jc] -= 1
      if ht[jc] <= 0:
        del ht[jc]
      j += 1  

  return maxCount
```

## Greedy

Make the optimal [choice](https://brilliant.org/wiki/greedy-algorithm/) at each step. 

[Increasing Triplet Subsequence](https://leetcode.com/problems/increasing-triplet-subsequence/), true if i < j < k
```python
def increasingTriplet(self, nums: List[int]) -> bool:
    l = m = float('inf')
    
    for n in nums:
        if n <= l:
            l = n
        elif n <= m:
            m = n
        else:
            return True
    
    return False
```

## Tree Tricks

Bottom up solution with arguments for min, max

```python
def maxAncestorDiff(self, root: TreeNode) -> int:
    if not root:
        return 0
    self.ans = 0
    def dfs(node, minval, maxval):
        if not node:
            self.ans = max(self.ans, abs(maxval - minval))
            return
        dfs(node.left, min(node.val, minval), max(node.val, maxval))
        dfs(node.right, min(node.val, minval), max(node.val, maxval))
    dfs(root, float('inf'), float('-inf'))
    return self.ans
```

Building a path through a tree 
```python
def binaryTreePaths(self, root: TreeNode) -> List[str]:
    rtn = []
    if root is None: return []
    stk = [(root, str(root.val))]
    while stk:
        node, path = stk.pop()
        if node.left is None and node.right is None:
            rtn.append(path)
        if node.left:
            stk.append((node.left, path + "->" + str(node.left.val)))
        if node.right:
            stk.append((node.right, path + "->" + str(node.right.val)))
    return rtn
```

Using return value to sum
```python
def diameterOfBinaryTree(self, root: TreeNode) -> int:
    self.mx = 0
    def dfs(node):
        if node:
            l = dfs(node.left)
            r = dfs(node.right)
            total = l + r
            self.mx = max(self.mx, total) 
            return max(l, r) + 1
        else:
            return 0
    dfs(root)
    return self.mx
```

Change Tree to Graph
```python
def distanceK(self, root: TreeNode, target: TreeNode, K: int) -> List[int]:
    adj = collections.defaultdict(list)
    
    def dfsa(node):
        if node.left:
            adj[node].append(node.left)
            adj[node.left].append(node)
            dfsa(node.left)
        if node.right:
            adj[node].append(node.right)
            adj[node.right].append(node)
            dfsa(node.right)
            
    dfsa(root)
    
    def dfs(node, prev, d):
        if node:
            if d == K:
                rtn.append(node.val)
            else:
                for nei in adj[node]:
                    if nei != prev:
                        dfs(nei, node, d+1)
                
    rtn = []
    dfs(target, None, 0)
    return rtn
```

## Anagrams

Subsection of sliding window, solve with Counter Dict

i.e.
abc   =   bca   !=  eba
111       111       111

```python
def isAnagram(self, s: str, t: str) -> bool:
    sc = collections.Counter(s)
    st = collections.Counter(t)
    if sc != st:
        return False
    return True
```

Sliding Window version (substring)

```python
def findAnagrams(self, s: str, p: str) -> List[int]:
    cntP = collections.Counter(p)
    cntS = collections.Counter()
    P = len(p)
    S = len(s)
    if P > S:
        return []
    ans = []
    for i, c in enumerate(s):
        cntS[c] += 1
        if i >= P:
            if cntS[s[i-P]] > 1:
                cntS[s[i-P]] -= 1
            else:
                del cntS[s[i-P]]
        if cntS == cntP:
            ans.append(i-(P-1))
    return ans
```



## Dynamic Programming

1. [dynamic programming](https://leetcode.com/discuss/general-discussion/458695/Dynamic-Programming-Patterns)

```python
def coinChange(self, coins: List[int], amount: int) -> int:
  MAX = float('inf')
  dp =  [MAX] * (amount + 1)
  dp[0] = 0
  for c in coins:
    for a in range(c, amount+1):    
      dp[a] =  min(dp[a], dp[a-c]+1)      
  return dp[amount] if dp[amount] != MAX else -1
```

Classic DP grid, longest common subsequence
```python
def longestCommonSubsequence(self, text1: str, text2: str) -> int:
    Y = len(text2)+1
    X = len(text1)+1
    dp = [[0] * Y for _ in range(X)]
    # [[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0]]
    for i, c in enumerate(text1):
        for j, d in enumerate(text2):
            if c == d:
                dp[i + 1][j + 1] = 1 + dp[i][j]  
            else:
                dp[i + 1][j + 1] = max(dp[i][j + 1], dp[i + 1][j])
    return dp[-1][-1]
# [[0,0,0,0],[0,1,1,1],[0,1,1,1],[0,1,2,2],[0,1,2,2],[0,1,2,3]]
# abcde
# "ace"
```



## Cyclic Sort

1. Useful algo when sorting in place

```python
# if my number is equal to my index, i+1 
# if my number is equal to this other number, i+1 (dups)
# else swap
def cyclic_sort(nums):
  i = 0
  while i < len(nums):
    j = nums[i] - 1
    if nums[i] != nums[j]:
      nums[i], nums[j] = nums[j], nums[i]  
    else:
      i += 1
  return nums
```

## Quick Sort

1. Can be modified for divide in conquer problems

```python
def quickSort(array):
	def sort(arr, l, r):
		if l < r:
			p = part(arr, l, r)
			sort(arr, l, p-1)
			sort(arr, p+1, r)

	def part(arr, l, r):
		pivot = arr[r]
		a = l
		for i in range(l,r):
			if arr[i] < pivot:
				arr[i], arr[a] = arr[a], arr[i]
				a += 1
		arr[r], arr[a] = arr[a], arr[r]
		return a

	sort(array, 0, len(array)-1)
	return array
```

## Merge Sort

```python
from collections import deque 
def mergeSort(array):
    def sortArray(nums):
        if len(nums) > 1:
            mid = len(nums)//2
            l1 = sortArray(nums[:mid])
            l2 = sortArray(nums[mid:])
            nums = sort(l1,l2)
        return nums
    
    def sort(l1,l2):
        result = []
        l1 = deque(l1)
        l2 = deque(l2)
        while l1 and l2:
            if l1[0] <= l2[0]:
                result.append(l1.popleft())
            else:
                result.append(l2.popleft())
        result.extend(l1 or l2)
        return result
	return sortArray(array)
```

## Merge Arrays

Merge K sorted Arrays with a heap
```python
def mergeSortedArrays(self, arrays):   
    return list(heapq.merge(*arrays))
```

Or manually with heappush/heappop. 

```python
class Solution:
def mergeSortedArrays(self, arrays):
    pq = []
    for i, arr in enumerate(arrays):
        pq.append((arr[0], i, 0))
    heapify(pq)

    res = []
    while pq:
        num, i, j = heappop(pq)
        res.append(num)
        if j + 1 < len(arrays[i]):
            heappush(pq, (arrays[i][j + 1], i, j + 1))
    return res
```

Merging K Sorted Lists

```python
def mergeKLists(self, lists: List[ListNode]) -> ListNode:
    prehead = ListNode()
    heap = []
    for i in range(len(lists)):
        node = lists[i]
        while node:
            heapq.heappush(heap, node.val)
            node = node.next 
    node = prehead
    while len(heap) > 0:
        val = heapq.heappop(heap)
        node.next = ListNode()
        node = node.next 
        node.val = val
    return prehead.next
```


## Linked List

1. Solutions typically require 3 pointers: current, previous and next
1. Solutions are usually made simplier with a prehead or dummy head node you create and then add to. Then return dummy.next

Reverse:
```python
def reverseLinkedList(head):
    prev, node  = None, head
    while node:
        node.next, prev, node = prev, node, node.next
    return prev
```

Reversing is easier if you can modify the values of the list
```python
def reverse(head):
  node = head
  stk = []
  while node:
    if node.data % 2 == 0:
      stk.append(node)
    if node.data % 2 == 1 or node.next is None:
      while len(stk) > 1:
        stk[-1].data, stk[0].data = stk[0].data, stk[-1].data
        stk.pop(0)
        stk.pop(-1)
      stk.clear()
    node = node.next
  return head
```
Merge:
```python
def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
    dummy = ListNode(-1)
    
    prev = dummy
    
    while l1 and l2:
        if l1.val < l2.val:
            prev.next = l1
            l1 = l1.next 
        else:
            prev.next = l2
            l2 = l2.next 
        prev = prev.next 
    
    prev.next = l1 if l1 is not None else l2 
    
    return dummy.next 
```

## Convert Base

1. Typically two steps. A digit modulo step and a integer division step by the next base then reverse the result or use a deque()

Base 10 to 16, or any base by changing '16' and index
```python
def toHex(self, num: int) -> str:
  rtn = []
  index = "0123456789abcdef"
  if num == 0: return '0'
  if num < 0: num += 2 ** 32
  while num > 0:
    digit = num % 16
    rtn.append(index[digit])
    num = num // 16
  return "".join(rtn[::-1])
```

## Parenthesis

1. Count can be used if simple case, otherwise stack. [Basic Calculator](#basic-calculator) is an extension of this algo

```python
def isValid(self, s) -> bool:
  cnt = 0
  for c in s:
    if c == '(':
      cnt += 1
    elif c == ')':
      cnt -= 1
      if cnt < 0:
        return False
  return cnt == 0
```

Stack can be used if more complex 
```python
def isValid(self, s: str) -> bool:
  stk = []
  mp = {")":"(", "}":"{", "]":"["}
    for c in s:
      if c in mp.values():
        stk.append(c)
      elif c in mp.keys():
        test = stk.pop() if stk else '#'
        if mp[c] != test:
          return False
  return len(stk) == 0
```

Or must store parenthesis index for further modification

```python
def minRemoveToMakeValid(self, s: str) -> str:
  rtn = list(s)
  stk = []
  for i, c in enumerate(s):
    if c == '(':
      stk.append(i)
    elif c == ')':
      if len(stk) > 0:
        stk.pop()
      else:
        rtn[i] = ''
  while stk:
    rtn[stk.pop()] = ''
  return "".join(rtn)
```

## Max Profit Stock

Infinite Transactions, [base formula](https://leetcode.com/problems/best-time-to-buy-and-sell-stock-with-cooldown/discuss/75924/Most-consistent-ways-of-dealing-with-the-series-of-stock-problems)
```python
def maxProfit(self, prices: List[int]) -> int:
    t0, t1 = 0, float('-inf')
    for p in prices:
        t0old = t0
        t0 = max(t0, t1 + p)
        t1 = max(t1, t0old - p)
    return t0
```

Single Transaction, t0 (k-1) = 0
```python
def maxProfit(self, prices: List[int]) -> int:
    t0, t1 = 0, float('-inf')
    for p in prices:
        t0 = max(t0, t1 + p)
        t1 = max(t1, - p)
    return t0
```

K Transactions
```python
t0 = [0] * (k+1)
t1 = [float(-inf)] * (k+1)
for p in prices:
    for i in range(k, 0, -1):
        t0[i] = max(t0[i], t1[i] + p)
        t1[i] = max(t1[i], t0[i-1] - p)
return t0[k]
```

## Shift Array Right
Arrays can be shifted right by reversing the whole string, and then reversing 0,k-1 and k,len(str)
```python
def rotate(self, nums: List[int], k: int) -> None:
    def reverse(l, r, nums):
        while l < r:
            nums[l], nums[r] = nums[r], nums[l]
            l += 1
            r -= 1
    if len(nums) <= 1: return
    k = k % len(nums)
    reverse(0, len(nums)-1, nums)
    reverse(0, k-1, nums)
    reverse(k, len(nums)-1, nums)
```

## Continuous Subarrays with Sum k 

The total number of continuous subarrays with sum k can be found by hashing the continuous sum per value and adding the count of continuous sum - k

```python
def subarraySum(self, nums: List[int], k: int) -> int:
    mp = {0: 1} 
    rtn, total = 0, 0
    for n in nums:
        total += n
        rtn += mp.get(total - k, 0)
        mp[total] = mp.get(total, 0) + 1
    return rtn
```

## Events

Events pattern can be applied when to many interval problems such as 'Find employee free time between meetings' and 'find peak population' when individual start/ends
are irrelavent and sum start/end times are more important

```python
def employeeFreeTime(self, schedule: '[[Interval]]') -> '[Interval]':
    events = []
    for e in schedule:
        for m in e:
            events.append((m.start, 1))
            events.append((m.end, -1))
    events.sort()
    itv = []
    prev = None
    bal = 0
    for t, c in events:
        if bal == 0 and prev is not None and t != prev:
            itv.append(Interval(prev, t))
        bal += c
        prev = t
    return itv
```

## Merge Meetings

Merging a new meeting into a list

```python
def insert(self, intervals: List[List[int]], newInterval: List[int]) -> List[List[int]]:
    bisect.insort(intervals, newInterval)
    merged = [intervals[0]]
    for i in intervals:
        ms, me = merged[-1]
        s, e = i
        if me >= s:
            merged[-1] = (ms, max(me, e))
        else:
            merged.append(i)
    return merged
```

## Trie

Good for autocomplete, spell checker, IP routing (match longest prefix), predictive text, solving word games

```python
class Trie:
    def __init__(self):
        self.root = {}
    
    def addWord(self, s: str):
        tmp = self.root 
        for c in s:
            if c not in tmp:
                tmp[c] = {}
            tmp = tmp[c]
        tmp['#'] = s # Store full word at '#' to simplify
    
    def matchPrefix(self, s: str, tmp=None):
        if not tmp: tmp = self.root 
        for c in s:
            if c not in tmp:
                return []
            tmp = tmp[c]
        
        rtn = []
        
        for k in tmp:
            if k == '#':
                rtn.append(tmp[k])
            else:
                rtn += self.matchPrefix('', tmp[k])
        return rtn
            
    def hasWord(self, s: str):
        tmp = self.root 
        for c in s:
            if c in tmp:
                tmp = tmp[c]
            else:
                return False
        return True
```

Search example with . for wildcards

```python
def search(self, word: str) -> bool:
    def searchNode(word, node):
        for i,c in enumerate(word):
            if c in node:
                node = node[c]
            elif c == '.':
                return any(searchNode(word[i+1:], node[cn]) for cn in node if cn != '$' )
            else:
                return False
        return '$' in node
    return searchNode(word, self.trie)
```

## Kadane

local_maxiumum[i] = max(A[i], A[i] + local_maximum[i-1])
[Explanation](https://medium.com/@rsinghal757/kadanes-algorithm-dynamic-programming-how-and-why-does-it-work-3fd8849ed73d)
Determine max subarray sum

```python
# input: [-2,1,-3,4,-1,2,1,-5,4]
def maxSubArray(self, nums: List[int]) -> int:
    for i in range(1, len(nums)):
        if nums[i-1] > 0:
            nums[i] += nums[i-1]
    return max(nums) # max([-2,1,-2,4,3,5,6,1,5]) = 6
```

## Union Find

[Union Find](https://www.geeksforgeeks.org/union-find/) is a useful algorithm for graph

DSU for integers
```python
class DSU:
    def __init__(self, N):
        self.par = list(range(N))

    def find(self, x): # Find Parent
        if self.par[x] != x:
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr: # If parents are equal, return False
            return False
        self.par[yr] = xr # Give y node parent of x
        return True # return True if union occured
```

DSU for strings
```python
class DSU:
    def __init__(self):
        self.par = {}

    def find(self, x):
        if x != self.par.setdefault(x, x):
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr: return
        self.par[yr] = xr
```

DSU with union by rank
```python
class DSU:
    def __init__(self, N):
        self.par = list(range(N))
        self.sz = [1] * N

    def find(self, x):
        if self.par[x] != x:
            self.par[x] = self.find(self.par[x])
        return self.par[x]

    def union(self, x, y):
        xr, yr = self.find(x), self.find(y)
        if xr == yr:
            return False
        if self.sz[xr] < self.sz[yr]:
            xr, yr = yr, xr
        self.par[yr] = xr
        self.sz[xr] += self.sz[yr]
        return True
```

## Fast Power

Fast Power, or Exponential by [squaring](https://en.wikipedia.org/wiki/Exponentiation_by_squaring) allows calculating squares in logn time (x^n)*2 = x^(2*n)
```python
def myPow(self, x: float, n: int) -> float:
    if n < 0:
        n *= -1
        x = 1/x
    ans = 1        
    while n > 0:
        if n % 2 == 1:
            ans = ans * x
        x *= x
        n = n // 2
    return ans
```

## Fibonacci Golden

Fibonacci can be calulated with [Golden Ratio](https://demonstrations.wolfram.com/GeneralizedFibonacciSequenceAndTheGoldenRatio/)

```python
def fib(self, N: int) -> int:
    golden_ratio = (1 + 5 ** 0.5) / 2
    return int((golden_ratio ** N + 1) / 5 ** 0.5)
```

## Basic Calculator

A calculator can be simulated with stack

```python
class Solution:
    def calculate(self, s: str) -> int:
        s += '$'
        def helper(stk, i):
            sign = '+'
            num = 0
            while i < len(s):
                c = s[i]
                if c == " ":
                    i += 1
                    continue
                elif c.isdigit():
                    num = num * 10 + int(c)
                    i += 1
                elif c == '(':
                    num, i = helper([], i+1)
                else:
                    if sign == '+':
                        stk.append(num)
                    if sign == '-':
                        stk.append(-num)
                    if sign == '*':
                        stk.append(stk.pop() * num)
                    if sign == '/':
                        stk.append(int(stk.pop() / num))
                    i += 1
                    num = 0
                    if c == ')':
                        return sum(stk), i
                    sign = c
            return sum(stk)
        return helper([],0)
```

## Reverse Polish

```python
class Solution:
    def evalRPN(self, tokens: List[str]) -> int:
        stk = []
        while tokens:
            c = tokens.pop(0)
            if c not in '+-/*':
                stk.append(int(c))
            else:
                a = stk.pop()
                b = stk.pop()
                if c == '+':
                    stk.append(a + b)
                if c == '-':
                    stk.append(b-a)
                if c == '*':
                    stk.append(a * b)
                if c == '/':
                    stk.append(int(b / a))
        return stk[0]
```

## Resevior Sampling

Used to sample large unknown populations. Each new item added has a 1/count chance of being selected

```python
def __init__(self, nums):
    self.nums = nums
def pick(self, target):
    res = None
    count = 0
    for i, x in enumerate(self.nums):
        if x == target:
            count += 1
            chance = random.randint(1, count)
            if chance == 1:
                res = i
    return res
```

## String Subsequence

Can find the min number of subsequences of strings in some source through binary search and a dict of the indexes of the source array

```python
def shortestWay(self, source: str, target: str) -> int:
    ref = collections.defaultdict(list)
    for i,c in enumerate(source):
        ref[c].append(i)
    
    ans = 1
    i = -1
    for c in target:
        if c not in ref:
            return -1
        offset = ref[c]
        j = bisect.bisect_left(offset, i)
        if j == len(offset):
            ans += 1
            i = offset[0] + 1
        else:
            i = offset[j] + 1
            
    return ans
```

## Candy Crush

Removing adjacent duplicates is much more effective with a stack
```python
def removeDuplicates(self, s: str, k: int) -> str:
    stk = []
    for c in s:
        if stk and stk[-1][0] == c:
            stk[-1][1] += 1
            if stk[-1][1] >= k:
                stk.pop()
        else:
            stk.append([c, 1])
    ans = []
    for c in stk:
        ans.extend([c[0]] * c[1])
    return "".join(ans)
```

## Dutch Flag

[Dutch National Flag Problem](https://en.wikipedia.org/wiki/Dutch_national_flag_problem) proposed by [Edsger W. Dijkstra](https://en.wikipedia.org/wiki/Edsger_W._Dijkstra)


```python
def sortColors(self, nums: List[int]) -> None:
    """
    Do not return anything, modify nums in-place instead.
    """
    # for all idx < p0 : nums[idx < p0] = 0
    # curr is an index of element under consideration
    p0 = curr = 0
    # for all idx > p2 : nums[idx > p2] = 2
    p2 = len(nums) - 1

    while curr <= p2:
        if nums[curr] == 0:
            nums[p0], nums[curr] = nums[curr], nums[p0]
            p0 += 1
            curr += 1
        elif nums[curr] == 2:
            nums[curr], nums[p2] = nums[p2], nums[curr]
            p2 -= 1
        else:
            curr += 1
```

Binary search
Bisect library
import bisect
#Get index to insert
bisect.bisect_left(array, val, lo=0, hi=len(a))
# Does insert
bisect.insort_left(array, val, lo=0, hi=len(a))

#Find index
def find_index(a, x, start = 0, end = None):
    # Locate the leftmost value exactly equal to x.
    i = bisect.bisect_left(a, x, start, end)
    if i != len(a) and a[i] == x:
        return i
    return -1

General binary search alg
def binary_search(array, target):
    L = 0
    R = len(array) − 1
    while L <= R:
        m = (L + R) // 2
        if A[m] < T then
            L = m + 1
        else if A[m] > T then
            R = m − 1
        else:
            return m
    return unsuccessful

Counter
from collections import Counter
c = Counter(iterable)
Dictionary
D = dict()
# or
D = {}
D.get() never raises value error, returns None when empty
D[] raises a value error

Check for key
x in D 
Default dict
from collections import defaultdict 
# Dict uses f() by default for unknown values
d = defaultdict(f)
d[notSet] = f()

# can use dict or list 
d = defaultdict(list)
d = defualtdict(dict)
Data class
from dataclasses import dataclass
@dataclass
class Rectangle
   # included in sort
    left :int
    bottom :int  
    right :int
    # NOT included in sort.
    top :int = field(compare = false)
    # __init__() is autocreated
 
# Use *args to create
coords = [1,2,3,4]
rec = Rectangle(*coords)
Round towards zero
def integer_divide_towards_zero(a, b):
    return -(-a // b) if (a < 0) ^ (b < 0) else a // b
Named Tuples 
from collections import namedtuple
Entry = namedtuple("Entry",['time', 'value'])
e = Entry(time = 1, value = 2)
e[0] == e.time #True


Nonlocal v global: https://www.dotnetperls.com/nonlocal-python
Queue / Stack 
# Queue
from collections import deque
q = deque()  
q.append( x )
X = q.popleft()

# Stack
l = []
l.append( x )
X = l.pop()
Type hinting
from typing import List, Dict, Tuple, Sequence
D :Dict[int,int]
L :List[str]n
Heap
# Min heap only, use negatives for max heap.
import heapq
l = list()
# Linear time, only at startup
heapq.heapify(l)
heapq.push(l, item)
item = heapq.pop(l)
Lists
Reverse
l[::-1]
Delete list element
l[:n] + l[n+1:]

DO NOT USE 
l[:n-1] +l[n:]
(for n =1; l[n-1:]= n[-1:] = whole list)
Slice
A = [0,1,2]
a[start:stop]  # items start through stop-1                 a[0:1] = [0]
a[start:]      # items start through the end of the array   a[1:] = [1,2]
                                                            a[2:]=[2]
a[:stop]       # items from the beginning through stop-1    a[:1] = [0]
               # stop <= len(a), but a[len(a)] is index out of bounds
a[:]           # a copy of the whole array
List initialization
L = [[0 for _ in range(X)] for __ in range(Y)]
The outmost list is the leftmost access. The innermost list is the rightmost access
L[y][x]
Eg: 
    len(L)    = Y
    len(L[0]) = X
Prepend list
s.insert(0, x)
Unit test
import unittest

class basicTest(unittest.TestCase):
    def test(self):
        self.assertEqual( A, B)       

unittest.main()
Itertools

import itertools

#Return successive r length permutations of elements in the iterable.
# permutations('ABCD', r = 2) --> AB AC AD BA BC BD CA CB CD DA DB DC
itertools.permutations(iterable, r=None)

# Cartesian product of input iterables.
# product('ABCD', 'xy') --> Ax Ay Bx By Cx Cy Dx Dy
itertools.product(*iterables, repeat=1)

def phoneText(self, digits) -> List[str]:
	buttons = {'2':'abc','3':'def','4': 'ghi'} #etc
iters = [buttons[d] for d in digits]
		# itertools.product(*args) returns the
		# Cartesian product of the input iterables.
return [''.join(x) for x in itertools.product(*iters)]
Zip_longest
for a,b in zip(listA,listB):
	# Stops when first iterator is exhausted

from itertools import zip_longest
for a,b in itertools.zip_longest(a,b, [fillvalue = None])
	#Does NOT STOP
Cache annotation
from functools import lru_cache
@cache(maxsize = 128)
def some_expensive_function(x)
Algorithms
Reverse linked list in place
def reverse( head ) 
        prev = None
        current = head
        while current is not None:
            swap = current.next
            current.next = prev
            prev = current
            current = swap
        return prev

Merge 2 linked lists
# Need to iterate over previous
def mergeTwoLists(self, l1: ListNode, l2: ListNode) -> ListNode:
        outHead = ListNode()
        prev = outHead
        while l1 is not None and l2 is not None:
            if l1.val < l2.val:
                prev.next = l1
                l1 = l1.next
            else:
                prev.next = l2
                l2 = l2.next
            prev = prev.next
	  
        # Exactly one of l1 or l2 is not empty
        if l1 is None:
            prev.next = l2
        else:
            prev.next = l1
        return outHead.next

K th largest number
(K is zero indexed)
import heapq
# min heap
heap = []
counter = 0
for number in iterables:
	if counter < k:
		counter += 1
		heapq.heappush(heap,number)
	if number > heap[0]:
		heapq.heapreplace(heap, number)
K_largest = heap[0]
Rectangle overlap
Intuition: complete disjoint both vertical and horizontal

if RectA.Left < RectB.Right and RectA.Right > RectB.Left and
     RectA.Top > RectB.Bottom and RectA.Bottom < RectB.Top:
	Return OVERLAP-TRUE
(Reverse Y-vals for matrix orientation (y from top to bottom))
Depth first search
def dfs(root)
	if root is None:
return
visit(root)
mark(node)
for node in root.adjacents:
	If node.marked == false:
		dfs(node);'

Dfs():
for v in vertices:
		if(v not in visited):
			dfs-visit(v)
DFS-Visit(v):
	previsit(v) // optional
	For n in neighbors(v):
		if(n not in visited):
			// set predecessor 
			n.pi = v
			// recurse
			dfs-visit(n)
	postvist(v)

Topological sort is the opposite of the post visit order. Equivalently, topological sort is when postvisit inserts v at the front of a linked list.

Khan's topo sort
L ← Empty list that will contain the sorted elements
S ← Set of all nodes with no incoming edge
while S is not empty do
    remove a node n from S
    add n to L
    for each node m with an edge e from n to m do
        remove edge e from the graph
        if m has no other incoming edges then
            insert m into S

if graph has edges then
    return error   (graph has at least one cycle)
else 
    return L   (a topologically sorted order)

Breadth first search 
BFS always finds the shortest path on an unweighted graph.
from collections import deque

def bfs(root):
    queue = deque()

    # Mark not needed for tree
    visit_and_mark(root)

    queue.append(root)
    while len(queue) > 0:

        n = queue.popleft()

       # Mark not needed for tree
        visit_and_mark(root)
         
         # Or iterate for graph
         if n.left is not None:
             queue.append(n.left)
         if n.right is not None:
              queue.append(n.right)
Kudane's Algorithm (max contiguous subsequence)
def max_subarray(numbers):
    """Find the largest sum of any contiguous subarray. 
EMPTY ARRAY NOT ALLOWED"""
    best_sum = 0  # or: float('-inf')
    current_sum = 0
    for x in numbers:
        current_sum = max(0, current_sum + x)
        best_sum = max(best_sum, current_sum)
    return best_sum

Empty Array Allowed
    def maxSubArray(self, nums: List[int]) -> int:
        bestEndHere = -float('inf')
        bestOverall = -float('inf')
        for n in nums:
            bestEndHere = max(bestEndHere + n, n)
            bestOverall = max(bestEndHere, bestOverall)
        return bestOverall
Yield in-order traversal 
# Python 3
def inorder(t) -> Iterator[int]
    if t is not None:
        yield from inorder(t.left)
        yield t.key
        yield from inorder(t.right)
g = inorder(t)

LinkedList Queue
# remove from queue
duque():
# removal algorithm
[advance head]

# Don't forget
if not head:
    		tail = None

# add to queue
enque():
	newNode = []
	if tail:
	   tail.next = newNode
         tail = newNode
      else:
		head = new
           tail = new
Exponentiation Algorithm
def myPow(self, x: float, n: int) -> float:
    if n < 0:
        x = 1 / x
        n = -n
    if n ==0:
        return 1
    y = 1
    while n > 1:
        if n%2 ==0:
            x = x*x
            n = n // 2
        else:
            y = x * y
            x = x * x
            n = (n - 1) // 2
     return x*y
Reconstruct tree
Start from not inorder traversal
inorder / postorder:
https://leetcode.com/problems/construct-binary-tree-from-inorder-and-postorder-traversal/solution/

inorder / preorder
https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/solution/
Binary Search Tree
Insert algorithm
class Solution:
    def insertIntoBST(self, root: TreeNode, val: int) -> TreeNode:
        if not root:
            return TreeNode(val)
        
        if val > root.val:
            # insert into the right subtree
            root.right = self.insertIntoBST(root.right, val)
        else:
            # insert into the left subtree
            root.left = self.insertIntoBST(root.left, val)
        return root
Traversal of BST
Pre-order visits root first.
Post-order visits root last.
In order visits in sorted order.
Dynamic Programming
Knapsack
# A naive recursive implementation
# of 0-1 Knapsack Problem
 
# Returns the maximum value that
# can be put in a knapsack of
# capacity W 

#          Max weight                         n=Len of items
def knapSack(W: int, wt: List[int], val: List[int], n: int): 
    # Base Case
    if n == 0 or W == 0:
        return 0
 
    # If weight of the nth item is
    more than Knapsack of capacity W,
    # then this item cannot be included
    # in the optimal solution
    if (wt[n-1] > W):
        return knapSack(W, wt, val, n-1)
 
    # return the maximum of two cases:
    # (1) nth item included
    # (2) not included
    else:
        included = val[n-1] + \
           knapSack(W-wt[n-1], wt, val, n-1)
        excluded = knapSack(W, wt, val, n-1))
	   return max(included, excluded)
Count twos (or other digit)
public class Question {	
	public static int count2sInRangeAtDigit(int number, int d) {
		int powerOf10 = (int) Math.pow(10, d);
		int nextPowerOf10 = powerOf10 * 10;
		int right = number % powerOf10;
		
		int roundDown = number - number % nextPowerOf10;
		int roundUp = roundDown + nextPowerOf10;
		
		int digit = (number / powerOf10) % 10; 
		if (digit < 2) { // if the digit in spot digit is 
			return roundDown / 10;
		} else if (digit == 2) {
			return roundDown / 10 + right + 1;
		} else ( digit > 2) {
			return roundUp / 10;
		}
	}
	
	public static int count2sInRange(int number) {
		int count = 0;
		int len = String.valueOf(number).length();
		for (int digit = 0; digit < len; digit++) {
			count += count2sInRangeAtDigit(number, digit);
		}
		return count;
	}


Longest common subsequence
LCSLength(X[1..m], Y[1..n])
    C = array[m][n]
    for i := 0..m
        C[i][0] = 0
    for j := 0..n
        C[0][j] = 0
    for i := 1..m
        for j := 1..n
            // last char the same
            if X[i] = Y[j]
                C[i][j] := C[i-1][j-1] + 1
            // max with stomping front and back
            else
                C[i][j] := max(C[i][j-1], C[i-1][j])
    return C[m][n]
Calendar overlap 
import bisect

class Interval:
    def __init__(self, s, e):
        self.s = s
        self.e = e
    def __lt__(self, other):
        return self.e < other.s
    def __gt__(self, other):	
        return self.s > other.e
    def __eq__(self, other):
        return not self < other and not self > other   

class MyCalendar:
    def __init__(self):
        self.intervals = []
        
    def book(self, start: int, end: int) -> bool:
        # end - 1 to avoid overlap
        interval = Interval(start, end-1)
        index = bisect.bisect(self.intervals, interval)
        
        # find the righmost interval less than or equal 
        # to the input-interval. If equal i.e. an overlap, 
        # then we return False
        if index and self.intervals[index-1] == interval:
            return False
        self.intervals.insert(index, interval)
        return True

https://memgraph.com/blog/graph-algorithms-cheat-sheet-for-coding-interviews

## <a id="additional-resources"></a>Additional Resources
[Khan Academy's Algorithm Course](https://www.khanacademy.org/computing/computer-science/algorithms)
