Transmission of data among *threads*.

After [[Thread Synchronization]] there are many ways that information can be transferred from one thread to the other.
- If the threads are in the same memory, then information can be transferred by value or address
- If the threads are not in the same memory (distributed), then transferring information by value is straightforward but by address is difficult.