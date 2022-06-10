# Code 201 Class 5 - HTML Images, CSS Color & Text

## HTML Images

1. **What is a real world use case for the `alt` attribute being used in a website?** The `alt` attribute provides a text description for an image. If images don't load, the alt text can let visitors know what the image is; it can also help search engines understand your page. Screen readers also use the alt text to describe the image to people who are visually impaired.
2. **How can you improve accessibility of images in an HTML document?**
    - Use CSS for background or other decorative images so they don't clutter up the HTML. If you do put a purely decorative image in the HTML, use `alt=''` so screen readers know to ignore it.
    - Don't put your text in images. If you use an image to convey information, it's best to also have that information in text in your page.
3. **Provide an example of when the `figure` element would be useful in an HTML document.** If you want to caption your images, you can the `figure` and `figcaption` elements to make sure browsers, screen readers, etc. know exactly which caption goes with wihch image. For instance, if you're writing a step-by-step tutorial with images, not using `figure` and `figcaption` could mean that your captions appear next to the wrong images.
4. **Describe the difference between a `gif` image and an `svg` image, pretend you are explaining to an elder in your community.** GIF images work best for simple images and animations (like pictures posted to social media, where it can be important to have small file sizes). SVG images work best for images that need to be displayed clearly at all sizes, like diagrams and icons.
5. **What image type would you use to display a screenshot on your website and why?** I would use a PNG because it provides the clearest image. Screenshots usually include a lot of information and need to be readable.

## CSS Color & Text

1. **Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.** The foreground color (usually referred to as just "color") determines the color of the content, like text and borders. The background color sets the background color of the element and will appear behind all of the content.
2. **Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?** I would probably start with colors for headings, links, and areas my friend wants to highlight. I might add a background color for the whole page, but would probably start with a pretty subtle one so it doesn't overwhelm the rest of the content.
3. **What should you consider when choosing fonts for an HTML document?** The first consideration is whether the font you want to use is available to the user, based on their browser and the computer they're using to access the site. There are a small number of "web safe" fonts, which are available in almost every operating system. (This list changes over time, but slowly.) Readability is another concern, although the web safe fonts are generally quite readable. Stay away from novelty fonts.
4. **What do `font-size`, `font-weight`, and `font-style` do to HTML text elements?**
    - `font-size` sets the size of the font. It can either be an absolute value expressed in pixels (`px`), or relative to the font size of either the parent element (`em`) or the root element (`rem`). For instance, a font size of `0.5em` would be half the size of the font of the parent element.
    - `font-weight` sets the weight of the font (usually to or from **bold**). It can be absolute or relative to the parent element.
    - `font-style` sets the font to *italic* (or sets it back to normal from italic). If the font doesn't have an italic option, it can be simulated by slanting the font's regular characters (`oblique`).
5. **Describe two ways you could add spacing around the characters displayed in an `h1`.**
    - `letter-spacing` and `word-spacing` set the space between letters and words, respectively
    - `line-height` can add space above and below the heading

## Tips

- **Make sure you have permission to use the images on your site, and do not link to images hosted on other sites that you don't have permission to link to.**

## Best Practices

- Using absolute URLs for images makes the browser do more work every time the page loads

## Things I Want to Know More About

I'd love to get into more detail on the pros and cons of using different image formats.
