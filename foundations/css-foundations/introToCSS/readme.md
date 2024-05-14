# Intro to CSS

### Basic syntax

- CSS is made up of various rules
- Made up of a selector, a semicolon-separated list of clecarations, with each of those declarations being made up of a property-value pair

```css
div.bold-text(selector) {
    font-weight(property): 700(value);
}
```

#### Selectors
- Refers to the HTML element to which CSS rules apply. What is being selected

- Unniversal *
```css
*{
    color: purple;
}
```

- Type selector (div will target the div)
```css
div {
    color: white;
}
```

- class selector
```html
<div class="alert-text">blah blah blah</div>
```
```css
.alert-text {
    color: red;
}
```

- Another thing you can do with class attribute is to add multiple classes to a single element, i.e. class="alert-text severe-alert"

- ID Selectors - similar to class. Search an element with the given id
```html
<div id="title">Title</div>
```
```css
#title {
    background-color: red;
}
```

- chaing selectors: chain as a list without an separation
```html
<div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection preview" id="preview">This is preview text</p>
</div>
```
- 2 elemtns with the subsection class that have some sort of unique styles. What is we only want to apply a separate rule to the element that also has header as a 2nd class
```css
.subsection.header {
    color: red;
}
```
- What the subsection.header does is it selects any element that has both the 'subsection' and 'header'
- Combine them
```css
.subsection.header {
    color: red;
}

.subsection#preview {
    color: blue;
}
```
- You can't chain more than one type of selector since an element can't be two different types at once

- -------
##### Descendant combinator
 - Allow us to combine multiple selectors differently than either grouping or chaing them
 - 4 types of combinators but lets look at descendant combinator ~ represented in css by a single space between selectors

    - .ancestor .child would select ane lement with the class child if it has an ancestor with the class ancestor
    - child will only be selected if it is nested inside ancestor

```html
<div class="ancestor">
    <!-- A -->
    <div class="contents">
        <!-- B -->
        <div class="contents"><!-- C --></div>
    </div>
</div>

<div class="contents"><!-- D --></div>
```
```css
.ancestor .contents {
    /* some declarations */
}
```
- In that example, the first two elements with the contents class (B and C) would be selected, but the last element (D) wouldn't be


### Properties to get started with

- Color and background-color: ~ color property sets an element's text color, while background-color sets the background


(below works)
```css
p {
    /* hex */
    color: #1100ff;
}

p {
    /* rgb */
    color: rgb(100, 0, 127);
}

p {
    /* hsl */
    color: hsl(15, 82%, 56%);
}
```

- --

- Typography basics and text-align

    - font-family can be a single value or a comma-separated list of values that determine what font an element uses ~ times new roman, serif. If browser doesn't support the style, it'll default to the next in the list
    - font-size ~ set the size of the font
    - font-weight ~ affects the boldness of text
    - text-align ~ will align text horizontally within an element

- Image and height and width

    - images aren't the only elements that we can adjust the height and width on, but we want to focuson them specifically in this case

        - Default, an <img> element's height and width values will be the same as the actual image file's height and width
        - Would use auto for the height property and adjust the width

---

- Add CSS to HTML

- To attach separate css to html, in <head> <link> </head>

- Internal or embedded css - adds css in the html file, still in the <head></head>

- inline: add styles directly to the element