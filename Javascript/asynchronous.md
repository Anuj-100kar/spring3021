# Asynchronous JavaScript
Asynchronous JavaScript is a programming approach that enables the non-blocking execution of tasks, allowing concurrent operations, improved responsiveness, and efficient handling of time-consuming operations in web applications, JavaScript is a single-threaded and synchronous language. The code is executed in order one at a time, But Javascript may appear to be asynchronous in some situations.

**Approach 1: Using callback**
Callbacks are functions passed as arguments to be executed after an asynchronous operation completes. They are used in asynchronous JavaScript to handle responses and ensure non-blocking execution,

function myFunction(callback) {
    setTimeout(() => {
        const data = { name: "Aman", age: 21 };
        callback(data);
    }, 3000);
}

myFunction((data) => {
    console.log("Data:", data);
});

**Approach 2: Using Promises**
Promises are objects representing the eventual completion (or failure) of an asynchronous operation, providing better handling of asynchronous code with .then() and .catch().

function mydata() {

    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const data = { name: "Rohit", age: 23 };
            resolve(data);
        }, 2000);
    });
}

mydata()
    .then((data) => {
        console.log("Data:", data);
    })
    .catch((error) => {
        console.error("Error:", error);
    });

# A callback function is a function that is passed as an argument to another function and executed later.

**Uses of Callbacks in JavaScript**
1. Handling Asynchronous Operations
2. Callbacks in Functions Handling Operations
3. Callbacks in Event Listeners
4. Callbacks in API Calls (Fetching Data)

**Problems with Callbacks**
1. Callback Hell (Nested Callbacks)
2. Error Handling Issues in Callbacks


JavaScript Promises make handling asynchronous operations like API calls, file loading, or time delays easier. Think of a Promise as a placeholder for a value that will be available in the future. It can be in one of three states

* Pending: The task is in the initial state.
* Fulfilled: The task was completed successfully, and the result is available.
* Rejected: The task failed, and an error is provided.

1. Promise.all() Method
2. Promise.allSettled() Method
3. Promise.race() Method
4. Promise.any() Method
5. Promise.resolve() Method
6. Promise.reject() Method
7. Promise.finally() Method
8. Chaining with Promise.prototype.then() Method
9. Sequential Execution with Array.prototype.reduce()
10. Dynamic Promise Creation
11. Timeout Handling with Promise.race() Method
12. Handling Multiple Failures with Promise.allSettled() Method
13. Combining Promises with Parallel and Sequential Execution
14. Wrapping Callbacks into Promises

# Benefits of Promises
- Avoid Callback Hell: Promises organize asynchronous code more neatly than nested callbacks.
- Error Handling: Errors can be caught in one place using .catch() Method.
- Chaining: Perform tasks sequentially with .then() Method.

# Event Loop in JavaScript
The event loop is an important concept in JavaScript that enables asynchronous programming by handling tasks efficiently. Since JavaScript is single-threaded, it uses the event loop to manage the execution of multiple tasks without blocking the main thread.

**Working of Event Loop**
The event loop continuously checks whether the call stack is empty and whether there are pending tasks in the callback queue or microtask queue.

* Call Stack: JavaScript has a call stack where function execution is managed in a Last-In, First-Out (LIFO) order.
* Web APIs (or Background Tasks): These include setTimeout, setInterval, fetch, DOM events, and other non-blocking operations.
* Callback Queue (Task Queue): When an asynchronous operation is completed, its callback is pushed into the task queue.
* Microtask Queue: Promises (.then(), .catch(), .finally()) and other microtasks are placed here. The microtask queue is always fully executed (drained) before moving to the next macrotask.
* Event Loop: It continuously checks the call stack and, if empty, moves tasks from the queue to the stack for execution.

# Async and Await in JavaScript
Async/Await in JavaScript allows you to write asynchronous code in a clean, synchronous-like manner, making it easier to read, understand, and maintain while working with promises.

* async functions always return a Promise.
* await pauses execution until the Promise is resolved or rejected.
* Improves readability compared to .then() and .catch() chaining.
* Makes error handling simpler using try...catch.
* Ideal for managing complex asynchronous flows in a structured way.

Syntax : 
async function functionName() {
  try {
    const result = await someAsyncFunction();
    console.log(result);
  } catch (error) {
    console.error("Error:", error.message);
  }
}

