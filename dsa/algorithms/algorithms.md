Algorithm must be

1. Defined - there must be a specific sequence to perform a task
2. Unambiguous - there is "correct" and "incorrect" interpretation of the steps
3. Implementable - it can be performed in code or using hardware

## Roadmap

1. Arrays
2. Hashmaps
3. Stack
4. Queue
5. Linked List
6. Trees
7. Binary Search Tree
8. Sliding Window
9. Tries
10. Backtracking
11. Heap / Priority Queue
12. Graps

## Basic data types

### Stack

A stack is an abstract data type that serves as a collection of elements. Our stack will have several methods:

-   `push` - adds an element to the stack (enqueue)
-   `pop` - removes an element from the stack (dequeue)
-   `peek` - returns the top element of the stack
-   `size` - returns the size of the stack

The order in which elements come off a stack gives rise to its alternative name, LIFO (last in, first out).

Think of a stacked booked. The first book that's stacked will be the last book that's able to be removed from the stack. Consequently, the last book to be put in the stack is easier to get because it's in the top.

All stack operations are O(1) operations.

### Queue

A queue is a abstract data type that serves as an ordered collection of elements. A simple queue typically has several operations:

-   push - adds an item to the tail of the queue
-   pop - removes and returns an item from the head of the queue
-   peek - returns an item from the head of the queue
-   size - returns the number of items in the queue

The order in which elements come off a queue gives rise to its alternative name, FIFO (first one, first out).

Think of a line to get tickets. The first person to get in line will be the first person to receive a ticket and get out of the line.

#### Linked List

A linked list is a linear data structure where elements are not stored next to each other in memory. The elements in a linked list are linked using pointers.

Linked lists can be compared with the standard list or array. Items in a normal list are stored next to each other in memory, and to get an item from the list, we use a numbered index.

In a linked list, there are no indices. We need to walk each node of the list because the only way to get the location of the second item in a linked list is to look at the pointer of the first item.

### Tree

A tree is a widely used data structure that simulates a hierarchical tree structure, wit a root value and subtrees of children with a parent node, represented as a set of linked nodes.

A tree is a collection of nodes starting at a root or head node, similar to how out Linked List was a collection of nodes starting with a head (root). The big difference between a LL and a tree is that a tree's nodes can have multiple children instead of just one.

A generic tree has the following rules:

-   Each node has a value and a list of children
-   Children can only have a single parent
-   Duplicate values are allowed, multiple nodes can have the same value

Linked List

```
node -> node -> node
```

Tree

```
            > node
      > node
            > node
> node
            > node
      > node
            > node
```

### Binary trees

Trees aren't particularly useful data structures unless they're ordered in some way. One of the most common types of ordered tree is a Binary Search Tree or BST.

Binary search tree has additional constrains:

-   Instead of a list of children, each node has at most 2 children, a right and a left child
-   The left child's value must be less than its parent's value
-   The right child's value must be greater than its parents
-   The two nodes in the BST can have the same value

Why?

By ordering the tree this way, we can add, remove, and find nodes very quickly.

#### Hash maps

A hash map or a hash table is a structure that maps keys to values. A hash table uses a hash function to compute an index into an array of buckets, from which the desired value can be found. During lookup, the key is hashed and the resulting hash indicates where the corresponding value is stored.

Ideally the hash function will assign each key to a _unique_ bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key. Such collisions are typically accommodated for somehow.

In a well-built hash map, the average computational cost or each lookup, insertion, and deletion is independent of the number of elements stored in the table. In other words, all three basic operations are O(1).

Hash maps are just key -> value stores.

### Tries

A trie is represented as a nest of dictionaries where each key is a character, and it maps to the next character in the word.

The words "hello," "help," and "hi" would be represented as:

```json
{
	"h": {
		"e": {
			"l": {
				"l": {
					"o": {
						"*": True
					}
				},
				"p": {
					"*": True
				}
			}
		},
		"i": {
			"*": True
		}
	}
}
```

A trie is also often referred to as a prefix tree because it can be used to efficiently find all the words that start with a given prefix.
