# Growing and Shrinking

## The flex shorthand

- The **flex** declaration is actually a shorthand for 3 properties that you can set on a flex item
- These properties affect how flex items size themselves within their container

---

##### Shorthand properties

    - CSS properties that let you set the values of multiple other CSS properties simultaneously
    - You can write more concise and more readable stylesheets

---

- **Flex** is actually a shorthand for flex-grow, flex-shrink, and flex-basis

```css
div {
    flex: 1;
}
```

- In the above, `flex: 1` equates to `flex-grow: 1`, `flex-shrink: 1`, and `flex-basis: 0`
    - Norm is to see the flex shorthand defined with only 1 value
    - Value is applied to `flex-grow`
    - When we put `flex: 1` on our divs, we are actually specifiying a shorthand of `flex: 1 1 0`

### Flex-grow

- `Flex-grow` expect a single number as its value, and that number is used as the flex-item's "growth factor"
- As we applied `flex: 1` to every div inside the container, we're telling every div to grow the same amount
- The result will be that every div ends up the same exact size
- If using `flex: 2` to just 1 of the divs, then that div would grow 2x the size of others

** see index.html and styles.css

### Flex-shrink

- `flex-shrink` is similar to `flex-grow`, but sets the "shrink factor" of a flex item
-`flex-shrink` only ends up being applied if the size of all flex items is larger than their parent container
    - Ex. if the 3 divs from the previously example had a width declaration like: `width: 100px`, and `.flex-conainer` was smaller than `300px`, our divs would have to shrink to fix
    - See image below

![Imgur](https://i.imgur.com/WhIjJx2.jpeg)

- The default shrink factor is `flex-shrink: 1`, which means all items will shrink evently
- If you don't want that to occur, you need `flex-shrink: 0`

- see index2.html and styles2.css for reference
- If you shrink the browser window, notice how `.two` never gets smaller than the given width of 250px ~ even though the `flex-grow` rule would otherwise specify that each element should be equally sized

- Fun fact: an important implication to notice is that when you specific `flex-grow` or `flex-shrink`, flex items do not necessarily respect your given values for `width`
- In the index2.html example, all 3 divs are given a width of 250px, but when their parent is big enough, they grow to fill it
    - Same when the parent is too small, the default behavior is for them to shrink to fit

### Flex-basis

- `flex-basis` sets the initial size of a flex item, so any sort of `flex-grow`ing or `flex-shrink`ing start from the baseline size
- Shorthand edfault to `flex-basis: 0%`
    - Reason we changed to auto in the `flex-shrink` ex is that with the basis set to 0, the items would ignore the item's width, and would shrink evenly
    - `auto` as a flex basis tell the item to check a width declaration (`width: 250px`)

- Important note about flex-basis:

    - There is a difference between the default value of flex-basis and the way the flex shorthand defines it if no flex-basis is given. The actual default value for flex-basis is auto, but when you specify flex: 1 on an element, it interprets that as flex: 1 1 0. If you want to only adjust an item’s flex-grow you can do so directly, without the shorthand. Or you can be more verbose and use the full 3 value shorthand flex: 1 1 auto, which is also equivalent to using flex: auto.

- What is flex: auto?

    - If you noticed, we mentioned a new flex shorthand flex: auto in the previous note. However we didn’t fully introduce it. flex: auto is one of the shorthands of flex. When auto is defined as a flex keyword it is equivalent to the values of flex-grow: 1, flex-shrink: 1 and flex-basis: auto or to flex: 1 1 auto using the flex shorthand. Note that flex: auto is not the default value when using the flex shorthand despite the name being “auto” which may be slightly confusing at first. You will encounter and learn more about flex: auto and its potential use-cases when reading through the assignment section.