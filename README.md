# Java Basics Tutorial

**1. Installation and Setup:**
   - To get started with Java, you'll need to install the Java Development Kit (JDK) on your computer. You can download it from the Oracle website (https://www.oracle.com/java/technologies/javase-downloads.html).

**2. Writing Your First Java Program:**
   - Java programs are written in plain text files with a `.java` extension. Here's a simple "Hello, World!" program in Java:

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**3. Variables and Data Types:**
   - Java has various data types, such as `int`, `double`, and `boolean`. You can declare variables like this:

```java
int age = 25;
double price = 9.99;
boolean isJavaFun = true;
```

**4. Operators:**
   - Java supports operators for performing operations on variables and values. For example:

```java
int sum = 5 + 3;
double product = 2.5 * 4.0;
boolean isEqual = (5 == 5);
```

**5. Control Structures:**
   - Java includes control structures like `if`, `else`, `while`, and `for` for making decisions and controlling program flow. Example:

```java
int x = 10;
if (x > 5) {
    System.out.println("x is greater than 5");
} else {
    System.out.println("x is not greater than 5");
}
```

**6. Functions and Methods:**
   - You can create reusable blocks of code called methods or functions. Example:

```java
public static void greet() {
    System.out.println("Hello, from the greet method!");
}

public static void main(String[] args) {
    greet();
}
```

**7. Object-Oriented Programming (OOP):**
   - Java is an object-oriented language. You create classes and objects to encapsulate data and behavior. Example:

```java
public class Person {
    String name;

    public void introduce() {
        System.out.println("Hello, my name is " + name);
    }

    public static void main(String[] args) {
        Person person = new Person();
        person.name = "John";
        person.introduce();
    }
}
```

**8. Input and Output:**
   - Java provides libraries for reading input from the user and displaying output. Example:

```java
import java.util.Scanner;

public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    System.out.print("Enter your name: ");
    String name = scanner.nextLine();
    System.out.println("Hello, " + name);
}
```

