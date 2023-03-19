# 3 Stack in Java

In Java, a stack is a data structure that follows the Last In First Out (LIFO) principle. It is a collection of elements that supports two main operations:

1. Push: adds an element to the top of the stack
2. Pop: removes the element from the top of the stack

Other common operations on a stack include:

1. Peek: returns the top element of the stack without removing it
2. isEmpty: checks if the stack is empty
3. Size: returns the number of elements in the stack

Java provides a built-in Stack class that implements the stack data structure. Here's an example of how to create and use a stack in Java:

```java
import java.util.Stack;

public class Example {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        stack.push(1);
        stack.push(2);
        stack.push(3);

        System.out.println("Stack: " + stack);
        // Output: Stack: [1, 2, 3]

        int top = stack.pop();
        System.out.println("Popped element: " + top);
        // Output: Popped element: 3

        int peek = stack.peek();
        System.out.println("Peeked element: " + peek);
        // Output: Peeked element: 2

        boolean empty = stack.isEmpty();
        System.out.println("Is stack empty? " + empty);
        // Output: Is stack empty? false

        int size = stack.size();
        System.out.println("Size of stack: " + size);
        // Output: Size of stack: 2
    }
}
```

In this example, we create a stack of integers using the Stack class. We then push three elements onto the stack, and print out the contents of the stack using the toString() method. We then pop the top element off the stack, peek at the new top element, check if the stack is empty, and get the size of the stack using the respective methods of the Stack class.