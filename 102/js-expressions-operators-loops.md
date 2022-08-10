# JavaScript Expressions, Operators, and Loops

## Expressions and Operators

Operators affect (operate on) *operands*. Most JavaScript operators are unary, meaning they have one operand, or binary, meaning they have two operands - a left one and a right one. 

### Comparison Operators

Comparison operators compare their operands and return `true` or `false` depending on the result. 

- `==` returns `true` if the operands are equal (remember that `=` is an assignment operator and cannot be used for this purpose)
- `!=` returns `true` if the operands are not equal
- `===` returns `true` if the operands are both equal and of the same type (string, number, etc.)
- `!==` returns `true` *unless* the operands are equal and of the same type
- `>` and `<` return `true` if the left operand is greater or less than the right operand, respectively
- `>=` and `<=` return `true` if the left operand is greater than or equal to or less than or equal to the right operand, respectively (note that `=>` is the notation for arrow functions and cannot be used for this purpose)

### Assignment Operators

Assignment operators use the right operand to assign a value to the left operand:

`x = 5`

`x = b + 2`

There are also compound operators that include other operations:

`x += 5` means `x = x + 5` (incrementing by a value of 5)

Assignment operators are usually used within variable declarations, but they do evaluate into a result value, which can be used by other expressions. Because this technique is rarely used, it is generally discouraged, and can have surprising results.

## Loops

Loops allow you to automatically repeat a piece of code until certain conditions are met. 

### For Statement

`for` loops repeat until a specified condition evaluates to `false`. A `for` statement looks like this:

`for ([initialExpression], [conditionExpression], [incrementExpression])`

`statement`

`initialExpression` is usually used to initialize a loop counter, but can be as complex as you need it to be. If `conditionExpression` evaluates to "false," the loop stops; if it evaluates to "true," or if there is no `conditionExpression`, the loop continues. Although it comes last, the `statement` executes next, performing whatever code the loop is controlling. Finally, the `incrementExpression` executes, incrementing the loop counter. 

### While Statement

Like a `for` statement, a `while` statement executes as long as a specified condition evaluates as "true." Unlike a `for` statement, `while` statements do not run for a known number of iterations. The condition is tested before the statement is executed; if it's true, the statement is executed, and if it's false, control moves to the next statement.

**Note:** Make sure the condition you base your `while` statement on will eventually evaluate to "false," or your loop will continue forever.