# What is Markdown?

Markdown is a way of telling computers how to display (or "render") text, images, and other elements of a page. It was designed to be readable by humans even when it's not rendered, so it's a lot simpler than HTML (that also means it has fewer features, although some markdown applications include the ability to use HTML).

Markdown can be used to format everything from a single letter to entire paragraphs, and can place many of the elements of a standard webpage, including headings, links, and images. 

## How does it work?

Markdown uses special characters such as `#`, `*`, or `()` to indicate how text should be formatted. For instance, a line of text with a single `#` in front of it will be formatted as a first-level heading; `##` indicates a second-level heading, and so on. Text can be enclosed in special characters to add bold or italic formatting.

## Formatting Text

To italicize text, enclose it in a single `*` or `_`; to make it bold, enclose it in `**` or `__`. To do both, you can use any combination of those tags.

To format text as code, as in the below examples, enclose the text in backticks (\`).

### Text Formatting Examples

- *italic*: `*italic*` or `_italic_`
- **bold**: `**bold**` or `__bold__`
- ***bold and italic***: `***bold and italic***`, `__*bold and italic*__`, `**_bold and italic_**`, etc.

### Escaping Characters

Because markdown uses characters like `*` to indicate how pages should be formatted, if you want to include those characters in your text, you'll need to use a backslash (\\) to indicate that the character should be displayed as-is (this is called "escaping" characters).

## Organizing Your Page

Markdown can also be used to create up to six levels of headings, which guide human and electronic readers through your page. You can use it to place and size images, arrange concepts into lists, and add internal and external links. 

To create headings, start the line with up to six `#` characters (one for a level 1 heading, two for a level 2 heading, etc.). Put a space after the last `#`, then start your heading.

Images are inserted by starting a line with `!`, then adding the alt text in \[\] and the image url in \(\). 

Markdown can create two different types of lists:
1. unordered lists (like the text formatting examples above)
2. ordered lists (like this one!)

Create an unordered list by starting each line with a `-`, `*`, or `+` followed by a space. Create an ordered list by starting each line with a number followed by a period and a space (it can be any number, as long as the first number of the list is 1). To create a nested list, use spaces or tabs to indent lines.

Finally, you can use markdown to easily insert links. The text to be displayed should go in \[\], and the address of the link goes in \(\). Because links can get long and complicated and markdown was designed to be easy to read, you can also use reference links, which function much like footnotes or endnotes.

## Best Practices and Troubleshooting

If your markdown isn't behaving how you expect, make sure:

- you have blank lines between every element of the page
- you have spaces after the `#`s in your headings
- you've closed all your tags
- all your special characters are escaped
