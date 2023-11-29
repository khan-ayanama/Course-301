# Lecture:04

## Components of OS

1. `User space:` App are running
2. `Kernel:` Access to hardware

## Userspace

* No Hardware access
* Convient environment User apps.
* Interacts with Kernel

## Kernel

* Heart of OS
* Directly interacts with Hardware.

## Functions of Kernel

* `Process Management`
  * Process creation
  * Process termination
  * Process & thread schedule
  * Process synchronization
  * Process communication
* `Memory Management:`
  * Memory Allocation, deallocation
  * Free space Management
* `File Management:`
  * Create/Delete File
  * Directory Management
* `IO Management:`
  * Management and controlling of all I/O Devices
  * Spooling
  * Buffering
  * Caching

## Types of Kernel

### 1. Monolithic Kernel

* Fast Communication
* Kernel Bulky
* Less reliable
* eg:- `linux, unix, MSDos`

`Read More About it`

* Software Interrupts
* User Mode
* Kernel Mode

### 2. Micro Kernel

* Less Bulky
* More Reliable
* Stable
* Impacts on Performance
* Overhead between user mode and kernel mode
* eg: L4 Linux, Symbian OS

    ````How User mode and Kernel mode interacts?
    Ans: IPC (Interprocess Communication)
    * Shared Memory
    * Message Passing````

### 3. Hybrid Kernel

Userspace: File Management
KernelSpace: Process, memory, I/O
eg: MacOS, WindowsNT(7+)

## Nano Kernel

## Exo Kernel
