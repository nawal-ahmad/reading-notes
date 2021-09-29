# read 05: Linked Lists

## What is a Linked List?
The Linked List: it's a sequence of nodes connected to each other, each node is a reference to the next node in the link.


`the most commonly used linked list is the singly linked list.`

- the linked list is considered as a data structure, each node links to the next node in the list.
- in a singly linked list each node has only one reference points to the next node in the list.
- in doubly linked list each node has two references, one for the next node and the other for the previous node.
- next is property for node contains the reference to the next node.
- head is a reference for the first node.

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
to traverse a linked list we depends on 'Next' property in each node to guide us to next reference.

one of the best ways to approach a traversal is by using while(), this will allow you to keep checking the Next node if its null.

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

#### linked list is a linear data structure type, that means in order to get to the end of it you have to go through all of the items in the list in order, on the other hand there is the non linear data structure in which items dont have to be arranged in order, you just can traverse the data non sequentially.

![linear](https://miro.medium.com/max/1838/1*Xokk6XOjWyIGCBujkJsCzQ.jpeg)

