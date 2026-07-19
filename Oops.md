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