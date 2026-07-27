**Arrays in Java**

An array is a collection of elements of the same data type stored in contiguous memory locations. It allows multiple values to be stored under a single name and accessed using an index.

* primitive array stores the values directly in the memory.
* each element of the object array stores a reference to seperate string object.

# declaration of array 
int arr[] or int[] arr

Once an array is created, its size is fixed and cannot be changed. For collections that can grow or shrink dynamically, Java provides classes like ArrayList or Vector.
Memory for arrays is always allocated on the heap in Java.
The elements in the array allocated by new will automatically be initialized to zero (for numeric types), false (for boolean) or null (for reference types).

# Arrays of Objects in Java
An array of objects is created like an array of primitive-type data items

# Advantages of Java Arrays
1. Efficient Access
2. Memory Management
3. Data Organization

# Limitations of Java Arrays
1. Fixed Size
2. Type Homogeneity - stores only same data type so use classes, collections...
3. Costly Insertion & Deletion


## Java Strings ##

A String in Java is an object used to store a sequence of characters enclosed in double quotes. It uses UTF-16 encoding and provides methods for handling text data.

* Each character in a string is stored using 16-bit Unicode (UTF-16) encoding.
* Strings are immutable, meaning their value cannot be changed after creation.
* Java provides a rich API for manipulation, comparison, and concatenation of strings.

## Interfaces and Classes in Strings in Java ## 

**Classes that implement CharSequence include** 
* String: An immutable class whose contents cannot be modified after creation; any change results in a new String object.
* StringBuffer: A mutable and thread-safe class used for string manipulation in multithreaded environments.
* StringBuilder: A mutable and non-thread-safe class that provides faster string manipulation in single-threaded applications.
* StringTokenizer: A utility class used to break a string into smaller tokens based on specified delimiters.

**Immutable String in Java**
