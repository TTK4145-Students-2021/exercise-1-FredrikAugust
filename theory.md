Exercise 1 - Theory questions
-----------------------------
 
### What is the difference between concurrency and parallelism?
> In a concurrent system the computer is working simultaneously on several tasks, but they are not run in parallel. That is the progress of the two (or more) tasks are intertwined, but strictly speaking only one is making progress _at the time_.
 
### Why have machines become increasingly multicore in the past decade?
> Because it allows for a greater degree of parallelism with multiple CPU cores which in turn (can) increase the performance of your program.
 
### Why do we divide software (programs) into concurrently executing parts (like threads or processes)? (Or phrased differently: What problems do concurrency help in solving?)
> In problems that can be divided into subproblems, we can calculate several subproblems at the same time before merging them into a larger problem. Thus making progress on several parts of the overall problem at the same time.
 
### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both? (Come back to this after you have worked on part 4 of this exercise)
> From a developer standpoint, working with concurrency is harder than working in a strictly synchronous code. This is because you have to deal with synchronisation of the different threads if you wish to dodge the indeterministic behaviour such as the results presented in part 4.
 
### What is the conceptual difference between threads and processes?
> Threads are spawned by processes, and share memory. For example, when we want to spawn a new handler in our web server we want to spawn a new thread. Processes, on the other hand, are more complex and have their own memory. For example our web server might run as a process.
 
### Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they?
> Green threads are managed by a virtual machine instead of the operating system. For example erlangs processes. They are often more lightweight and closely integrated with the language.
 
### What is the Go-language's "goroutine"? A C/POSIX "pthread"?
> Go's coroutine are actually not necessarily put on their own OS thread unless necessary. POSIX's `pthreads`, however, is a standardised structure for OS-level threads.
 
### In Go, what does `func GOMAXPROCS(n int) int` change? 
> This limits how many (OS-level) threads the process can spawn. This is due to the green threads Go uses, so you control how many "real" threads we can allocate to those.

