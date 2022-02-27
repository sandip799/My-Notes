# Petersion's Solution
- This is a [[Software Based Solution]] to the [[Critical Section]] problem.
- this solution may not work correctly on modern computer architecture
- However, it provides a good algorithmic description of solving the critical section problem and illustrates some of the complexities involved in designing software that addresses the requirements of mutual exclusion, progress, and bounded waiting requirements
`as this is not working on modern day computer then why we should study this?`
- so answer is it provides a good algorithmic description of the solving the critical section problem and it would help us understand how to solve the critical section problem at software level if we are designing a software that needs to have the critical section problem

#### Explanation
- Petersion's solution is restricted to two processes that alternate execution between their critical section and reminder sections. Let's call the processes Pi & Pj
- Petersion's solution requires two data items to be shared between the processes
- one is turn and another one is flag array 

| int turn | boolean flag[2] | 
| -------- | --------------- |
- turn variable indicates which process turn is to use the critical section, if turn equals i that means process Pi turn to enter into critical section and if turn is j then process Pj is going to use its critical section
- here the flag is used to show the status of the process, if the flag[i] = true, that means Pi is ready or it wants to enter into the critical section and if false then outside of the critical section and likewise for process Pj  