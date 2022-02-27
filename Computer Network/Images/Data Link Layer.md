#framing #bitStuffing #dataLinkLayer
# Framing & Bit Stuffing
![[DLL1.png]]
- In Data Link Layer small small **Frames** are created and then transfer to the Physical Layer,  then it converted into stream of bits and then there will be a devices which convert the stream of bits to signal and then it put over the link or the medium then it reaches at the destination, there will be a device which convert the signal to stream of bits and then it goes upward to the Data Link Layer in receiver side, then here the stream of bits are converted into the frames but here the question is `How to recognise that which set of bits are belongs to which frame?` so the answer is in the sender side the sender has to put some logic in the frame so that by help of that logic the receiver can identify which bits are belongs to which frame and this process is called as **Framing Protocol**
![[DLL2.png]]
- So the logic is we have to add some extra bit so that the receiver can easily extract the actual frames from the stream of bits
- In the upper diagram you can see that the flag bit is **01111** and the actual data in a single frame is **10010111101001** and the flag bit added at the both end of the frame. When the bits are received by the receiver then it will first check the flag and when another flag will come then it will repack and create a frame and so on, but if the flag bit will not come further that means the data is error prone.
- But here a problem arises, and that problem is suppose the flag bit appears in the actual data then at the receiver end when the stream of bits are converted to the frames, wrong set of bits are repacked as a frame so that the receiver can't get the actual data which is send from the sender
- So here question arises `how can we overcome from this problem?` we have two options,either we can add extra bit in the actual data or we can delete few bits from the actual data but deleting bits will effect in loss of the actual data so we have only one option left that is to adding some extra bit
- so we have to stuff some extra bit inside the actual data so that the flag never repeat in the actual data bits, and this method is called as **Bit Stuffing**, Stuff means we have to add something in it and as we introducing extra bit in the data that's why it is named as Bit Stuffing
- Again the extra bit will remove by the receiver so that receiver will get the actual data
![[DLL3.png]]
- if flag bit is '0' followed by n 1's then stuff '0' just after (n - 1) 1's
![[DLL4.png]]
- If you look carefully in upper example the actual data is **101101** and the flag is **0111** and as you can see the flag bit is not repeating in the actual data so we don't have to introduce extra bit but in the receiver side if it will remove 0 from the actual data because the program instruction is written like that, that's why we have to include extra bit 
![[DLL5.png]]
#flowControlProtocol
# Flow Control Protocol
- Flow control protocol is the design issue at Data Link Layer
- And remember that this protocol will be executed in every link, that why we are saying that the data link layer is responsible for link to link or hop to hop communication and the biggest reason is at every link the mac address is changing. `why mac address is changing ?` because each devices have their own unique mac address
- `Why we are saying flow control, what is the significance of it ?`
![[DLL6.png]]
## Parameter Associated With Flow Control Protocol
### Transmission Time
- the actual meaning of flow control is whenever a sender is sending something we have to create some synchronization so that the receiver will get the actual data
- Suppose Sender A sending 10 packets to the destination B, and two routers are connected in between A and B, then `how the data will flow over the network?`, so first all the packets are send from the source host to the router, and remember that router R1 recreate all the frames after receiving the frame from sender and again transfer the recreated frame to the router R2, then here question arises `why it recreate all the frames instead of just passing the same frame without any modification?`because each packet has two mac address that is source and destination address and each router has unique mac address so when the packets are received by the router then the destination mac address will be changed in all the packets because at that time the router is the sender and the next node is the receiver