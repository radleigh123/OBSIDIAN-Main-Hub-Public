---
cssclass: tbl-nalt, t-w
aliases:
tags:
- Java
- Java/Collection/Queue/PriorityQueue
---
**[[Java#Collections|HOME [Java]]]**

---
## PriorityQueue class
is used when the objects are supposed to be processed based on the priority. The PriorityQueue is based on the priority heap. The elements of the priority queue are ordered according to the natural ordering, or by a Comparator provided at queue construction time, depending on which constructor is used.

![[Pasted image 20230627100227.png|center wm-tl]]

A few important points on PriorityQueue are as follows: 
- doesn’t permit null.
- We can’t create a PriorityQueue of Objects that are non-comparable
- are unbound queues.
- The head of this queue is the least element with respect to the specified ordering. If multiple elements are tied for the least value, the head is one of those elements — ties are broken arbitrarily.
- Since PriorityQueue is not thread-safe, java provides `PriorityBlockingQueue` class that implements the `BlockingQueue` interface to use in a java multithreading environment.
- The queue retrieval operations `poll`,  `remove`,  `peek`, and element access the element at the head of the queue.
- It provides `O(log(n))` time for add and poll methods.
- It inherits methods from `AbstractQueue`, `AbstractCollection`, `Collection`, and `Object` class.

| <center>return `true` or `null`</center> | <center>throw exception</center> |
| ---------------------------------------- | -------------------------------- |
| offer()                                  | add()                            |
| peek()                                   | element()                        |
| poll()                                   | remove()                         | 

**Example**:
>[!aside|right]-
> Priority queue: [1, 2, 3, 4]
> peek(): 1
> poll(): 1
> &nbsp;
> Priority queue: [2, 4, 3]
> contains 3?: true        
> size: 3
> empty?: true

```java
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        Queue<Integer> q = new PriorityQueue<>();
        q.add(1);
        q.add(2);
        q.add(3);
        q.add(4);

        System.out.println("Priority queue: " + q);
        System.out.println("peek(): " + q.peek());
        System.out.println("poll(): " + q.poll());

        System.out.println("\nPriority queue: " + q);
        System.out.println("contains 3?: " + q.contains(3));
        System.out.println("size: " + q.size());
        q.clear();
        System.out.println("empty?: " + q.isEmpty());
    }
}
```

>[!EXAMPLE]+ Real Time Implementations
> - **Task Scheduling**: In operating systems, priority queues are used to schedule tasks based on their priority levels. For example, a high-priority task like a critical system update may be scheduled ahead of a lower-priority task like a background backup process.
> - **Emergency Room:** In a hospital emergency room, patients are triaged based on the severity of their condition, with those in critical condition being treated first. A priority queue can be used to manage the order in which patients are seen by doctors and nurses.
> - **Network Routing**: In computer networks, priority queues are used to manage the flow of data packets. High-priority packets like voice and video data may be given priority over lower-priority data like email and file transfers.
> - **Transportation**: In traffic management systems, priority queues can be used to manage traffic flow. For example, emergency vehicles like ambulances may be given priority over other vehicles to ensure that they can reach their destination quickly.
> - **Job Scheduling**: In job scheduling systems, priority queues can be used to manage the order in which jobs are executed. High-priority jobs like critical system updates may be scheduled ahead of lower-priority jobs like data backups.
> - **Online Marketplaces**: In online marketplaces, priority queues can be used to manage the delivery of products to customers. High-priority orders like express shipping may be given priority over standard shipping orders.

Overall, priority queues are a useful data structure for managing tasks and resources based on their priority levels in various real-world scenarios.

<br>

# 
---
- [PriorityQueue (Java Platform SE 8 ) (oracle.com)](https://docs.oracle.com/javase/8/docs/api/java/util/PriorityQueue.html)
- [PriorityQueue in Java - GeeksforGeeks](https://www.geeksforgeeks.org/priority-queue-class-in-java/)