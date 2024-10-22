# Lab 08 - Java Parallelism

## Deliverables

- [ ] Correctly implement a thread-safe unbounded blocking queue.
- [ ] Modify the hash map implementation to make it thread-safe.
- [ ] Describe to the TA why you needed to add synchronization at the specific locations in the hash map implementations.

## Instructions

Clone the repository from [https://github.com/CMU-17-214/f24-lab08](https://github.com/CMU-17-214/f24-lab08). Run `mvn install` to get started.

In the `src` directory you will find:

1. The `edu.cmu.cs.cs214.rec08.queue` package, which provides a `SimpleQueue` interface and an incomplete queue implementation.
1. The `edu.cmu.cs.cs214.rec08.map` package, which provides a `SimpleHashMap` class.
1. Various test files in a corresponding package in the `test` directory. These can be run with `mvn test`. Note that these are expected to fail at this point.

The queue implementation provided is "blocking". This means that its methods can pause (without computation) for an arbitrary amount of time. For example, a method that acquires a lock is likely a blocking method if other parts of the program hold the same lock.

Your task is to use primitive Java synchronization to implement a correct unbounded blocking queue from our incomplete implementation, and fix the race conditions in `SimpleHashMap`, which is currently not thread safe.

## Implementing a blocking queue

An _unbounded blocking queue_ is a normal queue except, if the queue is empty upon a dequeue request, then the request is blocked until an element is enqueued by another thread. This behavior is different from the standard `java.util` queue implementations, which either return `null` or throw a `NoSuchElementException` if the queue is empty. In an unbounded blocking queue, the dequeue method will always return a valid element from the queue, although the dequeueing thread might wait arbitrarily long to dequeue an element.

The `edu.cmu.cs.cs214.rec08.queue.UnboundedBlockingQueue` is not yet thread safe; if multiple threads access the same queue concurrently, race conditions can occur and you might obtain unexpected results.

To complete this part of the lab you should:

1. In the `src/test/main` folder, we have provided an `edu.cmu.cs.rec08.queue` test package that tests for the desired behavior of an unbounded blocking queue. Run the tests and understand their expected behavior. These tests will initially fail because the `UnboundedBlockingQueue` as given, is not thread safe and does not block when a thread attempts to dequeue from an empty queue.
1. Using basic Java synchronization and the `wait` and `notify` methods, eliminate race conditions in the `UnboundBlockingQueue` and make it a correct unbounded blocking queue. In other words, enqueueing an element should always succeed immediately. An attempt to dequeue from an empty queue, however, should block until an element has been enqueued by another thread. To simplify you implementation, prevent race conditions by allowing only one thread to enqueue or dequeue at a time. Use the provided JUnit tests to evaluate the correctness of your implementation. Look at the sample concurrency code from the lectures for more details.

## Implementing a thread safe concurrent hash map

In the `edu.cmu.cs.cs214.rec08.map` package we have provided a `SimpleHashMap` class that is currently not thread safe. Your task is to use primitive Java synchronization to make the implementation thread safe. When you have finished, show the TA your work and explain why synchronization was required where you used it.
