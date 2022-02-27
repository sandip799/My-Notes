# Progress
This is one of the requirement that processes have to fulfill to access the shared region of data.

- If no process is executing in its critical section and some process wish to enter their critical section, then only those processes that are not executing in their remainder sections can participate in the decision on which will enter its critical section next, and this section cannot be postponed indefinitely

##### Meaning
- at some point of time there are no processes executing in their critical section, and that point of time two or more processes wish to enter the critical sections, then here question is `which of the processes that wish to enter into the critical section should actually use their critical section first ?` because we know that one process can work at critical section at one time
- then this decision taken by those processes which are not executing in their reminder section, basically these processes participating in the decision making process
- again this selection cant be postponed indefinitely , this means decision who should enter the critical section should be taken without causing much delay.