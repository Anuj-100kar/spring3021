**Garbage Collection in Java**

Garbage Collection (GC) in Java is an automatic memory management process performed by the JVM. It helps in removing unused and unreachable objects from heap memory, which improves memory utilization and application performance. Java developers do not need to manually free memory because the JVM automatically handles object cleanup.

* Automatically removes unused objects from heap memory.
* Helps prevent memory leaks and improves memory management.
* Managed internally by the Java Virtual Machine (JVM).

Types of Garbage Collection in Java
Java Garbage Collection is mainly divided into two types based on the memory area cleaned by the JVM.

1. Minor Garbage Collection
Minor Garbage Collection occurs in the Young Generation of heap memory. It removes short-lived and unreachable objects that are recently created.

* Works on Young Generation memory.
* Faster compared to Major GC.
* Removes temporary objects quickly.

2. Major or Full Garbage Collection
Major Garbage Collection occurs in the Old Generation of heap memory. It removes long-lived objects that are no longer referenced.

* Works on Old Generation memory.
* Slower than Minor GC.
* Cleans long-lived unused objects.

**Advantages of Garbage Collection**

* It makes java memory-efficient because the garbage collector removes the unreferenced objects from heap memory.

* It is automatically done by the garbage collector (a part of JVM), so we don't need extra effort.