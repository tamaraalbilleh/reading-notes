## Linked Lists
* Linked List - A data structure that contains nodes that links/points to the next node in the list.
* Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
* Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
* Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
* Next - Each node contains a property called Next. This property contains the reference to the next node.
* Head - The Head is a reference of type Node to the first node in a linked list.
* Current - The Current is a reference of type Node to the node that is currently being looked at. When traversing, you create a new Current variable at the Head to guarantee you are starting from the beginning of the linked list.

## What is a linked list?

A linked list is an ordered collection of data elements. A data element can be represented as a node in a linked list. Each node consists of two parts:

* data
* pointer to the next node. <br>
Unlike arrays, data elements are not stored at contiguous locations. The data elements or nodes are linked using pointers, hence called a linked list.
## Traversal
When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.
## complexity:

time: O(n) (worse case) the node which has the value that searches for it is last

space: O(1) This because there is no additional space being used

## Adding a node ( to the middle of a linked list )

* Singly Linked List

* create new node , value = (any value) , next = null

* We will traverse while the next node is not null

* before moving current to the next node, should check if the value of the next node is equal to the value where to want to add on it

* If it is, new node == current node

* Current ----> node node.Next == the node we want

* should will be new Node.Next == the node we want now both the current node and new node are pointing to the same next node. current.Next = new node

* now we have a complete link list with the newly added node

## complexity:

* time: O(n) (worse case)
* space: O(1)
## Print Out Nodes
Printing out all of the nodes in a Linked List is very similar to what we did in the Includes() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.


## What’s a Linked List, Anyway?
### Linear data structures
One characteristic of linked lists is that they are linear data structures, which means that there is a sequence and an order to how they are constructed and traversed.
## Parts of a linked list
A linked list can be small or huge, but no matter the size, the parts that make it up are actually fairly simple. A linked list is made up of a series of nodes, which are the elements of the list.
## Lists for all shapes and sizes
Even though the parts of a linked list don’t change, the way that we structure our linked lists can be quite different. Like most things in software, depending on the problem that we’re trying to solve, one type of linked lists might be a better tool for the job than another.
## Singly linked lists
are the simplest type of linked list, based solely on the fact that they only go in one direction. There is a single track that we can traverse the list in; we start at the head node, and traverse from the root until the last node, which will end at an empty null value.
## what even is Big O?
Most of us have probably heard the term “Big O Notation”, even if we had no idea what it meant the first time that we heard someone use it. My personal experience with it has always been in the context of designing algorithms (or being asked to evaluate the efficiency of an algorithm). But Big O is really all over and omnipresent within computer science.
## Growing a linked list
Instead, all we really need to do is rearrange our pointers. We know that a linked list is made up a single node, and a node always contains some data and, most importantly, a pointer to the next node or null. So, all we need to do in order to add something to our linked list is figure out which pointer needs to point to where.
* First, we find the head node of the linked list.
* Next, we’ll make our new node, and set its pointer to the current first node of the list.
* Lastly, we rearrange our head node’s pointer to point at our new node.
## To list or not to list?
Even if you don’t have to work with them every day, it’s useful to know just enough about data structures like linked lists so that you can both recognize them when you see them, and know when to reach for them when the time is right.