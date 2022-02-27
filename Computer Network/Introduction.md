#protocols #layerArchitecutre
Date:- 27 - OCT - 2021
# Layer Architecture & Protocol
## Protocols
- A Network **Protocols** is an established set of rules that determines how the date is transmitted between different devices in the same network.
- Essentially it allows connected devices to communicate with each other, regardless of any differences in their processes, structure or design
### Example
![[protocols.png]]
- In Date Link layer one function is there called framing in which some set of bits added at the start and end of the original data stream, suppose user A sending the data to user B where user a use the frame bit 01111 where user b uses frame bit 0111, `is user B will get the actual data ?` No, so to communicate over the network we have to obey some set of rules and that is protocol  
![[ip.png]]
- Again here as user A uses IPv4 & B uses IPv6 so they cant interact with each other correctly, so that you have to obey some set of rules
### How to implement the Protocol
![[packets.png]]
- Suppose you ordered a product from flipkart or amazon, `is that automatically reach to your door step?` No, there are some carriers, that help to reach the product to your door step similarly when you sending data to another client there are something in between which helps to move the data nearer to the client like address, machines used in networks etc
- **Processing Capability**- Suppose 3 devices are connected to one node and that node has no processing capability , and you are sending data to one of the client that is connected to that node then how can the data reaches to the particular client? so basically here the node sends the same data into all the clients that are connected to that node and the data accepted by the actual client after recognizing the address by the client, but if the node has the processing capability then it only sends the data to the destination client without sending to all the clients
![[logic.png]]
- Again the supporting bits which are added to the actual data has some logic
- randomly bits are not added to the actual data, it has some logic so that when it reaches at the destination then it can be decoded successfully by using that particular logic
# Layer Architecture
## Overview Of All The Layers
![[LayerArchitecture.png]]
### Data Link Layer
- **Definition**= It is responsible for hop to hop or sometimes you can say link to link communication. Here question arises that `Why we are saying hop to hop communication ?`
![[dllayer.png]]
- Suppose we are trying to send data from source to destination, then the data will transfer through link or medium or channel and all the protocols are applied on this given link 
#### Example
- Let suppose there are 2 routers are in between source and destination, and you are checking the error that are generated when the data is transferred through the link.
- so this error checking process will be start when the data reaches from S to R1, again start when the data reaches R1 to R2 and so on until the data reaches at the destination node
- so when the data is passes through a link it has to pass all the protocols that is applied over the link
### Addressing Mode
- To send the data from source to destination how many addressing modes are required?
1. **MAC Address**(***DLL***)-**48Bits**
2. **IP Address**(***NL***)-**32Bits**
3. **Port Address**(***TL***)-**16Bits**
4. **Specific Address**(***AL***)- Not Defined **Sentential Form(ex- www.google.com)** (because user directly interact with user in the application layer)
`Why we are using different types of addressing modes?` 
![[igitnetwork.png]]
[[000 Course Content Of C Programming]]



