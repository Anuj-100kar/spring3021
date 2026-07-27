**Synchronization in Java**

Synchronization is used to control the execution of multiple processes or threads so that shared resources are accessed in a proper and orderly manner. It helps avoid conflicts and ensures correct results when many tasks run at the same time.

* It controls the access of shared resources.
* It avoids data inconsistency.
* It ensures proper execution of processes.

**Ways to Achieve Synchronization**
There are three main ways to achieve synchronization.

1. Synchronized Methods
Synchronized methods are used to lock an entire method so that only one thread can execute it at a time for a particular object. This ensures safe access to shared data but may reduce performance due to full method locking.

* Locks the whole method, not just a part of it.
* Uses the object-level lock (instance lock).

2. Synchronized Blocks
Synchronized blocks allow locking only a specific section of code instead of the entire method. This makes the program more efficient by reducing the scope of synchronization.

Locks only the critical section of code, not the entire method.
Provides better performance due to fine-grained control.

3. Static Synchronization
Static synchronization is used when static data or methods need to be protected in a multithreaded environment. It ensures that only one thread can access the class-level resource at a time.

Locks at the class level instead of the object level.
Shared across all instances of the class.

# Types of Synchronization

1. Process Synchronization
Process synchronization is a fundamental concept in operating systems that ensures multiple processes or threads can execute safely while sharing common resources. Process Synchronization is a technique used to coordinate the execution of multiple processes. It ensures that the shared resources are safe and in order.

* Prevents race conditions by controlling access to shared resources.
* Ensures data consistency and integrity in concurrent execution.
* Uses mechanisms like semaphores, mutex locks, and monitors for coordination.

2. Thread Synchronization in Java
Thread Synchronization is used to coordinate and ordering of the execution of the threads in a multi-threaded program. There are two types of thread synchronization are mentioned below:

* Mutual Exclusive
* Cooperation (Inter-thread communication in Java)

**Volatile Keyword**
The volatile keyword in Java ensures that all threads have a consistent view of a variable's value. It prevents caching of the variable's value by threads, ensuring that updates to the variable are immediately visible to other threads.

Working of Volatile Modifier:

* It applies only to variables.
* volatile guarantees visibility i.e. any write to a volatile variable is immediately visible to other threads.
* It does not guarantee atomicity, meaning operations like count++ (read-modify-write operations) can still result in inconsistent values

**Inter-thread Communication in Java**

Inter-thread communication in Java enables threads to coordinate their execution by signaling each other during runtime. It is mainly used when multiple threads depend on shared resources or need to work in a specific sequence.

* Helps avoid busy waiting and improves resource utilization
* Ensures proper execution order among dependent threads
* Commonly used in producer-consumer type problems

**Polling**
Polling is the process of repeatedly checking a condition in a loop until it becomes true. Once the condition is satisfied, the required action is performed. It is commonly used when one thread waits for another to produce or update data.

* Problem with Polling
* Wastes CPU cycles due to continuous condition checking
* Reduces efficiency and slows down overall execution
* Keeps the thread busy instead of allowing other tasks to run

# How Java Multithreading Handle Polling
Java avoids polling by using built-in communication methods that allow threads to wait efficiently instead of continuously checking a condition. These methods are defined in the Object class and must be used within a synchronized context. 

* wait(): Releases the lock and puts the thread into a waiting state until notified
* notify(): Wakes up one waiting thread (does not release the lock immediately)
* notifyAll(): Wakes up all waiting threads on the same object

# Producer-Consumer Problem
The Producer-Consumer problem involves two threads where one (producer) adds data to a shared queue and the other (consumer) removes data from it. Proper coordination is required to ensure the producer doesn’t add when the queue is full and the consumer doesn’t remove when it’s empty.

* Uses wait(), notify(), and notifyAll() for synchronization
* Ensures efficient communication between producer and consumer threads
* Prevents issues like data inconsistency and unnecessary waiting

