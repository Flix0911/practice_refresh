# The Box Model

- A very important skill in CSS ~ positioning and layout

## Lesson overview

- Box model
- Margin
- Padding
- Borders

### The box model

- Everything on a webpage is a rectangular box. These boxes have other boxes in them and can sit alongside one another

- Apply to every element on the page
```css
* {
    outline: 2px solid red;
}
```

- Laying out a webpage and positioning all its elements is deciding how you are going to nest and stack these boxes

- What gets complicated is there are many ways to manipulate the size of these boxes, and the spacing between them, i.e., padding, border, and margin

---
- Padding: Increases the space between the broder of a box and the content of the box
- Border: Adds space (even if it's only a pixel or two) between the margin and the padding
- Margin: increase the space between the borders of a box and the borders of adjacent boxes

![Imgur](https://i.imgur.com/Hu79LNR.jpg)