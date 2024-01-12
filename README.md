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

| Data Type        | Example                 | Range (for primitive types)        |
|------------------|-------------------------|------------------------------------|
| `byte`           | `byte myByte = 10;`     | -128 to 127                        |
| `short`          | `short myShort = 1000;` | -32,768 to 32,767                  |
| `int`            | `int myInt = 100000;`   | -2^31 to 2^31 - 1                  |
| `long`           | `long myLong = 10000000000L;` | -2^63 to 2^63 - 1           |
| `float`          | `float myFloat = 3.14f;` | Approximately ±3.4e38 (7 decimal digits precision) |
| `double`         | `double myDouble = 3.14;`| Approximately ±1.7e308 (15 decimal digits precision)|
| `char`           | `char myChar = 'A';`    | 0 to 65,535 (unsigned 16-bit integer)  |
| `boolean`        | `boolean myBoolean = true;` | N/A (represents true or false)  |

Note: The range values provided for `float` and `double` are approximate and may vary based on the specific implementation of the Java Virtual Machine (JVM).

| Data Type        | Example                                       |
|------------------|-----------------------------------------------|
| `String`         | `String myString = "Hello, Java!";`           |
| `int[]`          | `int[] myArray = {1, 2, 3, 4, 5};`            |
| `interface`      | `interface Printable { void print(); }`      |
| `class`          | `class Person { String name; int age; }`     |
| `enum`           | `enum Day {SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY}` |

These examples illustrate the declaration and initialization of variables with different reference data types in Java:

- `String`: A sequence of characters.
- `int[]`: An array of integers.
- `interface`: A contract for classes to implement certain methods.
- `class`: A blueprint for creating objects with attributes and behaviors.
- `enum`: A special data type representing a set of named constants.

Understanding these reference data types is essential for building complex and structured Java applications. Each data type serves a specific purpose in Java programming.

**4. Operators:**
   - Java supports operators for performing operations on variables and values. For example:

```java
int sum = 5 + 3;
double product = 2.5 * 4.0;
boolean isEqual = (5 == 5);
```

Certainly! Here's a table with examples of common operators in Java:

| Operator Type                 | Operator     | Example                 | Explanation                                      |
|-------------------------------|--------------|-------------------------|--------------------------------------------------|
| **Arithmetic Operators**       | `+`          | `int sum = 5 + 3;`       | Addition                                         |
|                               | `-`          | `int difference = 10 - 4;` | Subtraction                                   |
|                               | `*`          | `int product = 2 * 3;`   | Multiplication                                   |
|                               | `/`          | `double quotient = 8.0 / 2.0;` | Division                                   |
|                               | `%`          | `int remainder = 10 % 3;` | Modulus (Remainder)                              |
| **Relational Operators**       | `==`         | `boolean isEqual = (5 == 5);` | Equality                                        |
|                               | `!=`         | `boolean notEqual = (10 != 5);` | Inequality                                   |
|                               | `>`          | `boolean isGreaterThan = (8 > 3);` | Greater Than                              |
|                               | `<`          | `boolean isLessThan = (4 < 7);` | Less Than                                       |
|                               | `>=`         | `boolean greaterThanOrEqual = (5 >= 5);` | Greater Than or Equal To                   |
|                               | `<=`         | `boolean lessThanOrEqual = (3 <= 6);` | Less Than or Equal To                       |
| **Logical Operators**         | `&&`         | `boolean andResult = (true && false);` | Logical AND                                |
|                               | `||`         | `boolean orResult = (true || false);` | Logical OR                                 |
|                               | `!`          | `boolean notResult = !true;` | Logical NOT                                  |
| **Increment/Decrement**       | `++`         | `int count = 5; count++;` | Increment                                       |
|                               | `--`         | `int value = 8; value--;` | Decrement                                       |
| **Assignment Operators**      | `=`          | `int x = 10;`            | Assignment                                      |
|                               | `+=`         | `int total = 5; total += 3;` | Add and Assign                               |
|                               | `-=`         | `int result = 10; result -= 4;` | Subtract and Assign                      |
|                               | `*=`         | `int productValue = 3; productValue *= 2;` | Multiply and Assign                  |

