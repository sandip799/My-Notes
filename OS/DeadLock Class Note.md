Back-Link [[Deadlock]]
#deadlock

# Deadlock
- As the name itself showing that something is dead, that  cant go further , or cant proceed further means something is dead and that kind of lock means the process cant go ahead.
- **Definition**- if two or more process are waiting for such an event which is never going to occur then this is called as deadlock, means both the processes are in infinite wait.
 ### Real Life Example
- **Example-** Indian traffic jam
- **Example-** another example is that, suppose you and your friend working in a company together , one day your friend tell you that why don't you work hard, you have the great talent, then you said that the manager is not giving him much money , that's why , then your friend ask the manager why you don't pay him more, he is very talented, then the manager said that he doesn't work hard that's why....this type situation is deadlock

#deadlockDetection
## If There is Deadlock in the system Then How we can assure that deadlock is there?     
To satisfy deadlock there are 4 necessary condition to achieve
- Mutual Exclusion
- Hold & Wait
- No Preemption
- Circular Wait

`Is all these four conditions should be satisfied?`
- Yes 


`Always ?` 
- Yes always and all four..
- if you want deadlock should occur then these four condition should be satisfied
- if any of these missing then there is no deadlock

#### Explanation Of All These Conditions
- Hold and wait means every process should hold one resource and should waiting for one resource...
- Suppose there is a process that only waiting waiting.... and there can be a process that is only holding holding,.... then this type of situation is not a deadlock situation..
- For deadlock both hold and wait are compulsory for both process.
- No any force full preemption of resource, means suppose there is a process which is holding resource then if the os will preempt that resource form the process then there will be no deadlock...
- Again here question arises `process can be preempted?` so here we don't talk about **[[Process Preemption]]**, here we talk about **[[Resource Preemption]]**, that if a process holding a resource and no matter how many preemption happened it wont leave the resource then that situation will occurs deadlock.

  | Process | Holds     | Wait      |
  | ------- | --------- | --------- |
  | P1      | Keyboard  | Hard Disk |
  | P2      | Hard Disk | Printer   |
  | P3      | Printer   | Keyboard          |   

- Here in the above example if the p1 ends its execution it releases the resource and other process will execute but here every process are connected in a circular manner any no one give their resource so this is a deadlock condition...
- in this example suppose hardware is used by two process parallelly then there is no mutual exclusion so this will not be a deadlock situation.
- again suppose p2 is waiting for the harddisk and not waiting for the printer then p2 will end its execution at some point of time then p1 will execute and after that p3 will execute....so here circular waiting condition not satisfied so this is not a dead lock condition.
- again suppose p1 needs the harddisk and it forcefully preempt resource the harddisk from p2 then there will be no deadlock....so no forceful resource preemption.. 

#### Resource Allocation Graph
- remember that if there is a graph then there should be two things  
	1. Process
	2. Resource 
- again there are two types of vertex ,
	1. one is for process 
	2. another one is for resource.
- if process you have to show in the graph then show it using a circle and for resource using rectangle..
- again resource is of two types
	1. one is having single instance
	2.  another one is multiple instances.
	- single instance represented by using rectangle with one dot and multiple instance having multiple dots inside the rectangle
- but there might be possible that, there will be instance of the resource, then here question arises what is instance of resources ? suppose there are 2 same type of printers connected with a computer system ...so here we dont call that two different printers but we call that two instances of the same resource..
- again there are two types of edges , one is request and another one is allocation
		request- from process to resource
		allocation - from instance to process
		
#### Recovery From Deadlock
 1. Make sure that deadlock never occure means prevent the system from deadlock or avoid deadlock
 2. allow deadlock, detect and recover
 3. pretend that there is no any deadlock

 lets understand all three with an example...
