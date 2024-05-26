# Block and inline

- CSS has two box types *block* and *inline* ~ these determine the element behavior and interaction
- the *display* property controls how HTML elements appear on the webpage

## Block vs Inline

- Most of the elements learned so far are block elements
    - Their defalt style is '*display: block*'
    - By default, block elements will appear on the page staked atop each other 
        - Each new element starts on a new line

- Inline elements, do not start on a new line
    - Inline appear in line with whatever elements they are placed beside
    - Good example of an inline element is a <"a"> tag. If you add this in the middle of a paragraph or text, the line will behave like a part of the paragraph
    - Additionally, padding and margin behave differently on inline elements
        - Don't typically want to try to put extra padding or margin on inline elements

### The middle ground inline block

- Inline-block elements behave like inline elements, but with block-style padding and margin
- *display: inline-block* is a useful tool to know about, but in practice, you'll probably end up reaching for flexbox

## Divs and spans

- Keep in mind, all HTML elements discussed so far bring meaning to their content
- Divs and spans give no particular meaning to their content. They are just generic boxes that can contain anything
- This is important because we often need elements that serve no other purpose other than being a "hook" type of element

- Div is a block-level element by default
    - Commonly used as a container element to group other elements
    - Divs allow the ability to divide the page into different blocks and apply styling to said blocks


- Span is an inline-level element by default. It can be used to group text content and inline HTML elements for styling and should ony be used when no other semantic HTML element is appropriate


---

# Block level elements in HTML

![Imgur](https://i.imgur.com/f18wnHI.jpg)

---

# Inline elements

![Imgur](https://i.imgur.com/M36BqYZ.jpg)