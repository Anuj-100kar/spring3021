**Collections in Java**

A collection in Java is a group of individual objects that are treated as a single unit. In Java, a separate framework named the "Collection Framework" was defined in JDK 1.2, which contains all the Java Collection Classes and interfaces. 

In Java, the Collection interface (java.util.Collection) and Map interface (java.util.Map) are the two main “root” interfaces of Java collection classes.

**Advantages of the Java Collection Framework**

1. Consistent API: Interfaces like List, Set, and Map have common methods across classes (ArrayList, LinkedList, etc.).
2. Less Coding Effort: Developers focus on usage, not designing data structures—supports OOP abstraction.
3. Better Performance: Offers fast, reliable implementations of data structures, improving speed and quality of code.

**Interfaces that Extend the Java Collections Interface**

1. Iterable Interface
Iterable interface is the root of the Collection Framework. It is extended by the Collection interface, making all collections inherently iterable. Its primary purpose is to provide an Iterator to traverse elements, defined by its single abstract method iterator().

Iterator iterator(); 

2. Collection Interface
Collection interface extends Iterable and serves as the foundation of the Collection Framework. It defines common methods like add(), remove(), and clear(), ensuring consistency and reusability across all collection implementations.

3. List Interface
List interface extends the Collection interface and represents an ordered collection that allows duplicate elements. It is implemented by classes like ArrayList, Vector, and Stack. Since all these classes implement List, a list object can be instantiated using any of them

ArrayList , LinkedList , Vector , Stack 

4. Queue Interface
The Queue interface follows the FIFO (First-In, First-Out) principle, where elements are processed in the order they are added—similar to a real-world queue (e.g., ticket booking). It is used when order matters. Classes like PriorityQueue and ArrayDeque implement this interface, allowing queue objects to be instantiated accordingly.

For example:

Queue <T> pq = new PriorityQueue<> (); 
Queue <T> ad = new ArrayDeque<> (); 
Where T is the type of the object.

5. Deque Interface
Deque interface extends Queue and allows insertion and removal of elements from both ends. It is implemented by classes like ArrayDeque, which can be used to instantiate a Deque object.

For example:

Deque<T> ad = new ArrayDeque<> (); 
Where T is the type of the object.  

6. Set Interface
Set interface represents an unordered collection that stores only unique elements (no duplicates). It's implemented by classes like HashSet, TreeSet, and LinkedHashSet, and can be instantiated using any of these
For example:

Set<T> hs = new HashSet<> (); 
Set<T> lhs = new LinkedHashSet<> (); 
Set<T> ts = new TreeSet<> (); 
Where T is the type of the object.  

7. Sorted Set Interface
Sorted Set interface extends Set and maintains elements in sorted order. It includes additional methods for range views and ordering. It is implemented by the TreeSet class.

For example:

SortedSet<T> ts = new TreeSet<> (); 
Where T is the type of the object. 

**Map Interface**
Map is a data structure that supports the key-value pair for mapping the data. This interface doesn't support duplicate keys because the same key cannot have multiple mappings, however, it allows duplicate values in different keys. A map is useful if there is data and we wish to perform operations on the basis of the key. This map interface is implemented by various classes like HashMap, TreeMap, etc.


# Methods of the Collection Interface
* add(Object)
* addAll(Collection c)
* clear()
* contains(Object o)
* containsAll(Collection c)
* equals(Object o)
* hashCode()
* isEmpty()
* iterator()
* parallelStream()
* remove(Object o)
* removeAll(Collection c)
* removeIf(Predicate filter)
* retainAll(Collection c)
* size()
* spliterator()
* stream()
* toArray()