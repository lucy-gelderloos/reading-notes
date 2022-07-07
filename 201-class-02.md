# Code 201 Class 2 - Basics of HTML, CSS, & JS; Best Practices for Git Commit Messages

## HTML Text

HTML tags (aka markup) tell browsers how to display web pages. Markup can be structural or semantic.

### Structural Markup

Structural markup controls where and how text appears on the page.

- **Headings.** There are six levels of headings that display at decreasing sizes (so by default, heading 1 has very large text and heading 6 has very small text).
- **Paragraphs.** By default, each paragraph starts on a new line and has a line of space after it.
- **Bold & Italic.** Text can be formatted using `<b>` or `<i>`.
- **Superscript & Subscript.** Superscript raises text (like an exponent) and subscript lowers it (like a chemical formula).
- **White Space.** Browsers interpret line breaks and multiple spaces as a single space, enabling coders to use indentation for readability without affecting their code.
- **Line Breaks & Horizontal Rules.** `<br />` is used to add a line break inside an element; `<hr />` inserts a horizontal line between elements. (Note that these are empty elements.)

### Semantic Markup

These elements provide extra, non-structural information on the page.

- **Strong & Emphasis.** Text formatted as `<strong>` has extra importance, while text formatted as `<em>` has an emphasis that slightly changes its meaning. Strong displays as bold by default, while em appears as italic.
- **Quotations.** Use `<blockquote>` for longer quotes that should be set off from other text; use `<q>` for inline quotes. Both elements have a `cite` attribute that can include a URL for attribution.
- **Abbreviations & Acronyms.** When using an abbreviation, you can use the `title` attribute of the `<abbr>` tag to include the full text.
- **Citations & Definitions.** The `<cite>` element is used when referencing another source. `<definition>` is used for the first instance of a term you're defining on your page.
- **Address.** This element contains contact information for the author of the page.
- **Changes to Content.** Use `<ins>` and `<del>` to indicate text that was inserted or deleted, respectively. `<s>` indicates information that is no longer relevant.

## CSS

CSS can be visualized with a box around every HTML element - styling applied to that element will affec the whole "box." A CSS rule has two parts:

- The **selector** specifies which HTML element is being styled
- The **declaration** says what styles should be applied to that element. Declarations include a *property* and a *value* and are enclosed in curly braces.

CSS can be used in external style sheets that are linked to the HTML file, in internal style sheets in the head of the HTML document, and inline. CSS selectors can select elements based on their type, certain attributes, or their position relative to other specified elements.

If multiple CSS rules apply to a particular element, they will be prioritized by proximity and specificity. In some cases, applying a style to an element will apply that style to all child elements (you can force them to inherit using `inherit`).

## Basic JavaScript Instructions

A JavaScript script is a series of instructions. Each individual instruction is known as a *statement* and should end with a semicolon. Curly braces can be used to group statements into code blocks.

### Variables

Variables store information needed to perform the code's function. They are declared using `var` (`let`, `const`); once declared, they can be assigned a value using `=`. Where the variable is declared controls where it can be used.

Variables can store numbers, strings of text, or booleans. Strings need to be enclosed in quotation marks, but numbers don't; booleans can only have be *true* or *false*. There's some flexibility in how variables are declared, and they don't need to be in their own individual statements.

Variables' values can change over the course of the script. The variable doesn't need to be declared again in order to be reused.

#### Rules for Naming Variables

1. Must start with a letter, _, or $ (**never** a number)
2. Can contain the above and numbers, but not . or -
3. Cannot use reserved words or keywords (for instance, you can't name a variable "var")
4. Are case sensitive
5. Should be descriptive
6. Use camel case (if there are multiple words, capitalize the first letter of each word after the first one - firstName, classStartDate, etc.)

#### Arrays

Arrays are a kind of variable that can store a list of values. These values can be generated as the code runs, making arrays much more flexible than a list of individual variables. To declare an array, enclose your list in `[]`.

Each item in the list is assigned a number, **starting at zero**. You can access or change the values from the array using that number.

### Expressions & Operators

There are two types of expressions - ones that assign a value to a variable, and ones that use multiple variables to return a single value. Expressions rely on operators. Three of the most common types of operators are Assignment, Arithmetic, and String operators.

- **Assignment Operators** assign values to variables
- **Arithmetic Operators** do math to variables
- **String Operators** use `+` to join (concatenate) strings

## JavaScript Decisions & Loops

Unless your code is very simple, there will be times when different things happen depending on user input or other activity. When a decision needs to be made, you can set a condition and change the result based on whether the condition is met. You can use **comparison operators** to evaluate the condition and return *true* or *false*, and **logical operators** to compare the results of more than one comparison operator.

The values or variables on either side of the comparison operator are called *operands*. Operands can be expressions (so you could evaluate if (a + b) is greater than (c + d))

### Comparison Operators

- `==` returns `true` if the operands are equal (remember that `=` is an assignment operator and cannot be used for this purpose)
- `!=` returns `true` if the operands are not equal
- `===` returns `true` if the operands are both equal *and* of the same type (string, number, etc.)
- `!==` returns `true` *unless* the operands are equal and of the same type
- `>` and `<` return `true` if the left operand is greater or less than the right operand, respectively
- `>=` and `<=` return `true` if the left operand is greater than or equal to or less than or equal to the right operand, respectively (note that `=>` is the notation for arrow functions and cannot be used for this purpose)

### Logical Operators

- `&&` ("and") returns `true` if both expressions evaluate to `true`
- `||` ("or") returns `true` if **one** of the expressions evaluates as `true` and `false` if they both evaluate to `true`
- `!` ("not") reverses a single boolean value

### If/Then Statements

Once the condition has been evaluated, you can use conditional (if/then/else) statements to tell the code what to do.

`If` statements check if a condition evaluates to `true`, and if it does, executes certain code. If there are no other conditional statements, the code stops. You can use `else` to tell the code what to do if previous conditional statements have evaluated to `false`.

## Git Commit Messages

In order for your commit messages to be helpful both to other developers and to your future self, make sure to follow these best practices. Commit messages should be concise, and should prioritize communicating why a change was made, rather than just describing the change. The comments should have a consistent convention around style, content, and metadata (if you're working in a team, this should be one of the first things you decide on).

### Seven Rules of a Great Commit Message

- Separate subject from body with a blank line. This helps readability for both humans and computers. (It's ok for the commit message to only be the subject line, if more information is not needed.)
- Limit the subject line to 50 characters. This is a convention, not a technical requirement, but it's a widely-used one and helps keep comments concise and readable.
- Capitalize the subject line.
- Do not end the subject line with a period.
- Use the imperative mood in the subject line. One way to think about this is whether your subject line can complete this sentence: "If applied, this commit will..."
- Wrap the body at 72 characters. Git doesn't wrap text automatically, so this helps keep things readable.
- Use the body to explain what and why vs. how. The code will show the changes that were actually made, so use this space to explain why you made them.

## Tips

- CSS comments are enclosed with `/* */`
- In JS, single-line comments start with `//`; multiline comments are enclosed in `/* */`

## Best Practices

- Include a space and a forward slash before the closing bracket of an empty tag: `<br />`, not `<br>`
- Use external style sheets to decrease loading times and make editing easier
- Test your code in multiple browsers to see how it displays
- Because JS is case-sensitive, you could make two different variables with the same name but different capitalization (name vs. Name) - don't do that
- Use strict comparison operators (`===`, `!==`)

## Things I want to know more about

When to use `<b>` vs. `<strong>` and `<i>` vs. `<em>`
