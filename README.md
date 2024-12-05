# Uncommon HTML Bug: Incorrect innerHTML Usage

This repository demonstrates a subtle but potentially problematic bug in HTML involving the use of `innerHTML` to insert a complete HTML element.  The bug shows how directly inserting an entire `<p>` tag using `innerHTML` can lead to unexpected styling and accessibility issues. This is because the browser interprets the inserted HTML as plain text rather than a properly structured element.

## Bug Description
The bug lies in using `innerHTML` to replace the content of a div with a complete `<p>` tag. The browser treats the inserted `<p>` tag as simple text, which might not render as a paragraph visually and can break accessibility features such as screen readers.

## Solution
The solution avoids directly setting the `innerHTML` to a full HTML element. Instead, it uses `createElement` to create the `<p>` element and then `appendChild` to correctly insert it into the DOM.