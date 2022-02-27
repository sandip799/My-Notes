Back-Link [[Deadlock]]

# Resource
`What is resource ?`
- resource is like hardware or software. hardware means mouse , keyboard, hard disk, camera etc and it can be a software also like application, function or file also.


`is any process can directly access the resource ?`
- answer is no, because if a process can directly using the resource without any restriction then it can use the resource concurrently and no other process can use this resources further.

`who takes the dicission that this perticular resource is used by this process ?`
- operating system, process request to the os that please give that resource then os lookup all the process which are processing at the same time then take a decision that the resource should be given to the process or not.

`on a resource what process can do ?`
- **1- Request** - process request for a resource to the os 
- **2-Use** - when os allocates the resource to the process, then the process can use it.
- **3-Release** - when use is complited then process releases the resource