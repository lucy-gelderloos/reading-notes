# Code 201 Class 11 - Video and Audio Content; A Complete Guide to Grid; Responsive Images

## Video & Audio

### 1. Explain how the ability to use video and audio on the web has evolved since the early 2000s

In the early 2000s, there was no ability to embed video or audio in web pages without plugin-based tools like Flash and Silverlight.

### 2. Describe the use of the `src` and `controls` attributes in the `<video>` element

- `src` works the same as in an `<img>` tag - it tells the browser where to get the video file
- `controls` lets viewers use the browser's built-in video controls when watching the video(you can also build a custom control interface).

### 3. Why is it important to have fallback content inside the `<video>` element?

Older browsers may not support the `<video>` element. In that case, the fallback content will load, so you can provide an alternate way to watch the video.

### 4. Write a very short story where `<audio>` and `<video>` are characters

## Grid

### 1. How does Grid layout differ from Flex?

Flex layouts work in either rows *or* columns (one-dimensional). Grid layouts can control rows and columns at the same time (two-dimensional).

### 2. Grid container, grid item, and grid line are a few important terms to understand when using Grid. Please describe these terms in a few sentences

- The **Grid Container** is the *direct* parent element of all the grid items
- A **Grid Item** is a child (the *direct* descendant, not just any descendant) of the container element
- The **Grid Line** is the line dividing various grid items - "column grid lines" between columns and "row grid lines" between rows.

## Responsive Images

### 1. Besides making a site visually appealing across different screen sizes, why should developers make images responsive?

Including responsive images can reduce loading times and bandwidth use by loading smaller images when the user has a smaller screen.

### 2. Define the following `<img>` attributes `srcset` and `sizes`. Write an example of how they are used.

- The `srcset` attribute contains a list of all the available images and their sizes. For example, you could list an image that was 100w wide and one that was 350w (note that this measurement is the real (*intrinsic*) width of the image in pixels and uses the unit "w").
- The `sizes` attribute indicates which image should be used at which screen size. You can set a condition (`max-width: 600px` means "when the viewport width is 600 pixels or less"), and tell the browser to display one image when the condition is true and one when it's false (so we could display our 350w image when the site is wider than 600px, and the 100w image when it's narrower).

### 3. How is `srcset` more helpful for responsive images than CSS or JavaScript?

When a page loads, it starts downloading images before it interprets the page's CSS & JS; this means that it will load one image by default and replace it with the correct image after the page loads, which won't help reduce bandwidth use *at all*. Because `srcset` is part of the HTML document, the browser sees it as soon as the page loads.
