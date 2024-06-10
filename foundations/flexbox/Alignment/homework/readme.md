# Interactive guide to flexbox

- https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/

---

## Introduction to flexbox

- CSS is comprised of many different layout algorithms, know officially as "layout modes"
- Each layout mode is its own little sub-language within CSS
- The detaul layout mode is **Flow Layout**, can opt in to Flexbox by changing the `display` property on the parent container

- *Each layout algorithm is designed to solve a specific problem*. The default "flow" layout is meant to create digital documents; essentially the **microsoft word** layout algorithm
    - Headings and paragraps stack vertically as blocks, while text, links, and images sit inconspicously within these blocks
- **What problem does flexbox solve?** Flexbox is all about arranging a group of items in a row or column, and then giving us a ridiculous amount of control over the distribution and alignment of those itme
    - Flexbox is about flexibility
    - We can control whether items grow or shrink, how the extra space is distributed, and more

---

## Flex direction

- Flexbox is about controlling the distribution of elements in a row or column
- By default, items stack side-by-side in a row, but can flip to a column with `flex-direction` property

- With `flex-direction: row`, the primary axis runs horizontally from left to right
- When flipped to `flex-direction: column` the primary axis runs vertically from top to bottom

- **In Flexbox, everything is based on the primary axis.** The algorithm doesn't care about vertical/horizontal or even row/column
- All of the rules are structed around the primary axis and the **cross axis**
- **This is cool.** When learning the rules of flexbox, you can switch seamlessly from horizontal layouts to vertical
- All of the rules adapt automatically
    - Unique feature to the flexbox layout model

- Children will be positioned by default according to the following 2 rules:
1. **Primary axis:** Children will be bunched up at the **start** of the container
2. **Cross axis:** Children will stretch out to fill the entire container

![Imgur](https://i.imgur.com/pIGd0FQ.jpeg)

- In flexbox, must decide whether the primary axis runs horizontally or vertically
- This is the root that all flexbox calculations are pegged to