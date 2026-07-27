core java ... 

Java is a high-level, object-oriented programming language used to build web apps, mobile applications, and enterprise software systems.

Java is a platform-independent language, which means code written in Java can run on any device that supports the Java Virtual Machine (JVM).


Comments in Java ....

Comments in Java are notes written inside the code that are ignored by the compiler. They are used to improve code readability, explain logic, and make programs easier to maintain.

**Data Types in Java .... **

In Java, data types specify the type of values a variable can hold. They define the size, range and nature of data stored in memory.

**Primitive**: byte, short, int, long, float, double, char, boolean
**Non-Primitive**: String, Arrays, Classes, Interfaces, Objects

**Variables in Java**
Variables are containers to store data in memory. Each variable has a name, type and value.

**Local Variables**: Declared inside a method, constructor, or block. Accessible only within that block.
**Instance Variables**: Declared inside a class but outside any method. Each object of the class has its own copy.
**Static Variables**: Declared with the static keyword inside a class. Shared by all objects of the class.
**Final Variables**: Declared with final keyword. Value cannot be changed once assigned.

**Keywords in Java**
Keywords are reserved words in Java that have a predefined meaning. They cannot be used as variable names, class names or identifiers.

Examples: new, package, private, protected, public, return, short, static, etc.

**Operators in Java**
Operators are symbols that perform specific operations on one or more operands (variables or values). They are used to perform calculations, comparisons, logical operations and manipulate data.

# Arithmetic Operators (+, -, *, /, %)
# Relational Operators (==, !=, >, <, >=, <=)
# Logical Operators (&&, ||, !)
# Assignment Operators (=, +=, -=, *=, /=, %=)
# Unary Operators (+, -, ++, --, !) 
# Ternary Operator (condition ? value_if_true : value_if_false)
# Bitwise Operators (&, |, ^, ~, <<, >>, >>>)

**Decision Making (Control Statements) in Java**
Decision-making (or control statements) are used to execute different blocks of code based on certain conditions. They allow a Java program to choose a path of execution depending on whether a condition is true or false.

* **if**: Executes a block if a condition is true.
* **if-else**: Chooses between two blocks based on a condition.
* **if-else if-else**: Tests multiple conditions sequentially.
* **switch**: Selects one block from multiple options based on a variable’s value.

**Loops in Java**
Loops are control statements in Java that allow a block of code to be executed repeatedly as long as a specified condition is true. They help in reducing code repetition.

* **for**: Used when the number of iterations is known.
* **while**: Used when the number of iterations is not known in advance, condition checked before each iteration.
* **do-while**: Similar to while loop, but condition is checked after executing the block (executes at least once).
* **for-each**: Used to iterate over arrays and collections.


**Java Methods**
Java Methods are blocks of code that perform a specific task.

A method allows to write a piece of logic once and reuse it wherever needed in the program.
This helps keep your code clean, organized, easier to understand and manage.


# Method Call Stack in Java
Java is an object-oriented and stack-based programming language where methods play a key role in controlling the program's execution flow. When a method is called, Java uses an internal structure known as the call stack to manage execution, variables, and return addresses.

# Call Stack
The call stack is a data structure used by the program during runtime to manage method calls and local variables. It operates in a Last-In-First-Out (LIFO) manner, meaning the last method called is the first one to complete and exit.

# Java automatically manages the call stack using the Java Virtual Machine (JVM). .............

**Types of Methods in Java**
1. Predefined Method 
Predefined methods are the method that is already defined in the Java class libraries. It is also known as the standard library method or built-in method.

2. User-defined Method
The method written by the user or programmer is known as a user-defined method. These methods are modified according to the requirement.

* # Different Ways to Create Java Method *
1. Instance Method: Access the instance data using the object name. Declared inside a class.

// Instance Method
void method_name() {
    // instance method body
}

2. Static Method: Access the static data using class name. Declared inside class with static keyword.

// Static Method
static void method_name() {
    // static method body
}

