# The box model

- Everything in CSS has a box around it
    - It is critical to understand this for aligning items

# Block and inline boxes

- In CSS we have several types of boxes that fit into the categories of *block boxes* and *inline boxes*
- The type refers to how the box behaves in terms of page flow and also in relation to other boxes on the page
- Boxes have an *inner display type* and a *outer display type*
- Can set various values by using display property

# Outer display type

- If a box has an outer display type of **block**, then:
    - Box will break onto a new line
    The *width* and *height* properties are respected
    - Padding, margin, and border will cause other elements to be pushed away from the box
    - If *width* is not specified, the box will extend in the inline direction to fill the space available in its container
    - Most cases, the box will become as wide as its container, filling up 100% of space available

- Fun fact: some HTML elements like h1, h2, use *block* as their outer display type by default

---
- If a box has an out display type of **inline**, then:

    - The box will not break onto a new line
    - the *width* and *height* properties will not apply
    - Top and bottom padding, margins, and borders will apply but will not cause other inline boxes to move away from the box
    - Left and right padding, margins, and borders will apply and will cause other inline boxes to move away from the box

- Fun fact: some HTML elements like a, span, em, and strong, use *inline* as their outer display type by default

---

# Inner Display type

- Boxes also have an *inner* display type ~ dictares how elements inside the box are laid out

- Block and inline layout is the default way for things to behave on the web
- By default and without any other instruction, elemetns inside a box are also laid out in a normal flow
- You can change this via *display: flex;* ~ the element will still use the outer display type of *block* but this changes the inner display type to flex
    - Will learn more about flexbox later
