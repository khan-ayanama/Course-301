# Lecture:03

`Processing:` Program under execution
`Threading:` Lightweight process.

## MULTITHREADING

Multithreading is a programming and execution model that allows multiple threads to exist within the context of a single process. A thread is the smallest unit of execution, and multithreading enables concurrent execution of multiple threads within the same program. Here are key features and characteristics of multithreading:

`Concurrency:` Multithreading enables concurrent execution of multiple threads, allowing them to run independently and share the same resources, such as memory space.

`Thread:` A thread is a lightweight, independent unit of execution within a process. Multiple threads within a process share the same resources but have their own execution stack and program counter.

`Parallelism:` Multithreading can lead to parallelism, where multiple threads execute simultaneously on multiple processors or CPU cores, taking advantage of modern multicore architectures.

`Thread Creation and Termination:` Threads can be created and terminated dynamically during the execution of a program. This flexibility allows for dynamic adaptation to changing workloads.

`Thread Synchronization:` Since threads within a process share resources, synchronization mechanisms are required to coordinate their execution and prevent conflicts. Common synchronization tools include locks, semaphores, and barriers.

`Thread Communication:` Threads often need to communicate with each other. Inter-thread communication can be achieved through shared data structures or inter-process communication mechanisms, such as message passing.

`Efficiency:` Multithreading can improve the efficiency of a program by allowing the overlap of computation and I/O operations. While one thread is waiting for I/O, another thread can continue with computation.

`Responsive User Interface:` In applications with graphical user interfaces (GUIs), multithreading is often used to ensure that the user interface remains responsive while background tasks are being performed.

`Task Parallelism and Data Parallelism:` Multithreading supports both task parallelism (multiple threads perform different tasks) and data parallelism (multiple threads perform the same task on different data sets).

`Complexity:` Multithreading introduces additional complexity to program design and debugging. Proper synchronization and coordination are essential to avoid issues such as race conditions and deadlocks.

Multithreading is widely used in various types of software development, including desktop applications, server applications, and parallel computing. Many modern programming languages and operating systems provide support for multithreading, making it easier for developers to implement concurrent and parallel solutions.

### Theads can run on different processors but share same memory

Threads within the same process share the same address space and resources, and they do not have the same level of isolation as processes. Even if threads from a single process are scheduled to run on different processors, they still share the same memory space and data. This lack of isolation means that threads within the same process can directly access and modify each other's data.

In contrast, multiprocessing involves separate processes running independently, each with its own memory space. Processes are isolated from each other, and communication between them typically requires inter-process communication mechanisms.

While threads in a single process can be scheduled on different processors for concurrent execution, they still operate within the same address space. This shared memory space simplifies communication between threads, but it also means that developers need to carefully manage access to shared data to avoid race conditions and other synchronization issues.

In summary, the isolation between threads within a single process is not as strong as the isolation between separate processes in a multiprocessing environment. Threads within the same process have shared memory and resources, making communication and data sharing easier but requiring additional care to ensure proper synchronization and avoid conflicts

## Difference between multiprogramming vs multiprocessing vs multithreading

### Multiprogramming

`Definition:` Multiprogramming is an operating system technique that allows multiple programs to be loaded into memory at the same time.
`Objective:` The goal of multiprogramming is to keep the CPU busy at all times by switching between different programs as needed.
`Resource Sharing:` Multiple programs share the CPU time through time-sharing or time-slicing.
`Concurrency:` Programs run concurrently, but only one program is actively executing at a given moment.

### Multiprocessing

`Definition:` Multiprocessing involves the use of multiple processors or cores in a computer system, allowing multiple tasks to be executed simultaneously.
`Objective:` The primary goal is to improve overall system performance by parallelizing the execution of tasks across multiple processors.
Resource Sharing: Each processor operates independently and has its own set of resources, such as registers and cache.
`Concurrency:` True parallelism is achieved as different tasks execute simultaneously on separate processors.

### Multithreading

`Definition:` Multithreading is a programming and execution model that allows multiple threads to exist within the context of a single process.
`Objective:` The goal is to provide concurrent execution and improved responsiveness by allowing multiple threads to run independently.
Resource Sharing: Threads within a process share the same address space and resources, such as memory.
`Concurrency:` Threads can execute concurrently within the same process, even on a single processor. In a multiprocessor system, true parallelism is achieved as threads run on separate processors.

`In summary:`

* Multiprogramming focuses on keeping the CPU busy by switching between multiple programs on a single processor.
* Multiprocessing involves the use of multiple processors or cores for true parallel execution of tasks, improving overall system performance.
* Multithreading allows multiple threads to exist within the context of a single process, providing concurrent execution and improved responsiveness. In a multiprocessor system, threads can run on separate processors, achieving true parallelism.
* Each of these concepts addresses different aspects of concurrent computing, and their use depends on the requirements and characteristics of the applications and systems.

`Note:` When only one processor present multi-threading is similar to multiprgramming. In a multiprogramming scenario, each program is more self-contained, whereas in multithreading, threads within the same process have a higher degree of interaction due to their shared resources.
