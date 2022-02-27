# Buffer
-   buffers are two types,
    1. one is unbounded buffer 
    2. another is bounded buffer
-   unbounded buffer is that which has no practical limit in size, the consumer may have to wait for new item but the producer can produce new item.
-   again bounded buffer is a fixed size buffer, in this case the consumer must wait if the buffer is empty and the producer must wait if the buffer is full