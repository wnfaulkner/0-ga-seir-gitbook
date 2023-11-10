# Linked Lists

A linked list a data structure, used for fast and memory-efficient insertions and deletions. Unlike arrays, which are single objects, a linked list is a collection of _**node**_ objects that are linked via _**pointers**_ aka _references_.

## Nodes

Each _**node**_ is an object that has the following properties:

* **data** \(sometimes called _item_\): the piece of data to be stored
* **next**: the location of the next node in the list
* **previous** _\(optional\)_: the location of the previous node in the list, if it is a _**doubly linked**_ list

## Singly vs. Doubly Linked Lists

Singly linked lists only have references to the next item in the list, so they look like this:

![http://www.lisha.ufsc.br/teaching/sce/ine6511-2003-2/work/gp/lists\_files/image001.gif](http://www.lisha.ufsc.br/teaching/sce/ine6511-2003-2/work/gp/lists_files/image001.gif)

While doubly linked lists _also_ have references to the previous node, so they look like this:

![https://www.java2blog.com/wp-content/uploads/2017/09/DoublyLinkedList.png](https://www.java2blog.com/wp-content/uploads/2017/09/DoublyLinkedList.png)

## Wait, why not use arrays instead?

In lower level languages, arrays are allocated in **blocks.** Therefore, arrays are static in size and can only hold a specific data type. Linked lists store data in the **heap**, meaning that the data can be stored in an unorganized manner. Since each node points to the next one, it's still possible to maintain the list structure.

## Heads or tails?

To indicate the start and end of the list, we call the first node the _**head**_ and the last node the **\*tail**. The head node doesn't have another node pointing to it, and the tail node doesn't point anywhere \(in code, this looks like setting `next` to `null` or the equivalent\).

![https://hackernoon.com/hn-images/1\*GOKmkucFHN\_gmTMUtyC2sQ.png](https://hackernoon.com/hn-images/1*GOKmkucFHN_gmTMUtyC2sQ.png)

There is also such a thing as a _**circular linked list**_ which doesn't have a true head or tail, though you can designate a head and/or tail if it makes sense in your application of the list:

![https://static.packt-cdn.com/products/9781783554874/graphics/4874OS\_05\_18.jpg](https://static.packt-cdn.com/products/9781783554874/graphics/4874OS_05_18.jpg)

When coding a linked list, you will generally have a `Node` objects to represent each piece of data \(and the pointers\), as well as a `LinkedList` object that stores the head, tail, and all of the list's functionality \(which will be dependent on what type of linked list it is and how you plan to use it\).