These examples cover a range of operators, including arithmetic, relational, logical, increment/decrement, and assignment operators commonly used in Java programming.

**5. Control Structures:**
   - Java includes control structures like `if`, `else`, `while`, and `for` for making decisions and controlling program flow. Example:

###  **if-else Statement:**
   - The `if-else` statement is used to make decisions based on a condition.

   ```java
   int number = 10;

   if (number > 0) {
       System.out.println("Number is positive");
   } else {
       System.out.println("Number is non-positive");
   }
   ```

### **Switch Statement:**
   - The `switch` statement is used to select one of many code blocks to be executed.

   ```java
   int dayOfWeek = 3;

   switch (dayOfWeek) {
       case 1:
           System.out.println("Monday");
           break;
       case 2:
           System.out.println("Tuesday");
           break;
       // ... other cases ...
       default:
           System.out.println("Invalid day");
   }
   ```

### **for Loop:**
   - The `for` loop is used for iterating over a range of values.

   ```java
   for (int i = 0; i < 5; i++) {
       System.out.println("Iteration: " + i);
   }
   ```

### **while Loop:**
   - The `while` loop repeats a block of code as long as a specified condition is true.

   ```java
   int count = 0;

   while (count < 3) {
       System.out.println("Count: " + count);
       count++;
   }
   ```

### **do-while Loop:**
   - The `do-while` loop is similar to the `while` loop, but it guarantees that the code inside the loop is executed at least once.

   ```java
   int i = 0;

   do {
       System.out.println("i: " + i);
       i++;
   } while (i < 3);
   ```

###  **break and continue:**
   - The `break` statement is used to exit a loop prematurely, and `continue` is used to skip the rest of the loop and move to the next iteration.

   ```java
   for (int i = 0; i < 10; i++) {
       if (i == 5) {
           break; // exit the loop when i is 5
       }
       if (i % 2 == 0) {
           continue; // skip even numbers
       }
       System.out.println("Odd number: " + i);
   }
   ```

### **Nested Control Structures:**
   - Control structures can be nested within each other to create more complex logic.

   ```java
   for (int i = 1; i <= 3; i++) {
       for (int j = 1; j <= 3; j++) {
           System.out.println("i: " + i + ", j: " + j);
       }
   }
   ```

These examples showcase the use of control structures in Java for making decisions, iterating over values, and controlling the flow of execution in a program.

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

In Java, functions are known as methods. Methods in Java are blocks of code that perform a specific task and are defined within a class. They are used to organize code, make it reusable, and encapsulate functionality. Here are the key aspects of methods in Java:

###  **Method Declaration:**
   - A method is declared using the following syntax:

     ```java
     return_type method_name(parameter_list) {
         // method body
     }
     ```

   - `return_type`: Specifies the type of value that the method returns, or `void` if the method does not return any value.
   - `method_name`: Name of the method.
   - `parameter_list`: List of input parameters (if any).

###  **Example of a Simple Method:**
   - A method that adds two numbers and returns the result:

     ```java
     public class Calculator {
         public static int add(int a, int b) {
             return a + b;
         }

         public static void main(String[] args) {
             int result = add(5, 3);
             System.out.println("Sum: " + result);
         }
     }
     ```

###  **Method Overloading:**
   - Java supports method overloading, allowing multiple methods with the same name but different parameter lists or types.

     ```java
     public class MathOperations {
         public static int add(int a, int b) {
             return a + b;
         }

         public static double add(double a, double b) {
             return a + b;
         }
     }
     ```

###  **Static and Non-Static Methods:**
   - Methods can be static or non-static.
   - Static methods belong to the class rather than an instance and can be called using the class name.
   - Non-static methods are associated with an instance of the class.

     ```java
     public class MyClass {
         // Static method
         public static void staticMethod() {
             // method body
         }

         // Non-static method
         public void nonStaticMethod() {
             // method body
         }
     }
     ```

###  **Return Statement:**
   - The `return` statement is used to exit a method and can also return a value if the method has a non-void return type.

     ```java
     public static int square(int num) {
         return num * num;
     }
     ```

