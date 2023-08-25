---
cssclass:
aliases:
tags:
- Java
---
**[[Java#Java Memory Management|HOME [Java]]]**

---
The Java HotSpot VM includes three different types of collectors, each with different performance characteristics.

- The **serial collector** uses a single thread to perform all garbage collection work, which makes it relatively efficient because there is no communication overhead between threads. It is best-suited to single processor machines, because it cannot take advantage of multiprocessor hardware, although it can be useful on multiprocessors for applications with small data sets (up to approximately 100 MB). The serial collector is selected by default on certain hardware and operating system configurations, or can be explicitly enabled with the option `-XX:+UseSerialGC`.
- The **parallel collector** (also known as the _throughput collector_) performs minor collections in parallel, which can significantly reduce garbage collection overhead. It is intended for applications with medium-sized to large-sized data sets that are run on multiprocessor or multithreaded hardware. The parallel collector is selected by default on certain hardware and operating system configurations, or can be explicitly enabled with the option `-XX:+UseParallelGC`.
	- Parallel compaction is a feature that enables the parallel collector to perform major collections in parallel. Without parallel compaction, major collections are performed using a single thread, which can significantly limit scalability. Parallel compaction is enabled by default if the option `-XX:+UseParallelGC` has been specified. The option to turn it off is `-XX:-UseParallelOldGC`.
- The **mostly concurrent collector** performs most of its work concurrently (for example, while the application is still running) to keep garbage collection pauses short. It is designed for applications with medium-sized to large-sized data sets in which response time is more important than overall throughput because the techniques used to minimize pauses can reduce application performance. The Java HotSpot VM offers a choice between two mostly concurrent collectors. Use the option `-XX:+UseConcMarkSweepGC` to enable the CMS collector or `-XX:+UseG1GC` to enable the G1 collector.

> To find out which is the computer's default collector
> `-XX:+PrintCommandLineFlags`

<br>

# 
---
- [Available Collectors (oracle.com)](https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/collectors.html)
- [HotSpot Virtual Machine Garbage Collection Tuning Guide (oracle.com)](https://docs.oracle.com/en/java/javase/20/gctuning/introduction-garbage-collection-tuning.html#GUID-326EB4CF-8C8C-4267-8355-21AB04F0D304)
- [The Mostly Concurrent Collectors (oracle.com)](https://docs.oracle.com/javase/8/docs/technotes/guides/vm/gctuning/concurrent.html#mostly_concurrent)