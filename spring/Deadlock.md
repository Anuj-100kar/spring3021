**Deadlock in Java Multithreading**

Deadlock is a situation in multithreading where two or more threads are permanently blocked because each one is waiting for the other to release a required lock. In simple terms, threads get stuck forever, and the program never continues.

* Each thread holds a lock and waits for another lock held by a different thread.
* This creates a circular wait, causing the application to freeze indefinitely.

**Locks in Java**
In Java, locks are mechanisms used to control access to shared resources in a multithreaded environment.

**Deadlock Prevention**
Deadlock prevention is a strategy used in computer systems to ensure that different processes can run smoothly without getting stuck waiting for each other forever. Think of it like a traffic system where cars (processes) must move through intersections (resources) without getting into a gridlock.

Deadlock can only happen if all four of the following conditions are met simultaneously:

* Mutual Exclusion
* Hold and Wait
* No Preemption
* Circular Wait

**Daemon Threads**
Daemon threads are background threads that provide support services to user threads. They do not prevent the JVM from exiting when all user threads have completed execution.

* Run in the background to support user threads
* Automatically terminate when user threads end
* Created using setDaemon(true) method