**9. Exception Handling:**
   - Java includes exception handling to deal with errors and exceptions. Example:

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("An error occurred: " + e.getMessage());
}
```

**10. Standard Library:**
   - Java has a vast standard library (Java API) that provides pre-built classes and methods for various tasks, such as data structures, file handling, and more.



# Java collections 

**1. ArrayList:**
   - `ArrayList` is a dynamic array that can grow in size. It is part of the List interface and allows you to store elements in a specific order.

   ```java
   ArrayList<String> names = new ArrayList<>();
   names.add("Alice");
   names.add("Bob");
   names.add("Charlie");
   System.out.println(names.get(1)); // Output: "Bob"
   ```

**2. LinkedList:**
   - `LinkedList` is a doubly-linked list, which allows fast insertions and deletions. It is also part of the List interface.

   ```java
   LinkedList<Integer> numbers = new LinkedList<>();
   numbers.add(1);
   numbers.add(2);
   numbers.add(3);
   numbers.remove(1); // Removes the second element
   ```

**3. HashSet:**
   - `HashSet` is an implementation of the Set interface, and it does not allow duplicate elements. Elements are not stored in any specific order.

   ```java
   Set<String> uniqueNames = new HashSet<>();
   uniqueNames.add("Alice");
   uniqueNames.add("Bob");
   uniqueNames.add("Alice"); // Ignored, as it's a duplicate
   ```

**4. HashMap:**
   - `HashMap` is an implementation of the Map interface, used for key-value pairs. It allows you to associate a value with a unique key.

   ```java
   Map<String, Integer> ageMap = new HashMap<>();
   ageMap.put("Alice", 25);
   ageMap.put("Bob", 30);
   System.out.println(ageMap.get("Alice")); // Output: 25
   ```

**5. TreeSet:**
   - `TreeSet` is an implementation of the SortedSet interface and is used to store elements in ascending order.

   ```java
   Set<Integer> numbers = new TreeSet<>();
   numbers.add(3);
   numbers.add(1);
   numbers.add(2);
   System.out.println(numbers); // Output: [1, 2, 3]
   ```

**6. TreeMap:**
   - `TreeMap` is an implementation of the SortedMap interface and allows you to store key-value pairs in ascending order of keys.

   ```java
   Map<String, Integer> ageMap = new TreeMap<>();
   ageMap.put("Alice", 25);
   ageMap.put("Bob", 30);
   ageMap.put("Charlie", 22);
   System.out.println(ageMap); // Output: {Alice=25, Bob=30, Charlie=22}
   ```

**7. Queue (LinkedList):**
   - A `Queue` is used for implementing a first-in, first-out (FIFO) data structure. You can use `LinkedList` to create a basic queue.

   ```java
   Queue<String> queue = new LinkedList<>();
   queue.offer("Alice");
   queue.offer("Bob");
   String firstInLine = queue.poll(); // Removes and retrieves the first element
   ```

**8. Stack:**
   - A `Stack` is used for implementing a last-in, first-out (LIFO) data structure.

   ```java
   Stack<String> stack = new Stack<>();
   stack.push("Alice");
   stack.push("Bob");
   String topOfStack = stack.pop(); // Removes and retrieves the top element
   ```
Certainly! Here are some more examples of Java collections:

**9. Vector:**
   - `Vector` is similar to `ArrayList`, but it is synchronized, making it thread-safe. It can be useful in multi-threaded environments.

   ```java
   Vector<String> vector = new Vector<>();
   vector.add("Apple");
   vector.add("Banana");
   vector.add("Cherry");
   System.out.println(vector.elementAt(1)); // Output: "Banana"
   ```

**10. PriorityQueue:**
   - `PriorityQueue` is an implementation of a priority queue. Elements are stored based on their natural order or according to a specified comparator.

   ```java
   PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();
   priorityQueue.offer(3);
   priorityQueue.offer(1);
   priorityQueue.offer(2);
   System.out.println(priorityQueue.poll()); // Output: 1
   ```

**11. LinkedHashMap:**
   - `LinkedHashMap` is an implementation of `Map` that maintains the order of insertion. It combines the features of `HashMap` and `LinkedList`.

   ```java
   Map<String, Integer> linkedHashMap = new LinkedHashMap<>();
   linkedHashMap.put("One", 1);
   linkedHashMap.put("Two", 2);
   linkedHashMap.put("Three", 3);
   System.out.println(linkedHashMap.keySet()); // Output: [One, Two, Three]
   ```

**12. Concurrent Collections:**
   - Java provides concurrent collections in the `java.util.concurrent` package, such as `ConcurrentHashMap` and `CopyOnWriteArrayList`, designed for concurrent multi-threaded access.

   ```java
   ConcurrentHashMap<String, Integer> concurrentMap = new ConcurrentHashMap<>();
   concurrentMap.put("A", 1);
   concurrentMap.put("B", 2);
   System.out.println(concurrentMap.get("B")); // Output: 2
   ```

**13. EnumSet:**
   - `EnumSet` is a specialized set implementation for enum types. It is highly efficient and type-safe.

   ```java
   enum Days { MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY }
   EnumSet<Days> weekdays = EnumSet.of(Days.MONDAY, Days.TUESDAY);
   ```

**14. BitSet:**
   - `BitSet` represents a set of bits that can be manipulated using logical operations.

   ```java
   BitSet bitSet = new BitSet(8);
   bitSet.set(1);
   bitSet.set(4);
   System.out.println(bitSet); // Output: {1, 4}
   ```

**15. ConcurrentLinkedQueue:**
   - `ConcurrentLinkedQueue` is a thread-safe queue with efficient non-blocking operations, making it suitable for concurrent use.

   ```java
   ConcurrentLinkedQueue<String> concurrentQueue = new ConcurrentLinkedQueue<>();
   concurrentQueue.offer("Alice");
   concurrentQueue.offer("Bob");
   String firstInLine = concurrentQueue.poll(); // Retrieves and removes the first element
   ```
