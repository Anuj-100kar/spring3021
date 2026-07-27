**Classes and Objects in Java**

In Java, classes and objects form the foundation of Object-Oriented Programming (OOP). They help model real-world entities and organize code in a structured way.

* A class is a blueprint used to create objects that share common properties and behavior.
* An object is an instance of a class. It represents a specific entity created from the class template.

**Ways to Create Object in Java**

1. Using new Keyword
2. Using Reflection
class Student {
    public Student() {}
}

public class Main {
    public static void main(String[] args) {
        try {
            Class<?> c = Class.forName("Student");
            Student s = (Student) c.getDeclaredConstructor().newInstance();
            System.out.println(s);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

3. Using clone() method

class Geeks implements Cloneable {
    String name = "GeeksForGeeks";

    @Override
    protected Object clone() throws CloneNotSupportedException {
        return super.clone();
    }

    public static void main(String[] args) {
        try {
            Geeks g1 = new Geeks();
            Geeks g2 = (Geeks) g1.clone();
            System.out.println(g2.name);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

4. Using Deserialization

import java.io.*;

class Student implements Serializable {
    private String name;
    public Student(String name) { this.name = name; }
    public String toString() { return "Student: " + name; }
}

public class Main {
    public static void main(String[] args) {
        try (ObjectOutputStream out =
                new ObjectOutputStream(new FileOutputStream("student.ser"))) {
            out.writeObject(new Student("Alice"));
        } catch (IOException e) { e.printStackTrace(); }

        try (ObjectInputStream in =
                new ObjectInputStream(new FileInputStream("student.ser"))) {
            Student s = (Student) in.readObject();
            System.out.println(s);
        } catch (Exception e) { e.printStackTrace(); }
    }
}


**Object-Oriented Programming (OOP)** is a programming paradigm based on the concept of objects that contain data (fields) and behavior (methods). It focuses on designing software that closely represents real-world entities. It is used to:

* Improves code reusability
* Enhances maintainability and scalability
* Makes programs easier to understand and manage
* Closely models real-world entities

**Constructor**
A Constructor is a special member of a class that is automatically invoked when an object is created. It is primarily used to initialize the object's data members and set up the initial state of an object.

* Default Constructor:
* Parameterized Constructor:
* Copy Constructor:
* Private Constructor:

**Abstraction**
Abstraction in Java is the process of hiding implementation details and showing only the essential features of an object. It helps users focus on what an object does rather than how it does it.

Example: An ATM or a coffee machine represents abstraction, where the user interacts with simple operations while the internal working and implementation details remain hidden.

**How to Achieve Abstraction**
It is achieved in Java using abstract classes and interfaces.
Interfaces can provide 100% abstraction, while abstract classes provide partial abstraction.

**Encapsulation**
Encapsulation is the process of wrapping data and methods into a single unit, usually a class, and restricting direct access to the data. It acts as a protective shield that prevents data from being accessed directly from outside the class.

* Data members are hidden using the private access modifier.
* Access to data is provided through public getter and setter methods.
* It improves data security, maintainability, and controlled access.

**Association is an OOP** concept that defines a relationship between two or more classes that are connected to each other. It represents how objects interact with each other and communicate. In association, objects of one class are related to objects of another class, but they can exist independently.

# Types of Association
1. Aggregation (Weak Association)
Aggregation represents a “has-a” relationship where one class contains a reference to another class, but both can exist independently.

* It is a weak relationship
* Objects have independent lifecycles
* One object can exist without the other

Example: A Company has Employees, but employees can exist independently even if the company no longer exists.

2. Composition (Strong Association)
Composition is a strong form of association where one class owns another class. If the parent object is destroyed, the child object also gets destroyed.

* It is a strong relationship
* Objects have dependent lifecycles
* Child object cannot exist without the parent

Example: A House is composed of Rooms, and if the house is destroyed, the rooms cannot exist independently.

**Inheritance**
Inheritance is a core OOP concept in Java that allows one class to acquire the fields and methods of another class using the extends keyword. It represents an “is-a” relationship between classes.

* The class being inherited is called the superclass, and the inheriting class is the subclass.
* A subclass can use existing features of the superclass and also add its own.
* Inheritance promotes code reusability and reduces redundancy.

Example: Dog, Cat, Cow can be Derived Class of Animal Base Class. 

**Types of Inheritance**
* Single Inheritance:
* Multilevel Inheritance:
* Hierarchical Inheritance:
* Multiple Inheritance (through Interface): A class inherits from multiple interfaces since Java does not support multiple inheritance using classes.
* Hybrid Inheritance (through Interface): A combination of two or more types of inheritance, achievable using interfaces.

**Polymorphism**
Polymorphism means “many forms”, where a single entity can behave differently in different situations. In Java, it allows the same method or object to show different behavior based on context.

* Same method, different behavior depending on the object
* Achieved through method overloading and method overriding

Example: Different animals represent polymorphism, where the same method speak() produces different outputs like Bark, Meow, and Moo depending on the object.

**Types of Polymorphism**
* Compile-time Polymorphism(Method Overloading) :Achieved when multiple methods have the same name but different parameters. The method call is resolved at compile time.
* Runtime Polymorphism (Method Overriding ): Achieved when a subclass provides a specific implementation of a method already defined in its superclass. The method call is resolved at runtime based on the object 

