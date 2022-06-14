# Code 201 Class 7 - HTML Tables; JS Constructor Functions

## Domain Modeling

A model describes a group of interconnected items and behaviors. In software development, a domain model would describe a problem or project, including what entities are involved, how they behave, and what their limitations might be. Domain modeling can serve as a roadmap for a project, and can be a crucial tool in communication between the development team and otehr staeholders.

## HTML Table Basics

Fundamentally, tables are data arranged into rows and columns. They show connections between various data points (like which class is on what day of the week, or what each menu item costs). In order to keep the data together, tables are fairly rigid - if data were to wrap from one row to another, you'd lose the association between rows and columns and the table wouldn't make sense.

This rigidity is one reason they're not a great tool for page layouts. Tables are automatically sized to fit their content, so they aren't responsive to the size of the page. Additionally, screen readers expect tables to contain tabular data; when they're used for layouts, the screen reader can't interpret the page correctly.

### Creating Tables in HTML

- `<table>` creates a table
- `<tr>` creates a new row
- `<td>` tags are placed inside `<tr>` to create individual cells. The number of cells determines the number of columns in the table; if you don't have the same number of cells in each column, make sure to tweak the formatting or you'll have weird gaps in your table.
- `<th>` denotes a header for a row or column (use in place of `<td>`)

## Intro to Constructors

Object literals are great tools, but the more objects you have, the more work you're going to repeat (and if you make changes, you'll have to update each object individually). Instead, you can create a constructor, then give it the different values for each object and let it create the objects for you. Constructors are functions that are called with the `new` keyword and whose names start with a capital letter.

When used in a constructor, `this` attaches to the object that is created, so the object can later use `this` inside itself.

## Object Prototypes Using a Constructor

Every object in JavaScript has a built-in property called a `prototype`. Prototypes contain properties; if you look for a property that isn't associated with a specific object, the browser looks at the prototype to see if it can be found there (and keeps going up the chain as far as it can). You can also modify an object's prototype so you can reference those properties later.

Using prototypes can be like creating document templates, where many variables are available outside the document, but not all of them will necessarily be used.

## Things I Want to Know More About

I need more practice with prototypes to really understand how they work.
