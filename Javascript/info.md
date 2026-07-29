**Introduction to JavaScript**

JavaScript is a versatile, dynamically typed programming language that brings life to web pages by making them interactive. It is used for building interactive web applications and supports both client-side and server-side development.

* Interpreted language: Code is executed line by line.
* Dynamically typed: Variable types are determined at runtime.
* Single-threaded: Executes one task at a time (but supports asynchronous operations).

Features of JavaScript
Here are some key features of JavaScript that make it a powerful language for web development:

1. Client-Side Scripting: JavaScript runs on the user's browser, so it has a faster response time without needing to communicate with the server .
2. Versatile: Can be used for a wide range of tasks, from simple calculations to complex server-side applications.
3. Event-Driven: Responds to user actions (clicks, keystrokes) in real-time.
4. Asynchronous: It can handle tasks like fetching data from servers without freezing the user interface.
5. Rich Ecosystem: There are numerous libraries and frameworks built on JavaScript, such as React , Angular , and Vue.js, which make development faster and more efficient.


**Programming Paradigms in JavaScript**
- Imperative Programming : Focuses on how to perform tasks by controlling the flow of computation. This includes approaches like procedural and object-oriented programming, often using constructs like async/await to handle asynchronous actions.

- Declarative Programming : Focuses on what should be done rather than how it’s done. It emphasizes describing the desired result, such as with arrow functions, without detailing the steps to achieve it.

**Variables and Datatypes in JavaScript**

* Variables: Declared using var, let, and const to store data values.
- Primitive Data Types: Includes Number, String, Boolean, Null, Undefined, BigInt, and Symbol.
- Non-Primitive Data Types: Includes Object, Array, and Function used to store complex data.

# Variables
A variable is like a container that holds data that can be reused or updated later in the program. In JavaScript, variables are declared using the keywords var, let, or const.

1. var Keyword
The var keyword is used to declare a variable. 
It has a function-scoped or globally-scoped behaviour.

2. let Keyword
The let keyword is introduced in ES6, has block scope and cannot be re-declared in the same scope.

3. const Keyword
The const keyword declares variables that cannot be reassigned. It's block-scoped as well.

**JavaScript Operators**

JavaScript operators are symbols or keywords used to perform operations on values and variables. They are the building blocks of JavaScript expressions and can manipulate data in various ways.

1. JavaScript Arithmetic Operators
+ adds two numbers.
- subtracts the second number from the first.
* multiplies two numbers.
/ divides the first number by the second.

2. JavaScript Assignment Operators
= assigns a value to a variable.
+= adds and assigns the result to the variable.
*= multiplies and assigns the result to the variable.

3. JavaScript Comparison Operators
> checks if the left value is greater than the right.
=== checks for strict equality (both type and value).
Other operators include <, <=, >=, and !==.

4. JavaScript Logical Operators
&& returns true if both operands are true.
|| returns true if at least one operand is true.
! negates the boolean value.

5. JavaScript Bitwise Operators
& performs AND operation on each bit.
| performs OR operation on each bit.
^ performs XOR (exclusive OR) on each bit.
~ inverts all bits (NOT operator).
<< shifts bits to the left.
>> shifts bits to the right (with sign).
>>> shifts bits to the right (without sign).

6. JavaScript Ternary Operator
condition ? expression1 : expression2

7. JavaScript Comma Operator
8. JavaScript Unary Operators
+ converts a value to a number.
- negates a value (changes its sign).
++ increments a value by 1.
-- decrements a value by 1.
! converts to boolean and reverses the value (true ↔ false).
typeof returns the data type of a variable.
delete removes a property from an object.

9. JavaScript Relational Operators
* in checks if a property exists in an object.
* instanceof checks if an object is an instance of a constructor.

10. JavaScript BigInt Operators
* Operations like addition, subtraction, and multiplication work with BigInt.
* Use n suffix to denote BigInt literals.

11. JavaScript String Operators
+ concatenates strings.
+= appends to an existing string.

12. JavaScript Chaining Operator (?.)

const obj = { name: "Aman", address: { city: "Delhi" } };
console.log(obj.address?.city);
console.log(obj.contact?.phone);

* ?. safely accesses a property or method.
* Returns undefined if the property doesn’t exist.


# Control Statements in JavaScript

Types of Control Statements in JavaScript
Conditional Statement: 
Iterative Statement:

Approach 1: If Statement
Approach 2: Using If-Else Statement
Approach 3: Using Switch Statement
Approach 4: Using the Ternary Operator (Conditional Operator)
Approach 5: Using For loop
Approach 6: Using While loop
Approach 7: Using Do-While loop

