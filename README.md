# Linked-List Node Demo

This project demonstrates a simple linked-list structure using a `Node` class. Each node represents one item in a queue that stores a `name`, a `priority`, and a reference to the next node.

## What the `Node` class does

The file `PriorityQueue/Node.cs` defines:

```csharp
public class Node 
{
    public String name;
    public int priority;
    public Node next;

    public Node(String name, int priority)
    {
        this.name = name;
        this.priority = priority;
        this.next = null;
    }

    public void printNode()
    {
        Console.Write("Name: "+name+" Priority: "+priority+" ");
    }
}
```

### Fields

- `name`: a label for the item being stored
- `priority`: an integer used to decide ordering in the priority queue
- `next`: a reference to the next node in the chain

### Why `next` matters

A linked list works by connecting nodes together through `next` pointers. Each node points to the following node, forming a chain:

```text
Node A -> Node B -> Node C -> null
```

The `null` value at the end marks the end of the list.

## How this fits the priority queue

The project also contains `PriorityQueue/PriorityQueue.cs`, which uses these nodes as elements in a linked list-based queue. The queue keeps track of:

- `head`: the first node in the list
- `tail`: the last node in the list
- `length`: how many nodes are currently stored

When a new node is added, the queue inserts it in the correct place based on its `priority`, so items with higher priority are placed earlier in the list.

## Example

This code creates a node:

```csharp
Node n = new Node("Job_1", 5);
```

That creates a node object with:

- `name = "Job_1"`
- `priority = 5`
- `next = null`

If another node is added after it, the first node's `next` pointer is updated to point to the second node, creating a linked list.

## Summary

This file is a basic building block for linked-list-based data structures. It shows how data can be stored in individual node objects and linked together using references, which is the core idea behind linked lists, queues, and priority queues.
