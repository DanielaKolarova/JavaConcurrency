# JavaConcurrency
<b>Concurrency examples</b>

1. Object's wait(), notofy(), notifyAll()

  The Object class in java contains three final methods that allows threads to communicate about the lock status of a resource. 
  These methods are wait(), notify() and notifyAll().
  
  <ul>
  <li><b>wait</b>
    Object's wait methods has three variance, one which waits indefinitely for any other thread to call notify or notifyAll method
    on the object to wake up the current thread. Other two variances puts the current thread in wait for specific amount of time 
    before they wake up.</li>

  <li><b>notify</b>
    Notify method wakes up only one thread waiting on the object and that thread starts execution. So if there are multiple threads 
    waiting for an object, this method will wake up only one of them. The choice of the thread to wake depends on the OS implementation 
    of thread management.</li>

  <li><b>notifyAll</b>
    Wakes up all the threads waiting on the object, although which one will process first depends on the OS implementation.</li>
 </ul>   

These methods can be used to implement Producer-Consumer problem where consumer threads are waiting for the objects in Queue 
and producer threads put object in queue and notify the waiting threads.

In the example multiple threads work on the same object and wait, notify and notifyAll methods are used to demonstrated an example usage.
