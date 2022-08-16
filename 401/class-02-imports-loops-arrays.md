# Java Imports, Loops, and Arrays

## Imports

## Loops

Loops allow for the executino of a piece of code until a certain condition is met.

*For loops* allow a loop to run for a specified number of times (or infinitely, in some cases). For loops have an initialization (an integer, usually 0), a boolean expression (when this is false, the loop will stop), and a step (the change to make to the initializing integer). If all three are blank, the loop will run forever.

For loops can be labeled; if they are, you can access groups by label to break or continue them.

*Enhanced* for loops allow for the declaration of an array or other source and an element, and will iterate over the element.

*Iterable.forEach* methods allow us to iterate over an iterable object.

*While loops* execute a block of code while a boolean expression is true. If the expression evaluates to false before the code runs, it won't run at all.

*Do while* loops work like while loops, except the code block runs at least once,even if the boolean expression doesn't evaluate to true.

## Arrays

Arrays are variables that contain many values. They have a fixed size and are sequential (the values are always in the same order). Their values can be accessed using their index, which is zero-based (that is, the first array element will have an index of 0). Because the number and order of the elements don't change, for and forEach loops work very well with arrays. Arrays can be passed to methods as parameters, and returned from methods.

- Declare: `dataType[] arrayRefVar` (to declare an array of integers called "numbers": `int[] numbers`)
- Create: `arrayRefVar = new dataType[arraySize]` (to create the "numbers" array and set it to a length of 3: `numbers = new int[3]`)
- Declare and create: `dataType[] arrayRefVar = new dataType[arraySize]` (`int[] numbers = new int[3])

## Things I want to know more about

How working with arrays and loops is different between Java and Javacript.
