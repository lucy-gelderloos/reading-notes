# Class 03 - Primitives vs. Objects; Exceptions; Scanner

## [Primitives vs. Objects](https://www.baeldung.com/java-primitives-vs-objects)

Java's type system is two-fold, consisting of primitives and reference types (aka Objects). Primitives can be converted to reference types in a process autoboxing, and vice versa in a process called unboxing.

Primitive data types live in the stack and take up slightly less space than reference types, so performance is one consideration when deciding which to use; however, the difference is fairly small and depends on hardware and other environmental factors.

The default value for a primitive type corresponds to its type (so the default for int is 0, not 0.0 or false), but the default value for reference types is always null, even when that doesn't match the data type.

## Exceptions

### [What is an exception?](https://docs.oracle.com/javase/tutorial/essential/exceptions/definition.html)

An *exception* is an event that disrupts the normal flow of a program. *Throwing an exception* refers to the creation of an exception object with information about an error.

*Exception handlers* are blocks of code that tell the program how to deal with exceptions. The runtime system will search up the call stack from the method that caused the exception until it finds a method with an appropriate exception handler. If it doesn't find one, it terminates the program.

### [The Catch or Specify Requirement](https://docs.oracle.com/javase/tutorial/essential/exceptions/catchOrDeclare.html)

For Java code to be considered valid, if it might throw exceptions, it has to be enclosed in either a `try` (to **catch** the exception) or a method with a `throws` clause (to **specify** that it can throw the exception).

- **Checked exceptions** are exceptions the program should have accounted for, like user input with a typo. All exceptions other than errors and runtime exceptions are considered checked and must be handled.
- **Errors** are external to the application, like a hardware issue.
- **Runtime exceptions** are internal errors that couldn't be anticipated, like a bug or improper use of an outside resource.

### [Catching and Handling Exceptions](https://docs.oracle.com/javase/tutorial/essential/exceptions/handling.html)

Exception handlers have three components: try, catch, and finally.

- **Try:** The lines of code that might throw an exception are enclosed in a "try" block. If there is an exception, it will be handled by the catch block immediately after the try block.
  - A try-with-resources statement declares one or more resources, and closes them after the block has run, making it a good choice to reduce cleanup.
- **Catch:** One or more catch blocks can be associated with a try block; no other code can be between the associated blocks. The runtime system will look for the catch block whose ExceptionType matches the current exception. The catch block can have different results, including terminating the program, promting for different input, or send the error to a higher error handler.
- **Finally:** The finally block always runs, which makes it a good place for cleanup code and lets it handle unanticipated exceptions.

## Things I'd like to know more about

Are there standard kinds of errors that should always be anticipated.
