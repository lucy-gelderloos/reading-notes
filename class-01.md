# Code 201 Class 1 - Intro to HTML and JavaScript

## Basics of the Web

Websites are hosted on dedicated servers. People use web browsers to access the site. Websites are structured with HTML, styled with CSS, and activated with JavaScript.

HTML and CSS are updated as needs and technology change; the current versions are HTML5 and CSS3. The HTML version should be included in a `<DOCTYPE>` declaration at the very beginning of the HTML document.

Websites are fundamentally documents, similar to existing hardcopy documents (i.e., a newspaper). Documents of all kinds can be structured using various **elements**, like headings, to make them easier to use.

## HTML Elements

HTML elements are defined by opening and closing tags contained in angled brackets (`<`, `>`). The tags tell the browser how to display various parts of the page. Almost all elements require both opening and closing tags.

The foundational elements of a page are the `<head>`, `<title>`, and `<body>`.

- The `<head>` element contains information *about* the site, and visitors won't see it unless they look at the source code of the page. You can use the `<meta>` tag to add further information, like the page's author, a description, and instructions for browsers and search engines.
- The `<title>` element gives a title to the page, which will display at the top of the browser or tab.
- The `<body>` element contains the content of the page, and is what visitors to the site will see.

## HTML Attributes

Elements can be modified with attributes, which appear in the opening tag. The attribute name is lower-case, and the attribute value is in double quotes:

`<element attribute="attribute-value">`

Two of the most commonly-used attributes are `id`, which applies a unique identifier to the element, and `class`, which denotes that the element belongs to a group of elements. Multiple attributes, and in some cases multiple instances of an attribute, can be applied to an element: `<p id="id1" class="class1 class2">`. `id` and `class` are both global attributes, so they can be applied to any element.

These attributes can also be used with JavaScript to apply code to specific elements.

## Displaying and Grouping Elements

Block elements always start on a new line (like headings and paragraphs). Inline elements start in the same line (like `<b>` to make individual words **bold**).

Elements can also be grouped inside other elements. For block elements, use `<div>`, and for inline elements, use `<span>`. These elements can be styled with CSS, allowing you to style groups of elements all at once.

HTML5 includes a number of layout elements that both allow you to fine-tune your layout and allow browsers and screen readers to understand how to prioritize content. For instance, instead of using a `<div>` tag with `id="article`, you can use an `<article>` tag. HTML5 layout elements include:

- `<header>` & `<footer>` can be used for your site or for elements like `<article>`
- `<nav>` contains the major sitewide navigation links
- `<article>` contains content that stands alone
- `<aside>` is used either in articles (for pull quotes or other related information) or on the main site (for repeating information like lists of recent posts)
- `<section>` groups various parts of a page, like multiple articles on a particular topic
- `<hgroup>` is a controversial tag that groups headings together - for instance, to keep a heading and subheading together
- `<figure>` contains content, like images, that is referenced from an article (make sure to include a `<figcaption>` as well)
- `<div>` can be used in any situation not appropriate for another layout element

An iframe can be used to embed another site (like a Google map) into your site.

## Using JavaScript in Your Site

JavaScript can make your page interactive. It can change what content displays, allow users to enter information into a form, or update parts of the page depending on user input.

### What is a Script?

Scripts are a series of instructions a computer uses to generate a desired result - like a recipe or manual. To write a script, first define your goal. Then determine what steps you'll need to get to that goal, and finally write those steps into the code. Many programmers use flowcharts to visualize the steps of the script.

Because computers work very literally, each step of the script needs to be spelled out in a language the computer can understand. Those languages have vocabulary and syntax.

### How do Computers See the World?

Computers create "models" of the world based on data provided to them.

These models start with "objects," each representing an item in the real world. Appearances of an object are called "instances."

Every object has characteristics, or "properties." Each property has a name (like "color") and a value ("blue").

When people interact with an object and change one of the properties, it is called an "event." Programmers can tell the computer how to respond to a particular event.

A "method" represents how people interact with an object. Methods may contain lots of code that you can call without needing to understand how it does what it does.

Events, methods, and properties can all interact with each other.

Web browsers create models of the pages they're displaying - the "window" object represents the window of the browser that is displaying the page, and the "document" object is the page loaded in that window. The document object will have associated properties, events, and methods.

When browsers access a web page, they receive the HTML code for the page, create a model of the page, and use a rendering engine to show the page on screen. All major browsers can understand and use JavaScript to show the page.

### How do HTML, CSS, & JavaScript Fit Together?

HTML, CSS, and JavaScript are the three main languages used to create web pages. The HTML layer is the most foundational - it includes the content and basic structure of the page. The HTML layer is also the most accessible, since it can be read by all kinds of browsers and devices and will load faster. The next layer is CSS, which adds color and style to the site. Finally, the JavaScript enhances the page.

The HTML, CSS, and JavaScript should all be in separate files. That way, if a browser can't load all the features, it's easy to separate out the ones that can be loaded. It also means you can edit your CSS or JavaScript without having to make the change on every page.

Pages load from the top down, and initiate JavaScript code based on where it is found on the page.

## Creating a New Site

When designing a new site, there's a lot to do before you sit down and start coding. You'll want to know who will be visiting the site, how, and what they want to get from it. Think abou their motivations (reasons for visiting the site) and goals (reasons for visiting the site *now*), as well as what they might already know (what you sell) and what you want to tell them (big sale today!). The information they're looking for will also determine how often you update your site.

It can be helpful to create a group of fictional visitors, and thinking through the whole process, from why they would want to come to the site, to how they find and navigate it, to what they do while they're there.

Once you've figured out who the site is for, try building a site map showing which pages will go where. It can be helpful to write the name of each page on a notecard and physically arrange the pages.

The next step is a wireframe - a simple sketch of each page showing what information goes where. The wireframe doesn't have actual content in it and does not have any styling.

Next, think about how styling can help communicate your point, by grouping and prioritizing content. Using size and color can help visitors find what they need without having to read every word on the site. Knowing how people prioritize visual information can help make the site more useful.

Unless all your content is on one page, usable site navigation is crucial. Navigation areas should be clearly delineated and easy to read. They should have clear options and should indicate which page the visitor is on.

The main site navigation should be the same across all pages; secondary and tertiary navigation can change per page but should be as consistent as possible.

## Tips

- Web browsers can show the source code of a site.
- Add comments to HTML like so: `<!--comment text-->`. These comments will be invisible to people who view the site in a browser, but anyone who views the source code will see them.
- Because some characters, like `<`, are used in HTML code, you'll need to "escape" those characters if you want them to appear in the text without being read as code by the browser.
- When writing a script, use a flowchart to visualize the steps

## Best Practices

- Make sure your site is accessible for screen readers
- HTML5 can be flexible on things like nesting and closing tags, but for consistency, make sure to nest tags correctly and use closing tags for elements that use them
- Your site should be compatible with older browsers that may not use the most recent versions of HTML, CSS, etc.
- Don't use HTML5 layout tags (`<section>`, `<nav>`, etc.) for anything other than their explicit purpose
- Keep your HTML, CSS, and JavaScript in separate files for both development and accessibility reasons

## Things I want to know more about

Block vs. inline display - I need to practice with this to get a better sense of how it works.