- when you already noticed that you will be suffer in fever in near future and you take prevent, this is type 1
- now you suffering from fever and you take the madicine or something and then you recover from fever...this is of second type
-  now you are suffering from fever but you ignore that and you said that i am as perfect as old whine.
		
	
#### Deadlock Prevention
- we already discussed that if all the four conditions will satisfy then deadlock will occur but if one condition then deadlock will never occur
- so make an os and make such arrangement that one of these will never occure.
lets again understand this with an example
   #### Real Life Example
   - suppose there will be a function in your college. to attend that function you have to satisfy four conditions
	   1.  one is you have a invitation card
	   2.  then you have to wear a specific dress to join that party
	   3.  you have to wear a specific shoe
	   4.  you have to reach at a specific time
	- if you don't obey at least one of these condition then you can't attend the function
	- suppose your friend is a notorious person and he does not get any invitation for that function so he tried hard to stop you from attending that function
	- here your friend is the os and you are the process and all the conditions are the deadlock condition

 `So how can we prevent deadlock?`       #deadlockPrevention
 1. **Prevent Mutual Exclusion :-**
	- have enough resources to provide simultaneous execution..
	- this is possible if we have multiple instances of resources and practically this is impossible..
	- making all process independent but if we make independent process then it requires many instances of resources for individual process which is practically impossible 
2. **Preventing Hold & Lock :-**
   - a process can either hold or wait but not together
   - if all resources are available then acquire or else just wait for all.
		 #### Example
	   lets understand this with an example
	   1. suppose a process needed resources like hard disk, keyboard and printer...if suppose all the resources available except printer then the process will not hold any of the resources and wait till all the resources available for that, if this is the case then starvation may occur because may be a process not get resource for indefinite time
	   2.  if process is trying to acquire a resource which is not available while holding some resources, then release the allocated resources
		   - suppose same process needed keyboard and hard disk initially, and if at that time these resources are free then it acquire those resources and when that process needed printer and if at that time printer is not available then it should release all the previously hold resources and wait because to prevent deadlock the process will be either waiting or holding resources, not together...
		   - but here, the problem is if a process holds resources but not using them then there will be the poor utilization of the resources...
		   - suppose same process holding all the resources that it needed and suppose at the time of processing it only need keyboard and not using other resources but holding all of them then there is a poor resource utilization occur.
3. **Preventing No Preemption:-**
 	- suppose p1 is needed the resources r1 and p2 is holding r1 and that process is waiting for other resources then at that time may be os will preempt the resources from p2 and assign it to p1 and if this happen then we can prevent deadlock..
 	- but here the problem is all of the resources can't preempted.
 	- let suppose p2 holding hard disk and the same resource p1 needed, then possible that the process will not preempt, basically this depends upon os, if os find out that the resources is not used right now by the process p2 then it preempt that...
4. **Preventing The Circular Wait:-**
 	1. all the resources have been given a unique sequence number like r1,r2,r3 etc
	2. any process while holding a resource ri ,can request for rj only when j > i
	3. if a process is holding a resource ri, and wants another resources rj, when j < i, then process will have to release ri and will have to acquire rj first.
		by using this we can stop having the circular wait.
		
# Recovery From Deadlock
- In deadlock avoidance, the OS tries to keep system in *[[Safe State]]*
- when system is in safe state then there is no possibilities of having deadlock
- but if the system is in unsafe state then there will be possibility that deadlock can occur
`Suppose there is no deadlock, can we say that the system is not in unsafe state ?`
- no we can't say that
- it is possible that, there is no deadlock occur even if the system is in unsafe state
## Deadlock Avoidance
- in deadlock avoidance, the request for any resource will be granted if the resulting state of the system doesn't cause deadlock in system.
     #### Example
	- Suppose India vs Pakistan T-20 match is going to happen in your city, suppose all the tickets are sold and a person is selling tickets in black.
	- a friend of that person already reserved two tickets 
	- when you are going to buy tickets from that person then first he will check that how many tickets are left, if the number of tickets are more than two then that person will give you otherwise not
	- similarly, process ask os for resource allocation, then os analyze that if i give the resource to that process then the system will stay in safe state or not, if not then it doesn't allocate any resource to that process
`But here question arises how to implement this ?`
so we use [[Banker's Algorithm]] to implement this
   