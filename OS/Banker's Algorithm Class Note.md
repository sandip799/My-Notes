# Banker's Algorithm Class Note
- i learn that this is used to check is the system is in safe state or not
- its name derived form the term bank
- in bank suppose if a customer is needed any loan then it request to bank, then bank checks , if the total amount is greater than sum of all the customers total amount then it will be in safe state and it will sanction loan to that particular customer
- but if not, and the bank sanctioned loan to that person, then if other customer wants to withdraw amount from its account then might be possible bank will not be able to give that, so at that stage bank will be in unsafe mode
- so basically this is an algorithm which checks that is the system is in safe state or not
- before going to the algorithm first we solve few problems so that there will be a clear vision about this 

#### Lets solve a question to understand whole concept
| Process | Allocation | Max | Available | Need = Max-Allocation |
| ------- | ---------- | --- | --------- | --------------------- |
| P1      | 1          | 3   |           | 2                     |
| P2      | 5          | 8   |           | 2                     |
| P3      | 3          | 4   |           | 1                     |
| P4      | 2          | 7   |           | 5                     | 

so in this example you think that every process need same instance of resources
again given that system has total 12 resources. 
how many resource available in the system = total resource - total allocation
12-11 = 1
then you have to check that is there any process which needs less of equal to the remaining resource ?
so in this case p3 require only one resource, so allocate resource to that process
then after complete execution of the process p3 available resource amount will increase to 4
then again check that is there any process needed resource is less than or equal to 4
so in this case there are p1 and p2 process which needed less resources than available
so you can assign resource to any of them, let assign sequentially, assign resources to p1
then after complete execution of p1 available resources increases to 7
then assign p2, after complete execution available resource size increase to 9
then assign p4, and all processes complete its execution

here all the processes execute so the system is in  safe state 
here the sequence of process execution is <p3, p1, p2, p4 >

#### Lets solve another question little bit complex that previous

| Process | Allocation | Max       | Available |
| ------- | ---------- | --------- | --------- |
|         | A   B    C | A   B   C | A   B   C |
| P1      | 0   1    0 | 7   5   3 | 3   3   2 |
| P2      | 2   0    0 | 3   2   2 | 5   3   2 |
| P3      | 3   0    2 | 9   0   2 | 7   4   3 |
| P4      | 2   1    1 | 2   2   2 | 7   5   3 |
| P5      | 0   0    2 | 4   3   3 | 10  5   5 | 

- here all the information about the process like allocation resource data or max resource data is stored in memory using matrix
- here we only assign resource to that process when all type of remaining resources is less than equal to the available resources
- first we have to calculate the number of required processes for every process
| Process | A   | B   | C   |
| ------- | --- | --- | --- |
| P1      | 7   | 4   | 3   |
| P2      | 1   | 2   | 2   |
| P3      | 6   | 0   | 0   |
| P4      | 0   | 1   | 1   | 
| P5      | 4   | 3   | 1   |
- lets assign sequentially, first assign resources to p2, then after execution available resources becomes 5  3  2
- then execute p4, after execution available resource becomes 7  4  3
- then execute p1, after execution available resource becomes 7  5  3
- then execute p3, after execution available resource becomes 10 5  5
- then execute p5, after execution available resource becomes 10  5  7
- in this example safe sequence becomes <p2, p4, p1, p3, p5>

**_NOTE_**- after solving resources allocation problem, if addition of initial available resources and total assigned resource of all process is equal to final remaining resource then your solution is correct

- when we have n number of process and m number of resources then
	1. Allocation :- Matrix of n * m
	2. Max :- Matrix of size n * m
	3. Need :- Matrix of size n * m
	4. Available :- Array of size m
	5. Finish :- Array of size n

**Note-** OS will not change the Available actually, it only checks that if in this sequence process will execute like  <p2, p4, p1, p3, p5> then is the system will stay in safe state or not, so there is actual allocation of resources done by os using this algorithm, it just checks that if i execute p2 first then these amount of resource will available or if i execute p4 then this amount of resource will remain and so on and all these are **Imaginary** and this all are done by using variables or matrices and updates all these when process get executed

## Algorithm
1. Let Work and Finish be vectors of length 'm' and 'n' respectively.
	initialize Work = Available
	Finish[i] = false; for j= 1,2,3,4....n
2. FInd an i such that both
	(a) FInish[i] = false
	(b) Need i <= Work
	if no such i exists goto step (4)
3. Work = Work + Allocation[i]
	Finish [i] = true
	goto step (2)
4. if Finish[i] = true for all I
	then the system is in a safe state
	#### Work Of This Algorithm
	- Finish array store all the process and initially all the value of that array are false means no any process has complete its execution
	- Then we have to find out the process that is not executed yet and Need of that process is less than or equal to Work
	- If process available then after completion of that process we will update the Work by adding the allocation of that process, then change its state from false to true and then again goto step 2 and try to find another process
	-  If process available then well but if no process available then we goto step 4
	-  when the time comes when no other processes will not fulfilling the step 2 then might possible that all processes executed properly or complete their execution or might possible that whatever processes are available we cannot fulfill their requirement
	-  in the step 4 we check that all the processes are executed completely or not, if yes then system is in safe state otherwise system is in unsafe state