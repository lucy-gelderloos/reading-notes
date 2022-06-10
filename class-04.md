# Code 201 Class 4 - HTML Links, CSS Layout, JS Functions, Pair Programming

## HTML Links

Links use the `<a>` (anchor) element; the text inside the element is called the "link text." The page or spot the link points to is described by the `href` attribute. The href can point to an absolute or relative URL. An absolute URL usually points to an external site, while a relative URL points to another page in the site.

You can also use email links, which include `mailto:` at the beginning of the href and trigger a new email in the user's default email program.

You can use the `target="_blank"` attribute to have the link open in a new tab or window by default.

Finally, you can link to a specific section of a page by pointing to that section's `id` attribute.

## CSS Layout

Key concepts:

- **Block-level** elements always start on a new line. **Normal flow** means that every block-level element sits below the previous one; even very narrow block elements will not appear next to each other. This is the default, so you usually don't need to specify it, but if you do, use `position: static`.
- **Inline elements** flow in between surrounding text
- If an element sits inside another, the outer element is called the `containing` or `parent` element
- **Relative positioning** moves an element relative to where it would have appeared otherwise. Set relative position using `position: relative`.
- **Absolute positioning** positions the element reative to its containing element. When an element is set to `absolute`, other elements act like it's not there. This is useful for popups and flyouts, which you wouldn't want to move your other code around.
- **Fixed positioning** is like absolute, but it positions the element relative to the browser window instead of any containing element
- **Floating** elements are outside of the normal flow and appear to the far right or left of the containing element. Other content in the containing element will flow around the floated element.
- When you start playing with positioning, elements can overlap; the `z-index` property is used to determine what's on top
- Relative and absolute positioning use the `top`, `bottom`, `left`, or `right` offset properties to set the element's position.

## JS Functions

Functions allow you to store blocks of code that you want to reuse and call them with a short command. There are a number of functions built in to JS, or you can write your own. 

Creating a function is known as "declaring" it. Once you've created it, you invoke it by including its name in your code, followed by a set of parentheses.

Some functions require **parameters** to tell them what to do - for instance, a function used to calculate the area of a rectangle would need height and width parameters to work. Parameters are also called **arguments**.

## Pair Programming

Pair programming is a process where one person is the Driver, who actually types the code, and one is the Navigator, who thinks about the big picture during the coding process (and also watches for bugs and typos). Pair programming can seem more time-consuming, but reduces bugs and other issues down the line. It can keep the particiants engaged in the code and help them learn from each other. For this reason, it is often used in professional programming environment.

## Tips

- For relative URLs, if the page is in the same folder, the link can just be the page name. If it's in a different folder, use / to access child folders and ../ to access parent folders.
- Be sure to specify a width for floating elements; if they're as wide as the containing element, they may behave as a block element.

## Best Practices

- Your link text should describe where the link goes (not just "click here")

## Things I Want to Know More About

I want to practice CSS positioning more to understand the ways different layouts work.
