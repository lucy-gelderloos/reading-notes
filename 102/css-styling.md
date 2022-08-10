# Styling with CSS

Cascading Style Sheets, or CSS, are used to style html files when presented in a browser. CSS can be used in:

- external style sheets that are linked in the head of the document,
- internal style sheets embedded in the head of the document, or
- inline styling of individual html elements

These can be mixed and matched, and documents can link to multiple external CSS sheets.

## Priority

The CSS that applies to a specific element depends on how close it is in the code. Inline styling always takes priority over internal or external style sheets. The order in which any external or internal sheets are applied depends on their order in the head of the document, with later sheets overriding earlier ones.

## Syntax

A CSS rule starts with a **selector**, which determines which html element it applies to. Selectors can apply to, among other things, every instance of an element, elements with a specified class or ID, or elements in a certain state (for instance, links that have been visited can be differentiated from links that haven't).

After the selector comes a set of `{}`, inside of which will be at least one **declaration**. Declarations consist of a **property** (the thing you want to modify) and a **value** (how you want to modify it). Properties can include color, background color, size, position, and many more. 

## Research & Reference

There are so many properties, in fact, that they've been grouped into **modules**, which contain properties with similar features. Keep this in mind when searching for a property, because it can help narrow down your results.

CSS is changing all the time. While the specifications may be overwhelming, they can help understand the code and its relationship to browsers a bit better.

While browsers generally support the same features, the rate of change of CSS means that new features may be implemented unevenly. Make sure to check browser compatibility for all CSS features you want to use.

### MDN Links

- [What is CSS?](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/What_is_CSS)
- [CSS Selectors](https://developer.mozilla.org/en-US/docs/Glossary/CSS_Selector)
- [CSS Colors](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

### W3Schools links

- [How to add CSS](https://www.w3schools.com/css/css_howto.asp)
- [CSS Colors](https://www.w3schools.com/cssref/pr_text_color.asp)