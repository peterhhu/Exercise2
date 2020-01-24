# Mutex and Channel basics

### What is an atomic operation?
> In concurrent programming an atomic operation is a program operation that runs utterly independently of any other processes.

### What is a semaphore?
> A semaphore is a variable or abstract data type used to control access to a common resource by multiple processes in a concurrent system.

### What is a mutex?
> A mutex is a mutually exclusive flag. It lets only one thread gain access at a time, blocking the others. This ensures that only a single thread runs at a time. It acts like a locking mechanism used to synchronize acces to a resource.

### What is the difference between a mutex and a binary semaphore?
> A mutex is a locking mechanism whilst a binary semaphore is a signalling mechanism. This means that a mutex may only be called/signalled by the thread that holds it, while a using semaphores a thread can be signalled by another thread. A binary semaphore might be seen as a generalized mutex, and a mutex can therefore never be used as a binary semaphore, but a binary semaphore might be used as a mutex.

### What is a critical section?
> A critical section is a part of the code which accesses shared variables and has to be executed as an atomic operation. If there exists a group of cooperating processes, then at a given point of timen only one of the process can execute its critical section. Or else unpredictable behaviour occurs.

### What is the difference between race conditions and data races?
 > A race condition is a situation where the result of an operation depends on the order of occurence of certain individual operations. A data race is a situation where at least two threads access a shared variable at the same time.

### List some advantages of using message passing over lock-based synchronization primitives.
> Programs using message passing are highly portable.
It provides the programmer with explicit control over the location of memory in a parallell program, the memory used by each process. No need to worry about data races and deadlocks, which is vital to handle correctly when using locks.

### List some advantages of using lock-based synchronization primitives over message passing.
> Lock-based synchronization primitives doesn't bound the programmer's way of programming as much as message passing,
opening the possibility for a more efficient code.
