# Code 201 Class 6 - Object Literals; the DOM

## JavaScript Object Basics

[MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)

1. How would you describe an object to a non-technical friend you grew up with?

Objects are blocks of code that contain related data and functions. They can include variables (properties) and functions (methods). Each part of the object is called a member; members have a colon between their name and their value and are separated by commas. An object that has all of its methods and properties written out is known as an "object literal." You can use an object as a member of another object.

1. What are some advantages to creating object literals?

Object literals let you reuse code in multiple places without rewriting it, and can help in debugging because related code is all grouped together. Using an object is also more efficient than using each member separately.

1. How do objects differ from arrays?

Arrays store lists of items in a single variable; those items can be accessed by their index. The members of an object can be accessed and modified using their names, through either dot or bracket notation.

1. Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.

You would use bracket notation if you're trying to access a variable rather than a property. Unlike dot notation, bracket notation can be used with strings that include spaces and other special characters.

1. Evaluate the code below. What does the term `this` refer to and what is the advantage to using `this`?

> `const dog = {`
> `name: 'Spot',`
> `age: 2,`
> `color: 'white with black spots',`
> `humanAge: function (){`
> `console.log(${this.name} is ${this.age*7} in human years);`
> `}`
> `}`

`this` is shorthand for the current object. Instead of accessing the `name` property using `dog.name`, using `this` means that line could be reused exactly as-is in other objects with different names.

## Intro to the DOM

[MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

1. What is the DOM?

DOM stands for Document Object Model. It's a way of representing web documents as nodes and objects that allows programs to access and change different parts of a page. The DOM is specifically designed to work with any programming language, although it is usually used with JavaScript.

1. Briefly describe the relationship between the DOM and JavaScript.

The DOM is not part of JavaScript, but without it, there would be no way for JavaScript to access specific parts parts of the HTML document. Using the DOM, JavaScript can work with elements ranging from the whole page to the content of individual cells in a table.

## Things I want to know more about

I think object literals will make more sense as I work with them; right now, they're not making a ton of sense. I'm also interested to see more of what we can do with the DOM to make pages more responsive and interesting.
