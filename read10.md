---
# JS Debugging
---

## ***Error Handling & Debugging***

![debugging](https://image.slidesharecdn.com/debugging-javascript-web-141030080414-conversion-gate02/95/debugging-javascript-1-638.jpg?cb=1415345877)

Definition: Debugging is the process of detecting and removing of existing and potential errors (also called as 'bugs') in a software code that can cause it to behave unexpectedly or crash. To prevent incorrect operation of a software or system, debugging is used to find and resolve bugs or defects.

The debugger statement stops the execution of JavaScript, and calls (if available) the debugging function. Using the debugger statement has the same function as setting a breakpoint in the code. Normally, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

How to debug JavaScript:

Step 1: Reproduce the bug.
<br>Step 2: Get familiar with the Sources panel UI.
<br>Step 3: Pause the code with a breakpoint.
<br>Step 4: Step through the code.
<br>Step 5: Set a line-of-code breakpoint.
<br>Step 6: Check variable values. Method 1: The Scope pane. Method 2: Watch Expressions. ...
<br>Step 7: Apply a fix.

### What is object error in JavaScript?

Browser support: Represents a run-time error caused by a script operation. JavaScript interpreters throw an Error object, when a script error (exception) occurs. In some cases when the error is caused by a DOM operation, JavaScript interpreters throw an DOMException object, not an Error object.

The Error object in all browsers support the following two properties: 

+ name: The name of the error, or more specifically, the name of the constructor function the error belongs to. 
+ message: A description of the error, with this description varying depending on the browser.