# Closure in JavaScript
A closure is the combination of a function and its lexical environment, allowing the function to access variables from its outer scope even after the outer function has finished executing.

function outer() {
    let outerVar = "I'm in the outer scope!";

    function inner() {
        console.log(outerVar);
    }
    return inner;
}

const closure = outer();

closure();
closure();

- The function inner() forms a closure by retaining access to outerVar, which is a variable in the scope of outer().
- Even though outer() has completed execution, inner() still has access to outerVar due to the closure.

# Lexical Scoping
Closures rely on lexical scoping, which means a function’s scope is determined by where it is defined, not where it is executed.

# IIFEs (Immediately Invoked Function Expressions) use closures to encapsulate data within a function, keeping it private and preventing access from the outside, which helps create self-contained modules.

* Data is scoped to the IIFE.
* Prevents global namespace pollution.
* Uses closures for data privacy.
* Useful for creating modular code.

# JavaScript Hoisting
Hoisting refers to the behavior where JavaScript moves the declarations of variables, functions, and classes to the top of their scope during the compilation phase. This can sometimes lead to surprising results, especially when using var, let, const, or function expressions.

Temporal Dead Zone (TDZ)
The Temporal Dead Zone (TDZ) is the period in JavaScript between entering a scope and the initialization of variables declared with let or const, during which accessing them results in an error.

Types of Hoisting
Hoisting in JavaScript refers to moving declarations to the top of their scope before code execution.

1. Variable Hoisting with var
When you use var to declare a variable, the declaration is hoisted to the top, but its value is not assigned until the code execution reaches the variable’s initialization. This results in the variable being assigned undefined during the hoisting phase.

2. Variable Hoisting with let and const
Unlike var, let and const are also hoisted, but they remain in a Temporal Dead Zone (TDZ) from the start of the block until their declaration is encountered. Accessing them before their declaration will throw a ReferenceError.

3. Function Declaration Hoisting
Function declarations are hoisted with both their name and the function body. This means the function can be called before its definition in the code.

4. Function Expression Hoisting
Function expressions are treated like variable declarations. The variable itself is hoisted, but the function expression is not assigned until the line of execution. This means calling the function before its assignment will result in an error.

5. Hoisting with let and const in Functions
Variables declared with let and const inside a function are hoisted to the top of the function's scope, but they remain in the TDZ. This prevents access to them before they are initialized.

6. Hoisting with Classes
Classes are hoisted, but they cannot be accessed before they are declared, resulting in a ReferenceError.

7. Re-declaring Variables with var
With var, you can redeclare a variable within the same scope. This is a unique behavior compared to let and const.

8. Accessing Variables Declared Later in Loops
When using var in loops, the loop variable is hoisted to the function or global scope, which can cause unexpected behavior. If you use let, the variable is block-scoped and behaves as expected.

9. Using Hoisted Functions with Parameters
Functions can be hoisted with their parameters, but any parameters passed to the function are still determined by the invocation, not by the hoisting.

10. Hoisting in Nested Functions
Hoisting works within nested functions as well. Variables declared with var inside a function are hoisted to the top of that function scope.

# Scope of Variables in JavaScript

# JavaScript Higher Order Functions
A higher-order function is a function that does one of the following:

- Takes another function as an argument.
- Returns another function as its result.

**Popular Higher Order Functions in JavaScript**
1. map
The map function is used to transform an array by applying a callback function to each element. It returns a new array.

const n = [1, 2, 3, 4, 5];
const square = n.map((num) => num * num);
console.log(square);

2. filter
The filter function is used to create a new array containing elements that satisfy a given condition.

const n = [1, 2, 3, 4, 5];
const even = n.filter((num) => num % 2 === 0);
console.log(even);

3. reduce
The reduce function accumulates array elements into a single value based on a callback function.

const n = [1, 2, 3, 4, 5];
const sum = n.reduce((acc, curr) => acc + curr, 0);
console.log(sum);

4. forEach
The forEach function executes a provided function once for each array element.

const n = [1, 2, 3];
n.forEach((num) => console.log(num * 2));

5. find
The find function returns the first element in the array that satisfies a given condition.

const n = [1, 2, 3, 4, 5];
const fEven = n.find((num) => num % 2 === 0);
console.log(fEven);

6. some
The some function checks if at least one array element satisfies a condition.

const n = [1, 2, 3, 4, 5];
const hasNeg = n.some((num) => num < 0);
console.log(hasNeg);

7. every
The every function checks if all array elements satisfy a condition.

const n = [1, 2, 3, 4, 5];
const allPos = n.every((num) => num > 0);
console.log(allPos)

Advanced Techniques with Higher Order Functions
1. Function Composition
Function composition is the process of combining multiple functions to create a new function. The composed function applies multiple operations in sequence.

2. Currying
Currying transforms a function that takes multiple arguments into a series of functions that each take one argument. This allows partial application of the function.

3. Memoization
Memoization is a technique where function results are cached so that repeated calls with the same arguments return faster. This is particularly useful for expensive function calls.

# Debugging in JavaScript
Debugging in JavaScript is the process of identifying and fixing errors in code to make programs run correctly. It helps developers understand unexpected behavior by inspecting variables, checking logic flow, and tracking execution.

Types of Errors in JavaScript
* Syntax Errors: Issues with incorrect syntax, preventing execution.
* Runtime Errors: Errors occurring during execution.
* Logical Errors: Code runs without errors but produces incorrect results.

