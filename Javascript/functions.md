**Functions in JavaScript**

Functions in JavaScript are reusable blocks of code designed to perform specific tasks. They allow you to organize, reuse, and modularize code. They can take inputs, perform actions, and return outputs.

**Types of Functions**

1. Named Function
A function that has its own name when declared. It’s easy to reuse and debug because the name shows up in error messages or stack traces.

2. Anonymous Function
An anonymous function is a function defined without an explicit name. It is commonly used as a callback or assigned to a variable.

3. Function Expression
A function expression is a function created as part of an expression and assigned to a variable or passed to another function. It can be named or anonymous.

4. Arrow Function (ES6)
A new way to write functions using the => syntax. They are shorter and do not have their own this binding, which makes them useful in some cases.

5. Immediately Invoked Function Expression (IIFE)
IIFE functions are executed immediately after their definition. They are often used to create isolated scopes.

(function () {
    console.log("This runs immediately!");
})();

6. Callback Functions
A callback function is passed as an argument to another function and is executed after the completion of that function.

7. Constructor Function
A special type of function used to create multiple objects with the same structure. It’s called with the new keyword.

8. Async Function
Functions that handle asynchronous tasks. Declared with async, they return a Promise, and you can use await inside them to pause until another Promise resolves

9. Generator Function
Declared with an asterisk *, these functions can pause execution using yield and resume later. Useful for lazy loading values or handling iterators.

10. Recursive Function
A function that calls itself until a condition is met. Very useful for problems like factorial, Fibonacci, or tree traversals.

11. Higher-Order Function
A function that either takes another function as a parameter or returns another function. These are common in JavaScript (e.g., map, filter, reduce).

12. Nested Functions
Functions defined within other functions are called nested functions. They have access to the variables of their parent function.

13. Pure Functions
Pure functions return the same output for the same inputs and do not produce side effects. They do not modify state outside their scope, such as modifying global variables, changing the state of objects passed as arguments, or performing I/O operations.

14. Rest Parameter Function
Uses the ... syntax to collect remaining arguments into an array. Useful when the number of arguments is unknown.

function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3, 4));

# Function Overloading in JavaScript

- Function Overloading is a feature found in many object-oriented programming languages, where multiple functions can share the same name but differ in the number or type of parameters. While languages like C++ and Java natively support function overloading, JavaScript does not support this feature directly.

- In JavaScript, if two or more functions share the same name, the last defined function will overwrite the previous ones. This is because JavaScript treats functions as objects, and a subsequent function with the same name simply reassigns the function reference.

**Objects in JavaScript**
An object is a dynamic data structure that stores related data as key-value pairs, where each key uniquely identifies its value.

* The values of properties can be primitives, objects, or functions (known as methods when defined inside an object).
* Objects are mutable and dynamic properties can be added, modified, or deleted at any time.
* Objects allow data grouping and encapsulation, making it easier to manage related information and behaviour together.

Map	                                                 Object
Stores key-value pairs and allows keys
 of any type (including objects).
	                                                Stores key-value pairs but keys are usually strings or symbols.
Maintains the order of insertion.	                Does not guarantee key order.
Has a built-in size property to get the 
number of entries.	                                No built-in property for size; 
                                                    must be calculated manually.
Iteration is easy using for...of or map.forEach().	Iteration requires for...in or Object.keys      ()/                                                       Object.values().
Better performance for frequent additions and 
removals of key-value pairs.	
                                                    May be slower for frequent  additions/removals of properties.
Can use any value (primitive or object) as a key.	Keys are always converted to strings (except symbols).

