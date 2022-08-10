# Code 201 Class 3 - HTML Lists, CSS Boxes, JS Control Flow

## Lists

There are three types of lists in HTML:

- **Ordered Lists** are for information that follows a specific order (like instructions in a recipe). They are created with the `<ol>` element, and each item is enclosed in `<li>` tags.
- **Unordered Lists** are for information that doesn't need to be in an order. They are created with the `<ul>` element; like ordered lists, each item uses `<li>`.
- **Definition Lists** are for lists of terms and the definitions of those terms. They are contained in `<dl>` tags. Within that tag, `<dt>` indicates the **t**erm being defined, and `<dd>` indicates the **d**efinition.

You can put an `<li>` element inside another to create a nested list.

## Boxes

CSS treats every HTML element as if it's in its own box. CSS can control the size and display of those boxes.

By default, boxes fit the content inside them, but their width and height can be modified. You can also set a minimum and maximum width and height. If you've set a width or height that makes the box too small to hold its content, you can use the `overflow` property to either hide the extra content or add a scrollbar to the box.

The boxes' display can also be modified with borders, margins, and padding. Borders are always present, but invisible by default; they can be modified using the following properties:

- `border-width` can be set in pixels or use "thin," "medium," or "thick."
- `border-style` includes options likek "solid," "dotted," "dashed," and "double."
- `border-color` controls the color.

The border doesn't have to be the same on every side of the box - for instance, you could use `border-top-color: red;`, `border-right-color: yellow;`, `border-bottom-color: green;`, and `border-left-color: blue;` to set the border of each side to a different color. As a shorthand, you could also use `border-color: yellow red green blue` as a shorthand; note that the order is always clockwise - top, right, bottom, left. To simplify it even more, you can use the `border` property and specify (in this order), the width, style, and color of a border: `border: thin solid blue;`

Padding adds space between the border and the content (note that if a width has been specified, the padding is added to the width). Like borders, you can set padding using `padding-top`, `padding-right`, etc. or you can use shorthand to apply to each side of the box, clockwise.

Margins are outside the border, and create space between different elements. If two elements with margins are next to each other, the margins don't stack and only the largest margin is used. Like padding, the width of the margin is added to the width of the box. You can use the same clockwise shorthand with margins as with borders and padding.

To center a box, set the left and right margins to `auto` to create an equal margin on both sides of the box. Older browsers may require a `text-align` property as well.

All elements display either inline or in a block, but the `display` property can set block elements to inline and vice versa. For example, if you want your list items to all display in a line, you can set `display` to `inline`. `inline-block` uses both inline and block properties. The display property can also be set to `none`, which will make it appear as if the element has been removed from the page (although it will still be visible in the source code).

Boxes can also be hidden using the `visibility` property. Unlike setting `display` to `none`, a box set to `hidden` will still take up space on the page.

CSS3 allows fancier borders - you can use an image for the border, add a shadow, create rounded corners, or even have the border be a different shape (like a circle).

## Decisions & Loops

In class 2's notes, we talked about conditional statements. Another way to do conditionals is to use a switch statement. Rather than an `else` statement, you can use `switch` to provide the code with a number of cases and tell it what to do in which case.

### Data Types

JavaScript uses what is called "type coercion," which means that if it encounters a variable type it doesn't expect (like a string where a number should be), it will try to make the operation work instead of reporting an error. This is different from languages that use "strong typing," where the variable's type must be set and cannot change. To avoid errors related to type coercion, make sure to use strict equals operators.

Because JS treats variables like this, there are a number of values that behave as if they are true or false even though they're not Boolean true/false values. These values are called "truthy" and "falsy." Truthy values include numbers other than zero, strings that aren't blank (include "false" or "0" written as a string), and number calculations. Falsy values include the number zero, empty strings, NaN, and empty variables.

The presence of an object is considered a "true" result for the purposes of conditional statements.

When logical operators return a result, they stop processing. The value that is returned when the code stops is called a "short-circuit" value, and may or may not be a  Boolean true/false value.

### Loops

A loop checks a condition and runs a code block, then re-checks the condition and runs the code again if the condition is still met. A "for" loop runs a specific number of times, while a "while" loop will repeat as long as the condition is met. A "do...while" loop is like a while loop, but always runs at least once.

To set a counter for a for loop, create a variable with value 0, set the condition (i \< 10), and use ++ to increment the variable up by one every time the loop runs.

Loops use the keyword "break" to tell the interpreter to move to the next statement outside the loop, and the keyword "continue" to stop the current iteration and check the condition again.

Loops can be used to apply code to all elements of an array by finding the number of items in the array and running the code that number of times.

Note that when browsers find JavaScript in a page, they stop loading anything until they've processed the code. If you have a loop with a lot of items, it may take a long time to load, and if your loop never evaluates to false, it will keep running until your browser crashes.

## Tips

- When using switch statements, remember to end each case with `break;` so the code knows to move on, and include a `default` option so it knows what to do if none of the cases are met.

## Best Practices

- When setting CSS sizes, consider using percentages or ems rather than pixels so the display can adapt to different screen sizes
- Use strict equals to avoid type coercion

## Things I want to know more about

Still inline vs. block, and especially inline-block - I need to experiment with these more to understand how they work.
