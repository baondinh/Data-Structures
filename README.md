# Data-Structures

## B-trees:

B-trees are balanced trees and unlike binary trees which have nodes with at most two paths (left and right), B-tree nodes can have many paths. Thus, a B-tree is often referred to as a "multi-way tree."

**Determining Nodes:** A B-tree of order m is a tree where each node has
- At most 2m values and 2m + 1 children for internal nodes
- At least m values and m + 1 children for internal nodes
- The root is an exception and may have as few as one value

**Nodes with Keys and Children:** Each node in a B-tree stores a sorted set of keys (like numbers or names).  These keys divide the node's children into ranges. For example, a node with keys 5 and 12 might have three children representing values less than 5, between 5 and 12, and greater than 12.

Balanced Structure: B-trees are "self-balancing."  This means they adjust their structure during insertions and deletions to ensure that all leaf nodes (the nodes at the very bottom with no children) are the same distance from the root (the top node). This balance is crucial for efficient operations.

Why B-trees? Efficient Data Access

B-trees excel at storing and retrieving large amounts of data, especially when that data is too big to fit entirely in your computer's main memory. Here's why:

Optimized for Disks and Large Data:  B-trees are designed to work well with how data is stored on disks (hard drives, SSDs). Reading a large chunk of data from a disk at once is much faster than reading it in small bits. B-trees group data in ways that make these "block reads" very efficient.

Logarithmic Search Time O(log n): With a perfect balanced nature, B-tree searching is very quick and efficient. In the worst case, you only need to traverse a few levels of the tree to find your data. This is known as "logarithmic time complexity."  In simpler terms, as the size of your data grows, the time to search doesn't increase as drastically.

## 2-3 Tree: 
A 2-3 tree is essentially a B-tree of order m = 1. As such, it has at most 2 entries and 3 children and at least 1 entry and 2 children for for internal nodes. 
Like other B-trees, the 2-3 tree excels at storing and retrieving large amounts of data. 
It has logarithmic time efficiency O(log n) since tree traversal is dependant on the height of the true. 


