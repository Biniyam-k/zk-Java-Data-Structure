# 4 Queue in Java

n Java, a queue is a data structure that follows the First In First Out (FIFO) principle. It is a collection of elements that supports two main operations:

1. `Enqueue`: adds an element to the back of the queue
2. `Dequeue`: removes the element from the front of the queue

Other common operations on a queue include:

1. `Peek`: returns the front element of the queue without removing it
2. `isEmpty`: checks if the queue is empty
3. `Size`: returns the number of elements in the queue

Java provides a built-in Queue interface that defines these operations, as well as several implementations of the Queue interface. Here's an example of how to create and use a queue in Java:

```java
import java.util.LinkedList;
import java.util.Queue;

public class Example {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<>();

        queue.add("Alice");
        queue.add("Bob");
        queue.add("Charlie");

        System.out.println("Queue: " + queue);
        // Output: Queue: [Alice, Bob, Charlie]

        String front = queue.remove();
        System.out.println("Removed element: " + front);
        // Output: Removed element: Alice

        String peek = queue.peek();
        System.out.println("Peeked element: " + peek);
        // Output: Peeked element: Bob

        boolean empty = queue.isEmpty();
        System.out.println("Is queue empty? " + empty);
        // Output: Is queue empty? false

        int size = queue.size();
        System.out.println("Size of queue: " + size);
        // Output: Size of queue: 2
    }
}
```

In this example, we create a queue of strings using the LinkedList class, which implements the Queue interface. We then enqueue three elements onto the queue, and print out the contents of the queue using the `toString()` method. We then dequeue the front element from the queue, peek at the new front element, check if the queue is empty, and get the size of the queue using the respective methods of the Queue interface.