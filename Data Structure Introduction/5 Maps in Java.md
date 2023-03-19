# 5 Maps in Java

In Java, the Map interface provides a way to store and manipulate key-value pairs. A map is a collection of key-value pairs, where each key is unique and is used to access its corresponding value. The Map interface is part of the Java Collections Framework and is located in the java.util package.

The Map interface defines the following methods:

1. `void clear()`: Removes all the mappings from the map.
2. `boolean containsKey(Object key)`: Returns true if the map contains a mapping for the specified key.
3. `boolean containsValue(Object value)`: Returns true if the map contains at least one mapping with the specified value.
4. `Set<Map.Entry<K,V>> entrySet()`: Returns a set view of the mappings contained in this map.
5. `V get(Object key)`: Returns the value to which the specified key is mapped, or null if this map contains no mapping for the key.
6. `boolean isEmpty()`: Returns true if the map contains no key-value mappings.
7. `Set<K> keySet()`: Returns a set view of the keys contained in this map.
8. `V put(K key, V value)`: Associates the specified value with the specified key in this map.
9. `void putAll(Map<? extends K,? extends V> m)`: Copies all of the mappings from the specified map to this map.
10. `V remove(Object key)`: Removes the mapping for a key from this map if it is present.
11. `int size()`: Returns the number of key-value mappings in this map.
12. `Collection<V> values()`: Returns a collection view of the values contained in this map.

There are several classes that implement the Map interface in Java, including HashMap, TreeMap, LinkedHashMap, and ConcurrentHashMap. Each implementation has its own unique characteristics and performance characteristics, so it's important to choose the appropriate implementation for your use case.

### `HashMap`

 is an implementation of the Map interface and provides a way to store and manipulate key-value pairs. It uses a hash table to store the keys and values, allowing for quick access and retrieval of values based on their corresponding keys. HashMap is part of the Java Collections Framework and is located in the java.util package.

To use a HashMap, you must first create an instance of the class, specifying the types of the keys and values that it will store. For example, to create a HashMap that stores String keys and Integer values, you would write:

```java
HashMap<String, Integer> map = new HashMap<>();
```

Once you have created a HashMap, you can add key-value pairs to it using the `put()`
 method:

```java
map.put("one", 1);
map.put("two", 2);
map.put("three", 3);
```

You can retrieve a value from the map by specifying its corresponding key using the `get()`
 method:

```java
Integer value = map.get("two");
```

You can also check if a key exists in the map using the `containsKey()`
 method:

```jsx
if (map.containsKey("four")) {
    // do something
}
```

HashMap also provides methods for removing entries from the map, checking if the map is empty, and getting the size of the map. It's important to note that HashMap does not guarantee the order of its entries.

One potential issue with HashMap is that if too many keys hash to the same index in the hash table, the performance of the HashMap can degrade. To mitigate this issue, Java also provides other Map implementations like LinkedHashMap and TreeMap that can be used in situations where order or sorting is important.

### `Hashtable`

 is another implementation of the Map interface that provides a way to store and manipulate key-value pairs. It is similar to HashMap, but is synchronized, meaning that it can be safely used by multiple threads simultaneously. `Hashtable` is also part of the Java Collections Framework and is located in the `java.util` package.

To use a `Hashtable`, you must first create an instance of the class, specifying the types of the keys and values that it will store. For example, to create a `Hashtable` that stores String keys and Integer values, you would write:

```java
Hashtable<String, Integer> table = new Hashtable<>();
```

Once you have created a Hashtable, you can add key-value pairs to it using the `put()`
 method:

```java
table.put("one", 1);
table.put("two", 2);
table.put("three", 3);
```

You can retrieve a value from the table by specifying its corresponding key using the `get()`
 method:

```java
Integer value = table.get("two");
```

You can also check if a key exists in the table using the `containsKey()`
 method:

```java
if (table.containsKey("four")) {
    // do something
}
```

`Hashtable` also provides methods for removing entries from the table, checking if the table is empty, and getting the size of the table.

One potential issue with `Hashtable` is that it is synchronized, which can impact its performance in situations where only one thread is accessing the table at a time. In those cases, using HashMap or other unsynchronized Map implementations may be more appropriate.

In Java, `HashMaps` and `HashTable`s are both data structures used for key-value mapping. However, there are some differences between the two:

1. Synchronization: `HashTable` is synchronized, which means it is thread-safe and can be used in multi-threaded environments without any additional synchronization. HashMap, on the other hand, is not synchronized by default, which means it is not thread-safe. However, you can make it thread-safe by using the `Collections.synchronizedMap()` method.
2. Null keys and values: `HashTable` does not allow null keys or values, whereas HashMap allows one null key and any number of null values.
3. Iteration: The iterators returned by `HashTable` and HashMap are fail-fast and do not guarantee the order of iteration. However, in practice, HashMap tends to perform better in terms of iteration speed.
4. Inheritance: `HashTable` is a legacy class that was introduced in JDK 1.0, whereas HashMap was introduced in JDK 1.2 as part of the Java Collections Framework. HashMap is the preferred class for key-value mappings in new code.

Overall, if you need thread-safety and do not need to allow null keys or values, you should use `HashTable`. Otherwise, HashMap is generally preferred due to its better performance and flexibility.
