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

You can declare a variable with a value assigned (`const date = new Date();`), or assign a value later. Variables can hold numbers, text (strings), and other kinds of information.

**Note:** JavaScript is case-sensitive, so `date`, `Date`, and `DATE` would all be unique variables.


## Helpful Links

- [Objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects)
- [Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators)
- [Statements and Declarations](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements)
- [Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions)