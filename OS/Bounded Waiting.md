# Bounded Waiting
There exist a bound or limit, on the number of times that other processes are allowed to enter their critical section after a process has made a request to enter its critical section and before that request is granted

#### Means
- let say that one process requested to enter into their critical section, and the request may not granted, some other process which already made a request is now granted to use their critical section
- in this kind of scenario there will be a limit on the number of times other processes are allowed to enter into their critical section
- so `why should we have this ?` we have this because if we have not this kind of thing then we should face problem like _[[Starvation]]_ in the critical section, that's why we are having this bounded waiting
- so we will have a bound or limit on the number of times that other processes are allowed to enter their critical section if one process already requested to enter into their critical section but the request yet not been granted