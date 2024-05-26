# Normal flow
- The way webpage elements lay themselves out if you haven't changed their layout

---

- Elements on a webpage lay out in **normal flow** if you haven't applied any CSS to change the way they behave
- You can adjust their position in normal flow by removing them from it altogether
- Think of normal flow of working with the document rather than struggling against it as you make changes to the layout

## How are elements laid out by default?

- The process begins as the boxes of individual elements are laid out in such a way that any padding, border, or margin they happen to have is added to their content
    - This is again, the box model

- By default, a block-level element's content fills the available inline space of the parent element containing it
    - Will grow along with that block dimension to accomodate the content it has
    - Size of of inline-level elements are just the size of the content itself
        - width or height depending on elements that have a default display property of inline 
            - These can be img

- To change the behavior, can use CSS to be block-level
    - display: block
    - display: inline-block
        - This mixes characteristics from both
- Block level elements are laid out vertically


---

- Inline elements want to behave differently
    - Don't appear on new lines 
        - Sit all at the same line along with wrapped text content as long as there is space
    - If two vertically adjacent elements both have a margin set on them and they end up touching, the larger of the 2 elements will remain and the smaller of the 2 will disappear
        - This is margin collapsing