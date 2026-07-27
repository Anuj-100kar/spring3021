**Collection Interface in Java**

The Collection interface is the root of the Java Collections Framework, defined in the java.util package. It represents a group of individual objects as a single unit and provides basic operations for working with them.

* Represents a group of objects as a single unit
* Dynamic in size (can grow or shrink)
* Provide simple methods like add(), remove(), and clear().
* Stores elements of a specific type using generics

**Iterator in Java**

An Iterator in Java is one of the most commonly used cursors in the Java Collections Framework. It is used to traverse or iterate through elements of a collection one by one.

* It is used to traverse elements in the forward direction only.
* Removes elements safely during traversal using remove().
* Iterator is a universal cursor that applies to most collection types such as List, Set, and Queue.
* Although Map is part of the Java Collections Framework, it is not a subtype of the Collection interface.
* However, iterators can still be used with Map through keySet(), values(), or entrySet().

Declaration of Iterator
public interface Iterator<E>

Object Creation of Iterator
An Iterator object is created by calling the iterator() method on a collection object. Here, we will use an Iterator to traverse and print each element in an ArrayList.

Collection<String> names = new ArrayList<>();
Iterator<String> itr = names.iterator();

**Java Comparator Interface**

The Comparator interface in Java is used to define custom sorting logic for objects. It belongs to java.util package allows sorting of objects of user-defined classes without modifying their source code. It is especially useful when:

* We need multiple sorting strategies for a class.
* We want to keep sorting logic separate from the class definition.
* Comparator is a functional interface as it contains only one abstract method compare().

Syntax
class MyComparator implements Comparator<Type> {
           public int compare(Type obj1, Type obj2) {
               // comparison logic
      }
}

* Returns negative integer if obj1 < obj2.
* Returns 0 if obj1 == obj2.
* Returns positive integer if obj1 > obj2.

**Methods in Comparator Interface**
* compare(T o1, T o2): Compares two objects for order.
* equals(Object obj): Indicates whether another object is equal to this comparator.

