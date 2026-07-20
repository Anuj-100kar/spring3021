**Collections Class in Java**

The Collections class in Java is a utility class provided by the Java Collections Framework that contains static methods for performing common operations on collections. It simplifies tasks like sorting, searching, and modifying collection elements efficiently.

* Provides methods such as sort(), reverse(), shuffle(), and binarySearch()
* Helps improve code readability and performance without manual implementation

**Java Collections Classes**

Collection Framework contains both classes and interfaces. Although both seem the same but there are certain differences between Collection classes and the Collections framework.

1. List Implemented Classes
Lists are ordered collections that allow duplicates.

* ArrayList: A resizable array that maintains insertion order. Allows duplicates and provides fast random access.
* LinkedList: Implements a doubly-linked list. Can be used as List, Stack, or Queue.
* Vector: Synchronized resizable array. Slower than ArrayList but thread-safe.
* Stack: Extends Vector. Follows LIFO (Last-In-First-Out) principle for storing elements.

2. Set Implemented Classes
Sets are unordered collections that do not allow duplicates.

* HashSet: Stores elements in a hash table. Offers fast insertion, deletion, and search.
* LinkedHashSet: Maintains insertion order using a doubly-linked list internally.
* TreeSet: Stores elements in sorted order. Implements SortedSet and ensures natural or custom ordering.

3. Queue Implemented Classes
Queues hold elements prior to processing, typically following FIFO, but can support priority.

* PriorityQueue: Orders elements based on priority or a custom comparator.
* ArrayDeque: Double-ended queue using a resizable array. Can function as a stack or queue.
* LinkedList: Can also be used as a Queue. Maintains insertion order and allows duplicates

4. Map Implemented Classes
Maps store key-value pairs with unique keys. Not part of the Collection interface but part of JCF.

* HashMap: Stores key-value pairs with fast access. Allows one null key and multiple null values.
* LinkedHashMap: Maintains insertion order of keys.
* TreeMap: Keys are sorted either naturally or with a custom comparator.
* Hashtable: Synchronized map. Does not allow null keys or null values.
* EnumMap: Specialized map for enum keys. Efficient storage and fast access.
* WeakHashMap: Uses weak references for keys. Unreferenced keys can be garbage collected.
* IdentityHashMap: Uses reference equality (==) instead of equals() for key comparison.
* ConcurrentHashMap: Thread-safe map optimized for concurrent access by multiple threads.

5. Abstract Base Classes
These classes provide common functionalities and simplify implementation of concrete collection classes.

* AbstractCollection: Base class for implementing custom collections.
* AbstractList: Base class for List implementations. Provides default methods for lists.
* AbstractSet: Base class for Set implementations. Provides default methods for sets.
* AbstractMap: Base class for Map implementations. Simplifies map creation.
* AbstractQueue: Base class for Queue implementations. Provides basic queue operations.

