**Java Packages**

A package in Java is a mechanism to group related classes, interfaces, and sub-packages into a single unit. Packages help organize large applications, avoid naming conflicts, provide access protection, and make code modular and maintainable.

* Avoiding name conflicts (two classes with the same name can exist in different packages)
* Providing access control using public, protected, and default access
* Reusability: packaged code can be imported and used anywhere
* Encouraging modular programming

**Types of Java Packages**

1. Built-in Packages
Built-in Packages comprise a large number of classes that are part of the Java API. Some of the commonly used built-in packages are:

java.lang: Contains language support classes(e.g, classes that define primitive data types, math operations). This package is automatically imported.
java.io: Contains classes for supporting input/output operations.
java.util: Contains utility classes that implement data structures such as Linked Lists and Dictionaries, as well as support for date and time operations.
java.applet: Contains classes for creating Applets.
java.awt: Contains classes for implementing the components for graphical user interfaces (like buttons, menus, etc).

2. User-defined Packages
User-defined Packages are the packages that are defined by the user.

Example : 

package com.myapp;

public class Helper {
    public static void show() {
        System.out.println("Hello from Helper!");
    }
}

To use it in another class:

import com.myapp.Helper;

public class Test {
    public static void main(String[] args) {
        Helper.show();
    }
}

1. Import a Single Class
import java.util.Vector; 

2. Import all classes from a package:
import java.util.*; 

