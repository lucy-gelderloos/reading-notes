# Class 9 Reading Notes - HTML Forms, JavaScript Events

## HTML Forms

### 1. Why are forms so important in web development?

Forms allow users to interact with websites by sending data (for instance, adding items to a shopping cart or signing up for a mailing list).

### 2. When designing a form, what are some key things to keep in mind when it comes to user experience?

THe more data your form asks for, the less usable it will be, keep the information you're asking for limited. Also make sure to label your fields clearly and arrange the form so the most important areas are the most eye-catching.

### 3. List 5 form elements and explain their importance

1. The `<form>` element contains the rest of the form. Along with defining that area of the page, it allows for some special behavior.
1. The `<label>` element is associated with a form control. It allows users with pointing devices to focus on the associated control, and provides an identifier on the control for people using screen readers.
1. The `<input>` element defines an area where users can input data; types of inputs can include text, numbers, or email addresses.
1. The `<textarea>` element is like an input in that it can be used to enter data, but unlike a text input field, the text area allows multiple lines of text.
1. The `<button>` element defines a button that the user can click, often to submit a form.

## JavaScript Events

### 1. How would you describe events to a non-technical friend?

Events are actions the system takes in response to specific triggers or actions, like clicking a button or pausing a video.

### 2. When using the `addEventListener()` method, what 2 arguments will you need to provide?

You'll need to provide the name of the action that should cause the event listener to react (like `click` or `mouseover`) and the function you want to run when that action happens.

### 3. Describe the event object. Why is the target within the event object useful?

Event objects pass the event as a parameter to the associated function, which allows the function to act on the element the event occurred on.

### 4. What is the difference between event bubbling and event capturing?

Event bubbling means that if multiple nested elements have the same kind of event handler (a click, for example), the most deeply-nexted item will fire first. Modern browsers are set to "bubble" by default. Event capturing means that when an item is clicked, the browser looks for and runs handlers from the outside in until it reaches the parent of the element that fired off the original event.

## Things I want to know more about

Is it possible to tell a browser to capture instead of bubble, and what would be some advantages of doing that?
