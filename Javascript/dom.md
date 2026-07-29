**HTML DOM (Document Object Model)**

The HTML DOM (Document Object Model) is a structured representation of a web page that allows developers to access, modify, and control its content and structure using JavaScript. It powers most dynamic website interactions, enabling features like real-time updates, form validation, and interactive user interfaces.

* The HTML Document Object Model (DOM) is a tree structure, where each HTML tag becomes a node in the hierarchy.

**Structure of the HTML DOM**
Imagine your webpage as a tree:

- The document is the root.
- HTML tags like <html>, <head>, and <body> are branches.
- Attributes, text, and other elements are the leaves.

# How to select DOM Elements in JavaScript ?
Selecting DOM (Document Object Model) elements is a fundamental aspect of web development with JavaScript. It allows developers to interact with and manipulate elements on a webpage dynamically. Proper selection of elements is crucial for tasks such as updating content, adding event listeners, or modifying styles.

* Using getElementById
* Using getElementsByClassName
* Using getElementsByTagName
* Using querySelector
* Using querySelectorAll

# JavaScript Custom Events
Custom events are events created by developers to perform specific actions. They allow different parts of an application to communicate without being tightly connected. These events can be linked to elements or objects, and when triggered, they run certain tasks.

**How to Create and Trigger Custom Events?**
To create and trigger a custom event in JavaScript, we typically follow these steps:

- Create an Event: Use the Event constructor to create a new event.
- Add an Event Listener: Attach an event listener to an element or document to listen for the custom event.
- Dispatch the Event: Use the dispatchEvent() method to trigger the event when needed.
Syntax

const eventName = new Event('eventName');
const eventWithData = new CustomEvent('eventWithData', {
    detail: {
        key: 'value'
    }
});

# JavaScript addEventListener() with Examples
The addEventListener() method is used to attach an event handler to an element in the DOM (Document Object Model). It listens for specific events (such as click, keydown, or submit) on that element and executes a function when the event occurs.

Syntax

element.addEventListener(event, function, useCapture);

- element: The DOM element you want to listen for events on (for example, document, button, div).
- event: The type of event you want to listen for, such as 'click', 'keydown', 'submit', etc.
- function: The function to be executed when the event is triggered. It could be an anonymous function or a reference to a named function.
- useCapture (optional): A boolean value that specifies whether to use event capturing.