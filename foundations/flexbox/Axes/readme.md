# Axes
- How the orientation of items within a flex container can be controlled using the `flex-direction` property

## Part 1

- One thing that causes confusion in flexbox is that it can work either horizontally or vertically
    - This can cause rule changes depending on which direction you are working with
- **Default direction for a flex tonainer is horizontal, or `row`**
    - However, you can change the direction to vertail, or `column` see ex

```css
.flex-container {
    flex-direction: column;
}
```

- No matter which direction you currently use, you need to think of your flex-containers as having 2 axes:
    - The main axis and the cross axis
    - It is the direction of these axes that change when the `flex-direction` is changed
- In *most* cicrumstances, `flex-direction: row` puts the main axis horizontal (left to right), and `column` put the main axis vertical (top to bottom)

---

- See Folder example1
- We will put `display: flex` on a div and it arranged its children horizontally
- This is a demonstration of `flex-direction: row`, which is the default setting
- uncommenting the line will stack vertically

- `flex-direction: column;` would not work as expected if we used the shorthand `flex: 1`
    - The divs will collapse, even though they clearly have a `height` defined

- This is occuring because flex shorthand expands `flex-basis` to `0`. This means all `flex-grow`ing and `flex-shrink`ing would begin their calculations from `0`
    - Empty divs by default have 0 height, so the flex items to fill up the height of their container means they need nothing
    - Example above fixed by adding `flex: 1 1 auto`, telling the flex items to default to their given `height`
    - Could also do this by putting a height on the parent element, `.flex-container` or by using `flex-grow: 1`

---