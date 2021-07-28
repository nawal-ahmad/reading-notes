# read 05: Linked Lists

## What is a Linked List?

# A Vocabulary/Definition List

| **Vocabulary**              | **Definition**                                              |
| --------------------------- | ----------------------------------------------------------- |
| **Linked List**             | a sequence of nodes that are connected/linked to each other |
| **Singly**                  | linked list with one reference, point to the next node      |
| **Doubly**                  | linked list with two referencesn next and previous node     |
| **Node**                    | linked list element that contains the data for each link    |
| **Next**                    | property contains the reference to the next node            |
| **Head**                    | property contains the reference to the first node           |
| **Current**                 | property contains the reference to the current node         |
| **static data structures**  | data structures that need a given size and amount of memory |
| **dynamic data structures** | data structures that need a given size and amount of memory |

![Doubly](https://miro.medium.com/max/875/1*AeMDLFUjR0w0J4n8CP4H6g.jpeg)
![Node  ](https://miro.medium.com/max/875/1*K0_eV07tJtKQSVGKfP18bw.jpeg)

- The **Next** property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately. The best way to approach a traversal is through the use of **a while() loop**. This allows us to continually check that the Next node in the list is not null. If we accidentally end up trying to traverse on a node that is null, a NullReferenceException gets thrown and our program will crash.
- **_Traversal Example_**:
- Let’s put a use case on our traversal. We want to check whether or not our LinkedList Includes a specific value.

```
The pseudo-code for an Includes is as so:

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

- **The Big O** of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

- **The Big O** of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.
  ![image](https://miro.medium.com/max/875/1*Jy5tjwrMdtpGl2ceq4f94A.jpeg)

* When constructing your code, a few things to keep in mind>> When making your Node class, consider requiring a value to be passed in to require that each node has a value.

# array vs .linked list

![image](https://miro.medium.com/max/875/1*cUehR5S18XSoVLaPNfNzlA.jpeg)
