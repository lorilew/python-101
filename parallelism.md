# Parallelism And Concurrency in Python
[Back](README.md)

## Types of Concurrency

### Threading
The operating systems knows about each thread and can interupt it at any time
and start running another thread. This is called _pre-emptive multitasking_.
The code doesn't control threads and a thread could be switched in the middle of a
python statement, like `x = x + 1`.

When using threads  data that is shared between threads needs to be protected or 
thread-safe. If something is not thread-safe there will need to be a copy of it 
in each thread. Another strategy for shared data is to use _thread local 
storage_. The module handling the thread local storage takes care separating 
accesses from different threads.

You can also specify the number of thread the prgram should run on. More threads
does not necessarily mean faster. If you go to high the extra overhead of creating
and destroying threads erases any time savings.

### Asyncio Tasks
Asyncio uses _cooperative multitasking_. The tasks must cooperate by announcing 
they are ready to be switched out. 

### Multiprocessing
Threading and asyncio both run on a single processor. If your computer has more 
than one CPU you can make use of them by using multiprocessing. Think of each 
process as running in it's own Python interpreter. And because they can be run on 
different core that can be run simultaneously.

## When Is Concurrency Useful?
* Waiting for reading/writing (I/O-Bound Process)
* Repeated computations (CPU-Bound Process)

Adding concurrency adds complexity. Is it always worth it?
* The program doesn't take long in the first place. 
* If your program doesn't need to run ran frequently and time isn't as issue.

## Common Problems
### Race Conditions
As you do not have control when thread are run these bugs can happen 
if shared data is not sufficiently protected. Treating objects as immutable 
helps combat against this issue.



These are condensed notes from Real Python. More information and example can 
be found (here)[https://realpython.com/python-concurrency/].
