# Lecture:02

## Types of OS

### Single Process OS

A single-process operating system, also known as a single-user operating system, is an operating system that allows only one user to execute one task at a time. This means that the CPU is dedicated to running a single program or process until it completes or the user decides to switch to another task.

In a single-process OS, there is no multitasking capability, and resources are not shared among multiple users or processes simultaneously. Examples of single-process operating systems include early versions of MS-DOS and some simple embedded systems.

These systems are generally straightforward and suitable for simpler tasks where multitasking is not a requirement. However, they lack the efficiency and flexibility of modern multi-process and multi-user operating systems commonly used today.

`Example:` MS Dos

### Batch Processing OS

Batch processing operating systems are designed to execute tasks in large batches without manual intervention. In a batch processing system, users submit their jobs in the form of batches to the computer operator. The operating system then processes these batches one after another without requiring user interaction during the execution of individual jobs.

Here are some key characteristics of batch processing operating systems:

`No User Interaction during Job Execution:` Once a batch of jobs is submitted, the operating system takes control and executes the jobs in sequence. Users do not interact with the system until the entire batch is processed.

`Efficient Resource Utilization:` Batch processing systems aim for efficient use of resources. The operating system schedules and executes jobs based on their priority, resource requirements, and other factors.

`Job Queues:` Jobs are typically organized into queues based on their priority and the order in which they were submitted. The operating system selects jobs from these queues for processing.

`Limited Interactivity:` Batch processing systems are not designed for interactive use. They are suitable for scenarios where large volumes of similar tasks need to be processed without user intervention.

`Output:` Once a batch of jobs is completed, the system provides output, often in the form of printed reports or saved files. Users can then retrieve their results.

Historically, early mainframe systems often used batch processing for tasks such as payroll processing, scientific simulations, and large-scale data processing.

`Example:` ATLAS

### Multi Programming OS

Multiprogramming is a technique used in operating systems that allows multiple programs to be executed concurrently on a computer. The key idea behind multiprogramming is to keep the CPU busy at all times by switching between different programs. This enhances overall system efficiency and throughput.

Here are some key characteristics of a multiprogramming operating system:

`Concurrent Execution:` In a multiprogramming environment, multiple programs are loaded into memory simultaneously. The CPU switches between these programs, giving the illusion of concurrent execution.

`CPU Scheduling:` The operating system uses a CPU scheduler to determine which program to execute next. This decision is often based on priority, time-sharing, or other scheduling algorithms.

`Memory Management:` The operating system must manage the allocation and deallocation of memory for multiple programs. This includes ensuring that each program has enough memory to execute and preventing them from interfering with each other.

`I/O Operations:` While one program is waiting for I/O operations to complete (such as reading from or writing to a disk), the CPU can be switched to another program, allowing for more efficient use of system resources.

`Increased Throughput:` Multiprogramming increases overall system throughput by keeping the CPU busy with the execution of different programs, even if one or more programs are waiting for I/O operations to complete.

`Context Switching:` The process of saving the state of one program and restoring the state of another program is known as context switching. This is a critical aspect of multiprogramming and is managed by the operating system.

Multiprogramming is a fundamental concept in modern operating systems and is essential for achieving high levels of efficiency and responsiveness. It allows for better utilization of system resources and improved user experience by providing the appearance of concurrent execution.

`Example:` THE

### Multitasking OS

Multitasking is a capability of an operating system that allows multiple tasks or processes to run concurrently on a computer. Here are key features of a multitasking operating system:

`Concurrent Execution:` Multitasking enables the execution of multiple tasks simultaneously. This could involve running multiple applications, processes, or threads concurrently.

`Time Sharing:` The operating system allocates a specific time slice or quantum to each task, allowing them to execute for a short period. This gives the appearance of parallel execution, even on a single-core processor.

`Task Switching:` The operating system regularly switches between tasks, known as context switching. This involves saving the state of the currently executing task and restoring the state of the task that will resume execution.

`User Interaction:` Multitasking systems allow users to interact with multiple applications or perform various tasks concurrently. For example, a user might be writing a document, listening to music, and downloading a file, all at the same time.

`Resource Management:` The operating system manages system resources such as CPU time, memory, and input/output devices to ensure fair and efficient utilization among competing tasks.

`Foreground and Background Tasks:` Some tasks run in the foreground, where users interact directly with them, while others operate in the background, performing tasks without direct user input.

`Priority Scheduling:` Multitasking systems often use priority-based scheduling to determine the order in which tasks are executed. Higher priority tasks are given preference.

`Responsive User Interface:` Multitasking enhances the responsiveness of the user interface by allowing users to switch between applications seamlessly.

Modern desktop and server operating systems, such as Windows, macOS, and Linux, incorporate multitasking capabilities to handle the diverse and concurrent needs of users and applications. This capability is crucial for optimizing system performance and user experience.

`Example:` CTSS

### Multiprocessing OS

A multiprocessing operating system is designed to take advantage of multiple processors or CPU cores in a computer system, allowing for concurrent execution of multiple tasks or processes. Here are some key features and characteristics of multiprocessing operating systems:

`Parallel Execution:` Multiprocessing OS allows multiple tasks or processes to run in parallel, each on its own processor or core. This parallel execution enhances overall system performance and throughput.

`Task Distribution:` The operating system is responsible for distributing tasks across the available processors. This distribution can be based on load balancing to ensure that each processor is utilized efficiently.

