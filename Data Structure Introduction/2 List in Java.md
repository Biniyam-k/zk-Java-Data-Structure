# 2 List in Java

In Java, `List` is an interface in the `java.util` package that defines the behavior of a collection that stores elements in a specific order. A `List` allows you to add, remove, and access elements using an index. It also allows duplicate elements and preserves their order.

The `List` interface provides several methods that allow you to manipulate the elements of the list. Some of the commonly used methods are:

- `add(E e)`: adds an element to the end of the list.
- `add(int index, E element)`: inserts an element at the specified index in the list.
- `remove(int index)`: removes the element at the specified index from the list.
- `get(int index)`: returns the element at the specified index in the list.
- `size()`: returns the number of elements in the list.
- `indexOf(Object o)`: returns the index of the first occurrence of the specified element in the list.
- `contains(Object o)`: returns `true` if the list contains the specified element.

The `List` interface is implemented by several classes in the Java Collections Framework, including:

- `ArrayList`: an implementation of `List` that stores elements in an array-like structure.
- `LinkedList`: an implementation of `List` that stores elements in a linked list structure.
- `Vector`: an implementation of `List` that is similar to `ArrayList`, but is synchronized (thread-safe).
- `Stack`: a subclass of `Vector` that implements a stack data structure.

The two most commonly used list implementations in Java are `ArrayList` and `LinkedList`.

### `ArrayList`

 is an implementation of the `List` interface that stores elements in an array-like structure. Here are some features of `ArrayList`:

1. Dynamic Size: Unlike arrays, `ArrayList` can grow or shrink dynamically as you add or remove elements.
2. Fast Random Access: `ArrayList` provides fast random access to elements, as you can access any element in the list using an index.
3. Auto-Resizing: `ArrayList` automatically resizes itself when you add or remove elements, making it easy to work with.
4. Type Safety: `ArrayList` is type-safe, meaning you can only store elements of a specific data type in the list. This helps prevent type-related errors at runtime.

Here is an example of how to create and use an `ArrayList` in Java:

```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // create an ArrayList of integers
        ArrayList<Integer> numbers = new ArrayList<Integer>();

        // add elements to the ArrayList
        numbers.add(1);
        numbers.add(2);
        numbers.add(3);

        // access elements of the ArrayList
        System.out.println(numbers.get(0)); // prints 1
        System.out.println(numbers.get(1)); // prints 2
        System.out.println(numbers.get(2)); // prints 3

        // remove an element from the ArrayList
        numbers.remove(1);

        // iterate over the elements of the ArrayList
        for (int i = 0; i < numbers.size(); i++) {
            System.out.println(numbers.get(i));
        }
    }
}
```

### `LinkedList`

is another implementation of the `List` interface that stores elements in a linked list structure. Here are some features of `LinkedList`:

1. Dynamic Size: Like `ArrayList`, `LinkedList` can grow or shrink dynamically as you add or remove elements.
2. Fast Sequential Access: `LinkedList` provides fast sequential access to elements, as you can easily traverse the list from beginning to end.
3. Fast Insertion and Deletion: `LinkedList` provides fast insertion and deletion of elements, especially when working with large lists.
4. Memory Overhead: `LinkedList` has a higher memory overhead than `ArrayList`, as each element is stored as a separate object with a reference to the next element in the list.

Here is an example of how to create and use a `LinkedList` in Java:

```java
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        // create a LinkedList of strings
				//<> genric paramter
        LinkedList<String> names = new LinkedList<String>();

        // add elements to the LinkedList
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        // access elements of the LinkedList
        System.out.println(names.get(0)); // prints Alice
        System.out.println(names.get(1)); // prints Bob
        System.out.println(names.get(2)); // prints Charlie

        // remove an element from the LinkedList
        names.remove(1);

        // iterate over the elements of the LinkedList
        for (String name : names) {
            System.out.println(name);
        }
    }
}
```

![Untitled](2%20List%20in%20Java%202ecb05b398e64aa5b9755233e491bec9/Untitled.png)
