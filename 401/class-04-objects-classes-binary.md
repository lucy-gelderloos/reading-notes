# Class 04 - Object and Class Tutorial; Java Classes; Binary, Decimal, and Hexadecimal Numbers

## [Java OO Tutorial](https://docs.oracle.com/javase/tutorial/java/concepts/)

Software objects, like real-world objects, have state and behavior. Encapsulation means hiding variables and requiring that any other object interact with this object through methods. For example, an internal setProperty method could limit the available values for that property (between 0 and 59 minutes, for example), so any other method trying to add an invalid property (90 minutes, -4 minutes) receives an error.

Classes are bluprints for objects. A class doesn't have a main method; it is used by other classes to create objects for their use.

## [Java Classes](https://docs.oracle.com/javase/tutorial/java/javaOO/classes.html)

Classes have:

- fields
- a constructor
- methods

Classes can extend (be subclasses of) other classes, which allows the subclass to use the fields and methods of the parent class.

## [Binary, Decimal, and Hexadecimal Numbers](https://www.mathsisfun.com/binary-decimal-hexadecimal.html)

Decimal numbers (aka base ten) use the symbols 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9. To express a number greater than nine, we use the next "place" to specify how many tens, 100s, etc. are in the number.

Binary numbers (aka base two) only use the symbols 0 and 1. Again, to express a higher number, we move a place to the left - zero is 0, one is 1, two is 10, three is 11, four is 100, etc.

Hexadecimal numbers (aka base 16) uses the symbols 0-9, plus a, b, c, d, e, and f to express high numbers in a more compact format. For instance, two hundred and fifty in hexadecimal is FA; one million is F4240.