`Improved Performance:` Multiprocessing systems can significantly improve system performance by dividing the workload among multiple processors, reducing the time it takes to execute tasks.

`Parallel Processing:` In addition to parallel execution of multiple tasks, multiprocessing systems can also support parallel processing within individual tasks. This is particularly beneficial for computationally intensive applications that can be divided into smaller subtasks.

`Scalability:` Multiprocessing provides scalability, allowing a system to handle an increased workload by adding more processors. This is crucial for systems that need to adapt to growing demands.

`Synchronization:` To ensure proper coordination and communication between multiple processors, multiprocessing OS includes mechanisms for synchronization. This prevents conflicts and ensures that tasks are executed correctly.

`Resource Sharing:` Resources such as memory and input/output devices need to be shared among multiple processors. The operating system manages resource access and prevents conflicts through proper synchronization.

`Fault Tolerance:` Some multiprocessing systems incorporate fault-tolerant features to ensure system stability even in the presence of hardware failures. Redundancy and error recovery mechanisms may be employed.

Multiprocessing is widely used in servers, high-performance computing clusters, and certain types of desktop computers, especially those designed for demanding tasks such as scientific simulations, video rendering, and complex data analysis. Modern operating systems like Linux, Windows, and macOS include support for multiprocessing.

`Example:` Windows

### Distributed OS

A distributed operating system is an operating system that runs on multiple machines and enables them to work together as a single, integrated system. Here are some key features and characteristics of distributed operating systems:

`Resource Sharing:` In a distributed OS, resources such as files, applications, and peripheral devices can be shared across multiple machines. This enables more efficient utilization of resources and improved overall system performance.

`Transparency:` Distributed operating systems aim to provide transparency to users and applications. This means that the distribution of resources is hidden from users, and they interact with the system as if it were a single, centralized entity.

`Communication:` Communication is a critical aspect of distributed systems. Processes running on different machines need to communicate with each other, and the operating system provides mechanisms for inter-process communication (IPC) to facilitate this.

`Fault Tolerance:` Distributed systems often incorporate fault-tolerant mechanisms to ensure system reliability in the face of hardware or software failures. Redundancy, replication, and recovery strategies may be employed.

`Scalability:` Distributed operating systems can be easily scaled by adding more machines to the network. This scalability is beneficial for handling increasing workloads and accommodating growth.

`Concurrency:` Multiple processes can run concurrently on different machines within a distributed system. The operating system manages the coordination and synchronization of these processes.

`Security:` Ensuring the security of distributed systems is a complex task. Distributed operating systems implement security measures to protect data and resources from unauthorized access or malicious attacks.

`Location Transparency:` Users and applications in a distributed system may not be aware of the physical location of resources. This location transparency allows for flexibility in resource allocation and management.

`Load Balancing:` The operating system may implement load balancing algorithms to distribute computational tasks evenly across the network, preventing individual machines from becoming overloaded.

`Heterogeneity:` Distributed systems may consist of machines with different hardware architectures and operating systems. The distributed OS must handle this heterogeneity to provide a seamless environment.

Distributed operating systems are commonly used in large-scale computing environments, such as cloud computing infrastructures, where resources are distributed across data centers. Examples of distributed operating systems include Google's Chrome OS, distributed versions of Linux, and Microsoft's Azure Sphere OS.

## Real Time Opearting System (RTOS)

A Real-Time Operating System (RTOS) is an operating system designed to meet the specific timing and reliability requirements of real-time systems. Real-time systems must respond to external stimuli within a specified time frame, making the predictability and timeliness of operations critical. Here are key features and characteristics of Real-Time Operating Systems:

`Deterministic Behavior:` RTOS is designed to provide deterministic behavior, meaning that the timing of operations is predictable and consistent. This is crucial for applications where timing is critical, such as in control systems, robotics, and embedded systems.

`Task Scheduling:` RTOS uses scheduling algorithms that prioritize tasks based on their urgency and deadlines. Tasks with higher priority or closer deadlines are given precedence in execution.

`Hard and Soft Real-Time Systems:` Real-time systems are often categorized as hard or soft real-time. In a hard real-time system, missing a deadline is considered a catastrophic failure. In a soft real-time system, missing a deadline is undesirable but not necessarily catastrophic.

`Interrupt Handling:` RTOS provides efficient and predictable interrupt handling mechanisms. Interrupts are events that can preempt the normal execution of a task to handle time-critical events.

`Low Latency:` RTOS aims to minimize the time between the occurrence of an event and the system's response to that event. Low latency is crucial for applications where timely responses are essential.

`Predictable Task Execution Time:` RTOS ensures that the execution time of tasks is predictable and consistent. This predictability is essential for tasks that require synchronization and coordination.

`Resource Management:` Efficient management of system resources, including CPU time, memory, and I/O, is a critical aspect of RTOS. Resource allocation is done with a focus on meeting timing requirements.

`Concurrency:` Real-time systems often involve concurrent execution of tasks. RTOS manages this concurrency to ensure that tasks with higher priority or closer deadlines are given precedence.

`Clocks and Timers:` RTOS includes accurate clocks and timers to track time and deadlines. Timers are used to trigger events and ensure that tasks are executed within their specified time frames.

`Safety-Critical Applications:` RTOS is commonly used in safety-critical applications such as medical devices, automotive control systems, and aerospace systems where reliable and timely operation is essential for safety.

Popular examples of Real-Time Operating Systems include FreeRTOS, VxWorks, QNX, and RTLinux. These systems are widely used in various industries where real-time performance is critical.
