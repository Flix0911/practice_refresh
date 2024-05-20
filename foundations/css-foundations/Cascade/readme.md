# Introduction

- Combine our knowledge of selectors with the C of CSS ~ the cascade

## Goal

- What does cascade do
- Specificity and combining CSS selectors
- Inheritance affects certain properties

## The cascade of CSS

- Sometimes rules conflict with one another, and we end up with unexpected results
- Default styles that are provided by a browser

-- Cascade is what determines which rules actually get applied to our HTML. There are different factors that the cascade sues to determine this

### Specificity

- A CSS declaration is is more specific will take precedence over less specific ones
    - Inline styles, have the highest specificity compared to selectors
        - Each type of selector has its own specificity level that contributes to how specific a declaration is
    1. ID Selectors
    2. Class Selectors
    3. Type Selectors
- Specificity will only be taken into account when an element has multiple, conflicting declarations tatget it. 
    - Think of a tie breaker
- An ID selector will always beat any number of class selectors
- A class selector will always beat any number of type selectors
- A type selector will always beat any number of less specific selectors
- ID selector > Class Selector > Type Selector

```html
<div class="main">
    <div class="list subsection">Red Text</div>
</div>
```

```css
/* rule 1 */
.subsection {
    color: blue;
}

/* rule 2 */
.main .list {
    color: red;
}
```

- The above ~ rule 2 is more specific so the color: red declaration will take precedence

---

- Try a different one

```html
<div class="main">
    <div class="list" id="subsection">Blue Text</div>
</div>
```

```css
/* rule 1 */
#subsection {
    color: blue;
}

/* rule 2 */
.main .list {
    color: red;
}
```

- The above ~ despite rule 2 having more class selectors than ID selectors, rule 1 is more specific because ID beats class. ID > Class. Blue will take effect

---

```html
<div class="main">
    <div class="list" id="subsection">Red text on yellow background</div>
</div>
```

```css
/* rule 1 */
#subsection {
    background-color: yellow;
    color: blue;
}

/* rule 2 */
.main #subsection {
    color: red;
}
```

- In this example, the first rule uses and ID selector, which the 2nd uses an ID and Class selector. Therefore, neither rule is using a more specific selector than the other
- *CASCADE* then checks the number of each selector type. Both rules have only 1 ID, but rule 2 has a class selector in addition to the ID selector. Rule 2 has higher specificity

Fun fact
---
- Not everything adds specificity
    - Universal selector (*) as well as combinators (+, ~, >, and an empty space). They do not add more specificity

```css
/* rule 1 */
.class.second-class {
    font size: 12px;
}

/* rule 2 */
.class .second-class {
    font-size: 24px;
}
```
- Above rule 1 and 2 have the same specificity
- Rule 1 uses a chaning selctor (no space)
- Rule 2 uses a descendant combinator (the empty space)
- Both rules have two classes and the combinator symbol does not add to specificity

```css
/* rule 1 */
.class.second-class {
    font-size: 12px;
}

/* rule 2 */
.class > .second-class {
    font-size: 24px
}
```

- Above is the same thing
- Even though rule 2 is using a child combinator (>), this does not change the specificity value
- Both rules have two classes so they have the same specificity values


```css
/* rule 1 */
* {
    color: black;
}

/* rule 2 */
h1 {
    color: orange;
}
```

- Above, rule 2 would have a higher specificty and the orange value would take precedence
- Rule 2 uses a type selector, the lowest specificity value.
- However, rule 1 uses the universal selector (*) which has no specificity value
---

### Inhertance



