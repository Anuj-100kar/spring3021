**Java Multithreading Tutorial**

Multithreading in Java is a feature that allows multiple tasks to run concurrently within the same program. Instead of executing one task at a time, Java enables parallel execution using lightweight threads. This makes applications more efficient, faster and responsive in real-world scenarios like servers, games and chat systems.

**Key Features of Multithreading**

* A thread is the smallest unit of execution in Java.
* Threads share the same memory space but run independently.
* Java provides the Thread class and Runnable interface to create threads.
* Multithreading ensures better CPU utilization by executing tasks simultaneously.
* Synchronization is needed to prevent data inconsistency when threads share resources.

# Multithreading allows concurrent execution of two or more parts of a program for maximum CPU usage. It improves application performance and responsiveness.

**Difference between Multiprocessing and Multithreading**

**Multiprocessing**
Multiprocessing is a system that has more than one or two processors. In Multiprocessing, CPUs are added to increase the computing speed of the system. Because of Multiprocessing, There are many processes are executed simultaneously.

* Increases computing power by utilizing multiple processors.

* Suitable for tasks that require heavy computational power.

**Multithreading**
Multithreading is a system in which multiple threads are created of a process for increasing the computing speed of the system. In multithreading, many threads of a process are executed simultaneously and process creation in multithreading is done according to economical. 

* Multiple threads run within the same process

* Shares memory, so communication is faster

**Processes vs Threads**
A process is an independent program in execution, 
while a thread is a lightweight sub-process.

**Process**

Process is a program that is currently in execution within an operating system. It operates in an independent environment and is managed by the OS for proper scheduling and execution. Processes form the basis of program execution in a multitasking system. Its Properties are:

* Each process has a unique Process ID (PID) for identification.
* Every process moves through different states such as new, ready, running, waiting, and terminated.
* Processes communicate with each other using Inter-Process Communication (IPC) methods.

**Thread**

Thread is a smallest unit of execution within a process. It enables a program to perform multiple tasks concurrently while sharing the same memory and resources. Threads improve application performance and responsiveness in multitasking environments. Its properties are:

* Each thread has its own Thread ID (TID) for identification.
* A thread also moves through states such as new, runnable, running, waiting, and terminated.
* Threads within the same process share memory and resources, enabling faster communication.
* Context switching can occur between threads to allow multiple tasks to execute efficiently.

**Create Threads in Java**
We can create threads in java using two ways
1. By Extending Thread Class 
2. Using Runnable Interface

**Life Cycle of a Thread**
During its thread life cycle, a Java thread transitions through several states from creation to termination.

New State
Runnable State
Blocked State
Waiting State
Timed Waiting State
Terminated State

**Thread Methods**
Java provides built-in methods like start(), run(), sleep() and join() to manage thread execution and control its behavior.

* start() Method
* suspend() Method
* stop() Method
* sleep() Method
* join() Method

