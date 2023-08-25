---
cssclass:
aliases:
tags:
- Java
---
**[[Java#Java Memory Management|HOME [Java]]]**

---
## Generational Garbage Collection
There are many **GC algorithms** that run in the background, of which one of them is <mark class="hltr-lightgreen">mark and sweep</mark>.

#### Mark and Sweep Algorithm
Any garbage collection algorithm must perform 2 basic operations:
1. it should be able to detect all the unreachable objects and;
2. it must reclaim the heap space used by the garbage objects and make the space available again to the program.

**Mark phase**
When an object is created, its mark bit is set to `0`(false). In the Mark phase, we set the marked bit for all the reachable objects (or the objects which a user can refer to) to `1`(true). Now to perform this operation we simply need to do a graph traversal, a depth-first search approach would work for us. Here we can consider every object as a node and then all the nodes (objects) that are reachable from this node (object) are visited and it goes on till we have visited all the reachable nodes.
$\quad$▪ The root is a variable that refers to an object and is directly accessible by a local variable. We will assume that we have one root only.
$\quad$▪ We can access the mark bit for an object by ‘markedBit(obj)’.

**Algorithm:** Mark phase
```
Mark(root)
If markedBit(root) = false then
                     markedBit(root) = true
                                       For each v referenced by root
                                       Mark(v)
```
>[!NOTE|clean collapse no-t]
> $\qquad$**Note:** If we have more than one root, then we simply have to call `Mark()` for all the root variables.

**Sweep phase**
As the name suggests it “*sweeps*” the unreachable objects i.e. it clears the heap memory for all the unreachable objects. All those objects whose marked value is set to false are cleared from the heap memory, for all other objects (reachable objects) the marked bit is set to true.

Now the mark value for all the reachable objects is set to false since we will run the algorithm (if required) and again we will go through the mark phase to mark all the reachable objects.

**Algorithm:** Sweep phase
```
Sweep()
For each object p in heap
If markedBit(p) = true then
                  markedBit(p) = false
                                 else
                                     heap.release(p)
```
The mark-and-sweep algorithm is called a <mark class="hltr-lightblue">tracing garbage collector</mark> because it traces out the entire collection of objects that are directly or indirectly accessible by the program.

>[!EXAMPLE]-
> **A.** All the objects have their marked bits set to false.
> ![[Pasted image 20230620153523.png|center wm-tl]]
> **B.** Reachable objects are marked true
> ![[Pasted image 20230620153540.png|center wm-tl]]
> **C.** Nonreachable objects are cleared from the heap.
> ![[Pasted image 20230620153555.png|center wm-tl]]

<br>

# 
---
- [Mark-and-Sweep: Garbage Collection Algorithm - GeeksforGeeks](https://www.geeksforgeeks.org/mark-and-sweep-garbage-collection-algorithm/)