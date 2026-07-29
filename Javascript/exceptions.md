**Javascript Error and Exceptional Handling**

JavaScript error and exception handling helps developers control what happens when something goes wrong during program execution. It ensures the application continues running smoothly while providing useful feedback for debugging.

- Uses try and catch to detect and handle runtime errors safely.
- throw allows creating custom error messages for better clarity.
- finally runs cleanup code regardless of whether an error occurs.

**Types of Errors in JavaScript**
1. Syntax Errors: This happens when the code doesn't follow the correct syntax (e.g., missing parentheses, brackets, or commas).
2. Reference Errors: Occurs when we try to access a variable that hasn’t been declared.
3. Type Errors: This happens when a value is not of the expected type (e.g., trying to call a method on undefined).
4. Range Errors: Occurs when a value is out of range, like passing an invalid number to a function.
5. Custom Errors: A custom error is an error that you create yourself to give more specific messages that make sense for your app. It helps you explain exactly what went wrong in a way that's easy to understand and fix.

**Exception Handling in JavaScript**
Exception handling in JavaScript refers to the process of dealing with errors (exceptions) that occur during the execution of a program. JavaScript provides some mechanisms to catch, handle, and recover from error instead of letting the error stop the program. The most common approach is using try...catch blocks.

# How to create custom errors in JavaScript ?
Syntax of Error Class Instance:

new Error(msg , filename , lineno);

where:
- msg: The error message.
- filename: The file where the error occurs.
- lineno: line number of the error.


