# Code 201 Class 8 - CSS Layout

## [Learn CSS - FlexBox](https://web.dev/learn/css/flexbox/)

### 1. Flexbox is designed for one-dimensional content. Explain what this means

One-dimensional content exists along one axis (like a row *or* column of a table).

### 2. Explain the difference between the main axis and cross axis

Flexbox can display data along the horizontal or vertical axis. The axis it displays along is the *main axis*, and the other is the *cross axis*. You can use the cross axis to align boxes and to control how items wrap.

### 3. How can using certain properties of flexbox negatively impact accessibility?

By default, the appearance of flexbox elements is controlled by the language of the page (so for a page set to English, flexbox items will move left to right and top to bottom; if the page were set to Arabic, the items will move right to left). This default order can be *visually* reversed using the `row-reverse` or `column-reverse` values, but the browser (and screen readers) will focus on the first element first, even if it *appears* last on the page.

## [MDN - Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)

### What are some advantages of using flexbox over float?

Float allows you to set where an item will appear on the page, but is very limited in terms of setting the item's size - the element will usually resize to fit its content. Unlike float, flexbox allows you to set all your items to take up an equal amount of space or to all be the same height.

### How does this topic connect with your long term goals?

Being able to control exactly where and how content displays is a key requirement of successful design, whether it's for a website or a software GUI. Knowing all the available layout options, even if I don't use them, will help me understand what's possible in this industry.