###  **Void Methods:**
   - Methods with the `void` return type do not return any value.

     ```java
     public static void greet() {
         System.out.println("Hello!");
     }
     ```

###  **Parameters:**
   - Methods can have parameters, which are variables that hold values passed to the method.

     ```java
     public static int add(int a, int b) {
         return a + b;
     }
     ```

###  **Main Method:**
   - The `main` method is the entry point of a Java program.

     ```java
     public static void main(String[] args) {
         // program execution starts here
     }
     ```

These concepts provide a foundation for understanding methods in Java. Methods play a crucial role in structuring Java programs and promoting code reuse.




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

Object-oriented programming (OOP) is a programming paradigm that is based on the concept of "objects," which can encapsulate data and behavior. Java is a fully object-oriented programming language, and OOP principles are fundamental to its design. Here are the key concepts of object-oriented programming in Java:

### **Classes and Objects:**
   - **Class:** A class is a blueprint or template for creating objects. It defines the properties (fields/attributes) and behaviors (methods) that objects of the class will have.
   
   ```java
   public class Car {
       // Fields/Attributes
       String model;
       int year;

       // Methods
       void start() {
           System.out.println("Car started");
       }

       void stop() {
           System.out.println("Car stopped");
       }
   }
   ```

   - **Object:** An object is an instance of a class. It represents a real-world entity and has its own state (values of fields) and behavior (execution of methods).

   ```java
   Car myCar = new Car();
   myCar.model = "Toyota";
   myCar.year = 2022;
   myCar.start();
   ```

### **Encapsulation:**
   - Encapsulation is the bundling of data (fields) and methods that operate on that data into a single unit known as a class. It helps in hiding the internal details of the object.

   ```java
   public class Student {
       private String name;
       private int age;

       // Getter and setter methods
       public String getName() {
           return name;
       }

       public void setName(String name) {
           this.name = name;
       }

       // Similar methods for 'age'
   }
   ```

### **Inheritance:**
   - Inheritance is a mechanism where a new class (subclass/derived class) inherits properties and behaviors from an existing class (superclass/base class).

   ```java
   public class ElectricCar extends Car {
       // Additional fields and methods specific to ElectricCar
   }
   ```

### **Polymorphism:**
   - Polymorphism allows objects to be treated as instances of their parent class. It includes method overriding and method overloading.

   ```java
   // Method Overriding
   @Override
   void start() {
       System.out.println("Electric car started");
   }

   // Method Overloading
   void charge() {
       System.out.println("Charging the electric car");
   }

   void charge(int hours) {
       System.out.println("Charging the electric car for " + hours + " hours");
   }
   ```

### **Abstraction:**
   - Abstraction is the process of simplifying complex systems by modeling classes based on the essential properties and behaviors they possess.

   ```java
   abstract class Shape {
       abstract void draw(); // Abstract method
   }

   class Circle extends Shape {
       void draw() {
           System.out.println("Drawing a circle");
       }
   }
   ```

### **Interfaces:**
   - Interfaces define a contract for classes that implement them. They consist of abstract methods that must be implemented by the classes.

   ```java
   interface Printable {
       void print();
   }

   class Document implements Printable {
       public void print() {
           System.out.println("Printing a document");
       }
   }
   ```

### **Composition:**
   - Composition involves creating relationships between objects by including other objects as fields. It allows for building complex objects from simpler ones.

   ```java
   public class Computer {
       private CPU cpu;
       private RAM ram;

       // Constructor, getter, setter, etc.
   }
   ```

These OOP concepts provide a powerful and flexible way to design and structure Java programs, making code more modular, reusable, and easier to maintain. They support the principles of encapsulation, inheritance, polymorphism, and abstraction, contributing to a well-organized and scalable software architecture.

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

In Java, input and output are handled using the `java.util.Scanner` class for input and the `System.out.println` statement for output. Here's a brief overview of how input and output are typically done in Java:

### Input in Java:

To get input from the user, you can use the `Scanner` class. First, you need to import it:

```java
import java.util.Scanner;
```

Then, you can create a `Scanner` object to read input from the keyboard:

```java
Scanner scanner = new Scanner(System.in);
```

Now, you can use various methods of the `Scanner` class to get input:

