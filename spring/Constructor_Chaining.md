**Constructor Chaining In Java with Examples**

Constructor chaining is the process of calling one constructor from another constructor within the same class or from a parent class. It helps reduce code duplication and improves code readability by reusing existing constructor logic. Constructor chaining is achieved using the this() and super() keywords.

* Uses this() for constructors within the same class.
* Uses super() to call a parent class constructor.

**Types of Constructor Chaining in Java**

1. Constructor Chaining Within the Same Class Using this()
Constructor chaining within the same class occurs when one constructor calls another constructor of the same class using the this() keyword. It is mainly used to reuse initialization code between multiple constructors.

* this() calls another constructor of the same class.
* It must be written as the first statement in a constructor.

class Temp
{
    // default constructor 1
    // default constructor will call another constructor
    // using this keyword from same class
    Temp()
    {
        // calls constructor 2
        this(5);
        System.out.println("The Default constructor");
    }

    // parameterized constructor 2
    Temp(int x)
    {
        // calls constructor 3
        this(5, 15);
        System.out.println(x);
    }

    // parameterized constructor 3
    Temp(int x, int y)
    {
        System.out.println(x * y);
    }

    public static void main(String args[])
    {
        // invokes default constructor first
        new Temp();
    }
}

2. Constructor Chaining Using super() (Parent Class) 

Constructor chaining between classes occurs when a child class constructor calls the parent class constructor using the super() keyword. It ensures that the parent class object is initialized before the child class object.

* It must be the first statement in the child class constructor.
* Used in inheritance to initialize superclass members.

class Base
{
    String name;

    // constructor 1
    Base()
    {
        this("");
        System.out.println("No-argument constructor of" + 
                                           " base class");
    }

    // constructor 2
    Base(String name)
    {
        this.name = name;
        System.out.println("Calling parameterized constructor" 
                                              + " of base");
    }
}

class Derived extends Base
{
    // constructor 3
    Derived()
    {
        System.out.println("No-argument constructor " + 
                           "of derived");
    }

    // parameterized constructor 4
    Derived(String name)
    {
        // invokes base class constructor 2
        super(name);
        System.out.println("Calling parameterized " + 
                           "constructor of derived");
    }

    public static void main(String args[])
    {
        // calls parameterized constructor 4
        Derived obj = new Derived("test");

        // Calls No-argument constructor
        // Derived obj = new Derived();
    }
}


Advantages of Constructor Chaining
1. Avoids code duplication
2. Improves code readability
3. Makes constructor management easier
4. Provides better object initialization
5. Supports inheritance-based initialization
