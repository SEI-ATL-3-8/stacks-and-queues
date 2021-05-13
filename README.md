# Stacks and Queues
We are going to build a DIY version of both of these data structures. They have the following things in common:
1. A linear memory store. This could be either an array or a linked list, depending on which is more suited to your use cases. Today we'll use an array because we're more familiar with them.
2. A function that lets you add an element to the linear memory store. It doesn't really matter if you're adding it to the beginning or the end of the memory store.
3. A function that lets you remove an element from the memory store. Whether this removes the element from the beginning or end of the store depends on which end you're adding elements to.
4. A function that lets us look at the topmost element in the data structure without modifying the data structure. Here, "topmost" is defined as whichever element _would_ be removed from the store next if you were to remove one. This function is called _peek_.

Here's how stacks and queues differ from each other. Take a minute to diagram these differences out.
1. In a stack, the end of the linear store that we remove data from has to be the _same_ end that we used to insert it. (So if we put elements into the front, we take them out of the front and vice versa.)
1. In a queue, we need to remove elements from the _opposite_ end of where we inserted them. (So if we insert elements into the front, we need to remove them from the back, and vice versa.)
1. In a stack, the inserting function is called _push_ and the removing function is called _pop_.
1. In a queue, the inserting function is called _enqueue_ and the removing function is called _dequeue_.

## DIY Stack
Implement a stack object in `stack.js`. It should have 4 keys: store, pop, push, and peek.

## DIY Queue
Implement a queue object in `queue.js`. It should have 4 keys: store, enqueue, dequeue, and peek.

## Real world uses of these structures
For each of these examples, think about why the data structure is well suited!

### Stacks
1. Parentheses matching: this is a common interview question (see [here](https://www.geeksforgeeks.org/check-for-balanced-parentheses-in-an-expression/)). It's also something your text editor does continuously. Note that when solving this problem, you don't necessarily have to use a stack data structure; instead, you can use an array and just _treat it like a stack_ by only inserting data into one end, and removing it from that same end.
1. Browser history
1. Recursive function calls
1. Undo function in a text editor

### Queues
1. Messaging services
1. Long-running jobs: think of a shared printer
1. Web servers: if 100 requests get sent to your express server microseconds apart, it will process them in first-come-first-served order
