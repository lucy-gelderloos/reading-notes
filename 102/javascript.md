# Using JavaScript in Web Pages

JavaScript is a programming language mostly (but not exclusively) used in web pages. It's suited for web pages because it's a lightweight language that is compiled "just in time" (roughly speaking, the code is compiled when it's run, not beforehand). This gives JavaScript the speed and low resource use that is needed for interactive websites.

Along with HTML and CSS, JavaScript is one of the main building blocks of the web. Among other things, this means that there are tons of tools and resources already available - you can use JavaScript to:

- interact with and modify HTML and CSS
- modify a site based on the user's location
- create and animate graphics
- play and manipulate audio and video
- and much more!

Many major websites, such as Twitter, have made JavaScript tools available to do things like embed content from their site in yours.

**Note:** JavaScript is not Java! They're owned by the same company, but are entirely different languages.

## Example

You can create a JavaScript function to change an image on your page depending on the time of day:

`function sunOrMoon() {`

This creates a function called "sunOrMoon."

`    const date = new Date();`
`    const hour = date.getHours();`

This defines "date" as today's date and "hour" as the current hour. The date and hour will be re-calculated every time the function is called.

`    if (hour > 6 && hour < 18) {`
`        document.getElementById("sunOrMoon").src="sun.png";`
`    } else {`
`        document.getElementById("sunOrMoon").src="moon.png";`
`    }`
`}`

Here, we say that if the hour is between 6:00 AM and 6:00 PM, the page should display "sun.png"; otherwise, it should display "moon.png."

The image will be displayed in the `<img>` element that has been given the ID `sunOrMoon`. The function must be **later** in the page than the element. If not, the function will be called before the `<img>` element exists, and you'll get an error.

**Like this:**

`<img id="sunOrMoon">`

`<script>sunOrMoon()</script>`

**Not like this:**

`<script>sunOrMoon()</script>`

`<img id="sunOrMoon">`

## Variables

Above, we used `const` to declare the date and hour variables. `const` is one of several ways to declare variables:

- `var` was used to declare all JavaScript variables until `const` and `let` were introduced in 2015. It can be used for local (available in the current function only) or global (available to any function in the current documenet) variables. Use this if you want to be sure your code will run in older browsers.
- `let` declares a local variable
- `const` declares a local constant

Variables must start with a letter, `_`, or `$`, and can include numbers after the first character. 

You can declare a variable with a value assigned (`const date = new Date();`), or assign a value later. Variables can hold numbers, text (strings), functions, and other kinds of information.

Local variables can only be accessed from within their functions, so you can reuse variable names across different functions as long as all those variables are local. Local variables are deleted after the code runs. 

**Note:** JavaScript is case-sensitive, so `date`, `Date`, and `DATE` would all be unique variables.

## Functions

Functions are blocks of code designed for specific tasks. They are defined as follows:

`function newFunction()`

- `newFunction` is the name of the function. Function names follow the same rules as variable names. 
- The parentheses may (but don't have to) include parameters that modify when and how the function is executed.

The code the function is to execute is inside `{}` following the parentheses. 

### Invoking Functions

Functions can be called, or invoked, automatically, when invoked from other JavaScript code, or when an event occurs, like when a user clicks something. When the function is invoked, the code must include (), or else it will return the function itself, rather than the result of the function. 

## Operators

JavaScript has a number of different operators, depending on what you're trying to do. Examples are below; see [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators) for more.

- *Assignment Operators* assigns a value to its left operand (`x = 5`). They have shorthand options that can include operations (`x += 5` is shorthand for `x = x + 5`).
- *Comparison Operators* compare both operands and return `true` or `false` depending on the result. `==` returns `true` if the operands are equal; `>` returns `true` if the left operand is greater than the right.
- *Arithmetic Operators* do math to their operands. `+` adds the operands, `%` divides them and returns the remainder, and `++` increments the operand by one.
- *Logical Operators* are `&&` (AND), `||` (OR), and `!` (NOT). 
- *String Operators* operate on strings! `+` is used to concatenate (combine) multiple strings.
- *Relational Operators* determine whether one operand is `in` the other.

## Control Flow

The "control flow" is the order in which statements in a script are executed. By default, code is executed in the order it's written (for these pages, top to bottom, left to right), but there are many structures that modify that flow, like conditionals and loops. 

## Helpful Links

- [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects)
- [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)
- [Statements and Declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements)
- [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)
- [Control Flow](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow)
- [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)