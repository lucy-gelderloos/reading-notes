# Code 201 Class 9 - Debugging

## Troubleshooting JavaScript

### 1. Name some key differences between a Syntax Error and a Logic Error

A syntax error is usually a typo or similar issue (like capitalizing variables inconsistently, or using a comma when you need a semicolon). Syntax errors will usually stop the code from running and trigger an error message that will help with troubleshooting.

A logic error is more difficult to troubleshoot, because the code will run without errors, but it won't produce the expected result (like a while loop that runs indefinitely because there's no "false" condition, or trying to use `===` to assign a value to a variable).

### 2. List a few types of errors that you have encountered in past lab assignments and explain how you were able to correct them

In two different projects, I've gotten stuck for about half an hour because I didn't use the right syntax for my for loops (in two different ways, even). I was finally able to correct it by checking the console to see what line the error was on, then comparing it to working loops I'd written previously to see what the differences were.

### 3. How will this topic continue to influence your long term goals?

It's impossible to code without making mistakes. Knowing how to evaluate and address inevitable errors is crucial to working efficiently and writing good code.

## The JavaScript Debugger

### 1. How would you describe the JavaScript Debugger tool and how it works to someone just starting out in software development?

All browsers have tools that allow you to see the underlying code of a page, including HTML, CSS, and JavaScript. One of those tools is a debugger, which can be accessed in Chrome by opening the developer tools and going to the Sources tab. You'll see a list of files, and from there you can open the file you want to test.

### 2. Define what a breakpoint is

You can set breakpoints in your code to pause it as it's running. If your code isn't working how you expect it to, you can use breakpoints to figure out where exactly it goes wrong.

### 3. What is the call stack?

The call stack shows what specifically happened to get to the line of code that you're looking at. Each function that affects that line will be added to the list, in reverse order to how they run. When each function has been fully executed, it is removed from the call stack (this is another place where breakpoints can be useful, so you can see the whole call stack before it gets deleted).

## Things I Want To Know More About

I definitely need to do some debugging in my sales mode page for the cookie stand project, so I'm interested to see how these tools work when applied to my code.
