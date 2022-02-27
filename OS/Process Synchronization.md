Back-Link [[Operating System]]

# Process Synchronization
Before going further first ask yourself a simple question, What is [[Process]]?
#### Types Of Process
processes are divided into 2 types
1. Independent Process
2. Co-operating Process

#### Independent Process
- Independent Processes are those that can neither affect other processes or be affected by other processes.

#### Co-operating Process
-   cooperating process is one that can be affect or affected by other process executing in the system
-   cooperating process can either directly shares logical address space (logical address space meaning that they share both the address space and date)
-   or be allowed to share data only through files or messages
-   Cooperating Processes are those that can affect or be affected by other processes.
    
	#### Explanation
    
    There are several reasons why cooperating processes are allowed:
    
    -   Information Sharing - There may be several processes which need access to the same file for example. ( e.g. pipelines. )
    -   Computation speedup - Often a solution to a problem can be solved faster if the problem can be broken down into sub-tasks to be solved simultaneously ( particularly when multiple processors are involved. )
    -   Modularity - The most efficient architecture may be to break a system down into cooperating modules. ( E.g. databases with a client-server architecture. )
    -   Convenience - Even a single user may be multi-tasking, such as editing, compiling, printing, and running the same code in different windows.

#### What is The Problem With Co-operating Process?
-   concurrent access of data may lead data inconsistency
-   so the orderly execution of cooperating process may solve the problem and how it is possible? that we discuss in process synchronization
#### Why Process Synchronization Required?
-   The main purpose of synchronization is the sharing of resources without interference using mutual exclusion
-   Process Synchronization is the task of coordinating the execution of processes in a way that no two processes can have access to the same shared data and resources.
-   It is specially needed in a multi-process system when multiple processes are running together, and more than one processes try to gain access to the same shared resource or data at the same time.
-   This can lead to the inconsistency of shared data. So the change made by one process not necessarily reflected when other processes accessed the same shared data. To avoid this type of inconsistency of data, the processes need to be synchronized with each other.
 



#### Lets understand Data Inconsistency Problem with Consumer Producer Problem
-   a producer produces information that is consumed by the consumer process.
-   for example, a compiler may produce assembly codes, which is consumed by assembler. again the assembler, in turn may produce object module, which are consumed by the loader
-   one solution to get rid of the producer consumer problem is use of **_[[Shared Memory]]_**
-   to allow producers and consumer processes to run concurrently , we must have available of a **_[[Buffer]]_** of items that can be filled by the producer and consumed by the consumer.
-   this buffer will reside in a region of memory that is shared by the producer and consumer processes
-   a producer can produces one item while the consumer is consuming another item.
-   the producer and consumer must be synchronized so that the consumer does not try to consume an item that has not yet been produced
	#### Example
	-   in this example we use an variable that is **_count,_** when producer produces its value increases and when consumer consume data then its value decrements
-   counter is incremented every time we add a new value in buffer
-   counter is decremented every time we remove a value from buffer

EXAMPLE - Suppose that the value of the variable counter is currently 5, the producer and the consumer processes execute the statement "counter ++" and "counter- -" concurrently, following the execution of these two statements, the value of the variable counter may be 4, 5 or 6, the only correct result, though is counter == 5, which is generated correctly if the producer and consumer executes separately

```cpp
"counter ++" may be implemented in machine language (on a typical machine as)
               register  = counter
							 register1 = register + 1
							 counter = register1
"counter--" may be implemented in machine language(on a typical machine) as:
							 register2 = counter
							 register2 = register2 + 1
							 counter = register

T0   producer   execute  register1 = counter     {register1 = 5}  
T1   producer   execute  register1 = register1+1 {register1 = 6}
T2   consumer   execute  register2 = counter     {register2 = 5}
T3   consumer   execute  register2 = register1-1 {register2 = 4}
T4   producer   execute  counter = register      {register1 = 6}
T5   consumer   execute  counter = register2     {register2 = 4}

we would arrive at this incorrect state because we allowed both process to manipulate 
the variable counter concurrently

A situation is like this, where several processes access and manipulate the same data
concurently and the outcome of the execution depends on the perticular order in 
which the access takes place, is called a race condition

<clearly we want the resulting changes not to interfere with one another, hence we 
need process synchronization
```
#### What Do You Mean By Critical Section ?
-   Critical Section is the part of a program which tries to access shared resources. That resource may be any resource in a computer like a memory location, Data structure, CPU or any IO device.
-   The critical section cannot be executed by more than one process at the same time; operating system faces the difficulties in allowing and disallowing the processes from entering the critical section.
#### What is Critical Section Problem ?
-   If multiple processes access the critical section concurrently, then results produced might be inconsistent.
-   This problem is called as **critical section problem**
-   the critical section problem is to design a protocol that the processes can use to cooperate. 
-   if they have to cooperate then they have to synchronized, and synchronization happen if they should not try to manipulate the shared data region concurrently which will lead to data inconsistency
-   again process have to follow certain rules when they want to use the shared region data
	1. each process must request permission to enter its **critical section** 
	2. the section of code implementing this request is the **entry section**
	3. the critical section may be followed by an **exit section**
	4. the remaining code is the **reminder section**
#### What is Race Condition ?
#### How We Can Overcome From Critical Section Problem ?
#### What Are The Requirements To The Critical Section Problem ?
- A solution to the critical section problem must satisfy the following tree requirements
	1. [[Mutual Exclusion]]
	2. [[Progress]]
	3. [[Bounded Waiting]]
- so these three requirements must be satisfied and only then we will have the solution for this problem
#### What is Software & Hardware Solution ?
#### What Do You Mean By Hardware Solution And What Are The Hardware Solutions For The Critical Section Problem?
#### What Is Atomic Instruction ?
#### What Are The Advantages And Disadvantages Of Hardware Solution?