```java
System.out.print("Enter an integer: ");
int number = scanner.nextInt();

System.out.print("Enter a double: ");
double decimal = scanner.nextDouble();

System.out.print("Enter a string: ");
String text = scanner.next();
```

Remember to close the `Scanner` when you're done:

```java
scanner.close();
```

### Output in Java:

To output data to the console, you can use the `System.out.println` statement:

```java
int number = 42;
System.out.println("The value of number is: " + number);

double decimal = 3.14;
System.out.println("The value of decimal is: " + decimal);

String text = "Hello, Java!";
System.out.println("The value of text is: " + text);
```

You can also format output using `printf`:

```java
int number = 42;
System.out.printf("The value of number is: %d%n", number);

double decimal = 3.14;
System.out.printf("The value of decimal is: %.2f%n", decimal);

String text = "Hello, Java!";
System.out.printf("The value of text is: %s%n", text);
```

In addition to the console, Java provides other I/O classes for reading from and writing to files, working with streams, etc. These include classes like `FileReader`, `FileWriter`, `BufferedReader`, and `BufferedWriter`. These classes offer more advanced capabilities for handling input and output operations in various scenarios.

**9. Exception Handling:**
   - Java includes exception handling to deal with errors and exceptions. Example:

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("An error occurred: " + e.getMessage());
}
```

Exception handling in Java is a mechanism to handle runtime errors (exceptions) in a program. Exceptions are unexpected events that occur during the execution of a program and can disrupt the normal flow of the program. Java provides a robust and comprehensive exception-handling mechanism to deal with such situations.

Here are the key components of exception handling in Java:

### **try-catch Block:**
   - The `try` block contains the code that might throw an exception. The `catch` block handles the exception if it occurs.

   ```java
   try {
       // code that may throw an exception
   } catch (ExceptionType1 ex1) {
       // handle ExceptionType1
   } catch (ExceptionType2 ex2) {
       // handle ExceptionType2
   } finally {
       // optional block, always executed whether an exception occurs or not
   }
   ```

### **Example:**
   - Here's an example of handling an `ArithmeticException`:

   ```java
   try {
       int result = 10 / 0; // This line will throw an ArithmeticException
   } catch (ArithmeticException ex) {
       System.out.println("ArithmeticException caught: " + ex.getMessage());
   }
   ```

### **Multiple catch Blocks:**
   - You can have multiple `catch` blocks to handle different types of exceptions.

   ```java
   try {
       // code that may throw an exception
   } catch (ExceptionType1 ex1) {
       // handle ExceptionType1
   } catch (ExceptionType2 ex2) {
       // handle ExceptionType2
   } catch (ExceptionType3 ex3) {
       // handle ExceptionType3
   }
   ```

### **finally Block:**
   - The `finally` block is optional and is used to specify code that will be executed regardless of whether an exception is thrown or not.

   ```java
   try {
       // code that may throw an exception
   } catch (Exception ex) {
       // handle exception
   } finally {
       // code that will always be executed
   }
   ```

### **Throwing Exceptions:**
   - You can use the `throw` statement to explicitly throw an exception.

   ```java
   if (someCondition) {
       throw new CustomException("This is a custom exception");
   }
   ```

### **Creating Custom Exceptions:**
   - You can create your own exception classes by extending the `Exception` class or one of its subclasses.

   ```java
   class CustomException extends Exception {
       // constructor and additional methods
   }
   ```

### **Try-with-Resources:**
   - Introduced in Java 7, the try-with-resources statement automatically closes resources like files, sockets, etc., after they are no longer needed.

   ```java
   try (FileReader fr = new FileReader("file.txt")) {
       // code that uses FileReader
   } catch (IOException ex) {
       // handle exception
   }
   ```

### **Common Exception Classes:**
   - Java provides a variety of predefined exception classes, such as `ArithmeticException`, `NullPointerException`, `ArrayIndexOutOfBoundsException`, `FileNotFoundException`, etc.

Exception handling in Java helps improve the robustness of the code by providing a structured way to deal with unexpected situations. It allows developers to gracefully handle errors and prevent the abrupt termination of the program.

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
