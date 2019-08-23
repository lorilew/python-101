
# Parallelism And Concurrency in Python
[Back](README.md)

## Types of Concurrency

### Threading
The operating systems knows about each thread and can interrupt it at any time
and start running another thread. This is called _pre-emptive multitasking_.
The code doesn't control threads and a thread could be switched in the middle of a
python statement, like `x = x + 1`.

When using threads  data that is shared between threads needs to be protected or 
thread-safe. If something is not thread-safe there will need to be a copy of it 
in each thread. Another strategy for shared data is to use _thread local 
storage_. The module handling the thread local storage takes care separating 
accesses from different threads.

You can also specify the number of thread the program should run on. More threads
does not necessarily mean faster. If you go to high the extra overhead of creating
and destroying threads erases any time savings.

### Asyncio Tasks
Asyncio uses _cooperative multitasking_. The tasks must cooperate by announcing 
they are ready to be switched out. 

Asyncio uses a Python object called the _event loop_ to control how and when 
tasks are ran. All tasks run on one thread. Tasks set their state to show that 
they are waiting or ready to run. The event loop picks the task to run by 
the one that has been waiting the longest.

The _await_ key word in Python signal that the call is likely going to
take time and that the task should give up control. The _async_ key word
is a flag telling Python that a function uses _await_.

### Multiprocessing
Threading and Asyncio both run on a single processor. If your computer has more 
than one CPU you can make use of them by using multiprocessing. Think of each 
process as running in it's own Python interpreter. And because they can be run on 
different core that can be run simultaneously.

When setting up multiprocessing the module has to set up multiple python 
interpreters to be able to run code on multiple cores. This set up process needs
to be considered when choosing this option as it may actually increase the 
time your program runs.

Multiprocessing is very useful when dealing with CPU-Bound Processes as it takes 
advantage of the full CPU power in your computer.

## When Is Concurrency Useful?
* Waiting for reading/writing (I/O-Bound Process)
* Repeated computations (CPU-Bound Process)

Adding concurrency adds complexity. When is it not worth it?
* The program doesn't take long in the first place. 
* If your program doesn't need to run ran frequently and time isn't as issue.

## Common Problems
### Race Conditions
As you do not have control when thread are run these bugs can happen 
if shared data is not sufficiently protected. Treating objects as immutable 
helps combat against this issue.

### Starving Other Threads
Keep in mind when running tasks in a cooperative way, if a task takes a long time
to run because of a small bug, and there's no way to break the cycle it will starve
the other tasks that need to run.


These are condensed notes from Real Python. More information and example can 
be found (here)[https://realpython.com/python-concurrency/].
