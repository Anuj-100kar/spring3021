**Access Modifiers in Java**

Access modifiers in Java are used to control the visibility and accessibility of classes, methods, and variables. 

* Public modifier: Accessible from anywhere in the program
* Protected modifier: Accessible within the same package and by subclasses
* Private modifier: Accessible only within the same class
* Default modifier: Accessible only within the same package

# Real-World Example :In a banking app, private is used for balance (hidden), default for internal helpers, protected for methods used in subclasses, and public for actions like deposit or view details.

**Types of Access Modifiers**

**Private Access Modifier**
The private access modifier is specified using the keyword private. The methods or data members declared as private are accessible only within the class in which they are declared.

**Default Access Modifier**
If no access modifier is specified, the member has default (package-private) access and can only be accessed within the same package.This means only classes within the same package can access it.

**Protected Access Modifier**
The protected access modifier is specified using the keyword protected. The methods or data members declared as protected are accessible within the same package or subclasses in different packages.

**Public Access Modifier**
The public access modifier is specified using the keyword public. Public members are accessible from everywhere in the program. There is no restriction on the scope of public data members.

**When to Use Access Modifier in Real-World Projects**
1. Private: The idea should be use as restrictive access as possible, so private should be used as much as possible.
2. Default (Package-Private): Often used in package-scoped utilities or helper classes.
3. Protected: Commonly used in inheritance-based designs like framework extensions.
4. Public: This is used for API endpoints, service classes, or utility methods shared across different parts of an application.


**Java Constructors**

A constructor in Java is a special member that is called when an object is created. It initializes the new object’s state. It is used to set default or user-defined values for the object's attributes

* A constructor has the same name as the class.
* It does not have a return type, not even void.
* It can accept parameters to initialize object properties.

**Types of Constructors in Java**

1. Default Constructor
A default constructor has no parameters. It’s used to assign default values to an object. If no constructor is explicitly defined, Java provides a default constructor.

2. Parameterized Constructor
A constructor that has parameters is known as parameterized constructor. If we want to initialize fields of the class with our own values, then use a parameterized constructor.

3. Copy Constructor in Java
Unlike other constructors copy constructor is passed with another object which copies the data available from the passed object to the newly created object.

4. Private Constructor
A private constructor cannot be accessed from outside the class. It is commonly used in:

* Singleton Pattern: To ensure only one instance of a class is created.
* Utility/Helper Classes: To prevent instantiation of a class containing only static methods.

**Constructor Overloading**
This allows us to create multiple constructors in the same class with different parameter lists.

