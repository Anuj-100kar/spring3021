**Java Exception Handling**

Exception Handling in Java is a mechanism used to handle both compile-time (checked) and runtime (unchecked) exceptions, allowing a program to continue execution smoothly even in the presence of errors.

* Handles abnormal conditions that occur during program execution.
* Helps maintain program stability by preventing unexpected termination.

**Basic try-catch Example**
* The try block contains code that might throw an exception,
* The catch block handles the exception if it occurs.

class Geeks{
    public static void main(String[] args) {
        
        int n = 10;
        int m = 0;

        try {
            int ans = n / m;
            System.out.println("Answer: " + ans);
        } catch (ArithmeticException e){
            System.out.println("Error: Division by 0!");
        } 
    }
}

**Finally Block**
The finally block executes after the try and catch blocks in most situations, whether an exception arised or not. It is typically used for closing resources such as database connections, open files, or network connections.

Finally may not execute in cases like:

* System.exit()
* JVM crash
* infinite loop before finally

**throw and throws Keywords**

1. throw: Used to explicitly throw a single exception. We use throw when something goes wrong (or “shouldn’t happen”) and we want to stop normal flow and hand control to exception handling.

class Demo {
    static void checkAge(int age) {
        
        if (age < 18) {
            throw new IllegalArgumentException("Age must be 18 or above");
        }
    }

    public static void main(String[] args) {
        
        checkAge(15);
    }
}

2. throws: Declares exceptions that a method might throw, informing the caller to handle them. It is mainly used with checked exceptions (explained below). If a method calls another method that throws a checked exception, and it doesn’t catch it, it must declare that exception in its throws clause

import java.io.*;

class Demo {

    // Method declares that it may throw IOException
    static void readFile(String fileName) throws IOException {

        // Using try-with-resources to automatically close FileReader
        try (FileReader file = new FileReader(fileName)) {
            int data;
            while ((data = file.read()) != -1) {
                System.out.print((char) data); // Read and print file content
            }
        }
        // No need for finally block to close the resource
    }

    public static void main(String[] args) {

        try {
            readFile("test.txt"); // Attempt to read file
        } catch (IOException e) {
            System.out.println("File not found or error reading file: " + e.getMessage());
        }

        System.out.println("\nProgram continues after file operation.");
    }
}

# Internal Working of try-catch Block:
* JVM executes code inside the try block.
* If an exception occurs, remaining try code is skipped and JVM searches for a matching catch block.
* If found, the catch block executes.
* Control then moves to the finally block (if present).
* If no matching catch is found, the exception is handled by JVM’s default handler.
* The finally block always executes, whether an exception occurs or not.

# Types of Java Exceptions

1. Built-in Exception
Built-in Exception are pre-defined exception classes provided by Java to handle common errors during program execution. There are two type of built-in exception in java.

* Checked Exception: These exceptions are checked at compile time, forcing the programmer to handle them explicitly.
* Unchecked Exception: These exceptions are checked at runtime and do not require explicit handling at compile time.
To know more about Checked and Unchecked Exception -> Checked and Unchecked Exception

2. User-Defined Exception
Sometimes, the built-in exceptions in Java are not able to describe a certain situation. In such cases, users can also create exceptions, which are called "user-defined Exceptions".

Methods to Print the Exception Information
* printStackTrace(): Prints the full stack trace of the exception, including the name, message and location of the error.
* toString(): Prints exception information in the format of the Name of the exception.
* getMessage() : Prints the description of the exception


# Exception - An event that occurs during program execution, disrupting normal flow, which can be handled using try-catch.
# Error -A serious problem that occurs in the JVM, generally cannot be handled by the application.

**Java final, finally and finalize**

In Java, final, finally, and finalize() are three different concepts that serve different purposes. The final keyword is used to restrict changes, finally is used in exception handling, and finalize() is related to garbage collection.

* final prevents modification of variables, methods, and classes.
* finally always executes after the try-catch block.
* finalize() runs before an object is garbage collected (deprecated in Java 9+).

**final Keyword**
The final keyword is used to restrict changes in Java. It can be applied to variables, methods, and classes. Once declared as final, certain modifications are not allowed.

* A final variable cannot be reassigned after initialization.
* A final method cannot be overridden by subclasses.
* A final class cannot be inherited.

**finally Keyword**
The finally block is used in exception handling. It contains code that is executed after the try and catch blocks, regardless of whether an exception occurs or not.

* Always executes after the try-catch block.
* Used for cleanup tasks such as closing files or database connections.
* Executes even if an exception is thrown.

**finalize() Method**
The finalize() method is defined in the Object class and is called by the Garbage Collector before an object is removed from memory. It was traditionally used for cleanup operations.

* Invoked before an object is garbage collected.
* Defined in the Object class.
* Used for resource cleanup before object destruction.

**Null Pointer Exception in Java**

A NullPointerException in Java is a RuntimeException. It occurs when a program attempts to use an object reference that has the null value. In Java, "null" is a special value that can be assigned to object references to indicate the absence of a value.

**Exception Handling with Method Overriding in Java**

Exception handling with method overriding in Java defines how exceptions are declared when a subclass overrides a superclass method. It restricts checked exceptions to maintain type safety and ensure consistent runtime behavior.

* Checked exceptions in the subclass must stay within the superclass method’s declared range.
* Overriding allows reducing or completely removing checked exceptions.
* Ensures safe and predictable behavior during method overriding.

