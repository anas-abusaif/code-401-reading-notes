# Big O: Analysis of Algorithm Efficiency

Big O(oh) notation is used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

1. Running Time (also known as time efficiency / complexity):
  The amount of time a function needs to complete.

2. Memory Space (also known as space efficiency / complexity):
The amount of memory resources a function uses to store data and instructions.

### when calculating Big O, 4 keys must be considered.

1. Input Size
2. Units of Measurement
3. Orders of Growth
4. Best Case, Worst Case, and Average Case

# Linked Lists.

A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

There are two types of Linked List - Singly and Doubly. We will be implementing a Singly Linked List in this implementation.

### Traversal
When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.

The best way to approach a traversal is through the use of a while() loop. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash/end.

When traversing through a linked list, the Current variable will tell us where exactly in the linked list we are and will allow us to move/traverse forward until we hit the end.

Traversal Example
Let’s put a use case on our traversal. We want to check whether or not our LinkedList Includes a specific value.

The pseudo-code for an Includes is as so:
```
ALGORITHM Includes (value)
// INPUT <-- integer value
// OUTPUT <-- boolean

  Current <-- Head

  WHILE Current is not NULL
    IF Current.Value is equal to value
      return TRUE

    Current <-- Current.Next

  return FALSE
```

### Adding a Node

Order of operations is extremely important when it comes to working with a Linked List. What I mean by this is you must be careful that all references to each link/node is properly assigned.

An example can be with adding a node to a linked list. If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.

Here are the required steps to add a new node with an O(1) efficiency.

1. We can then instantiate the new node that we are adding. The values passed in as arguments into the Add() method will define what the value of the Node will be.

2. newNode.Next by default is set to null. We want to set newNode.Next property to the same location that the Head node is pointing towards. Because Head is just a reference type, we will be assigning it to the same allocation in memory as the node it is pointing too. In this case, it’s Node1.

3. At this point in the program we now “technically” have newNode at the beginning of the linked list, but we are not done yet. We now have to re-assign where Head is pointing too. Since Node1 is no longer the first node in the list, we want to re-assign Head to point at newNode.