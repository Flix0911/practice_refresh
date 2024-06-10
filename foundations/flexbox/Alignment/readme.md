# Alignment

- Everything so far in flexboz has used the rule `flex: 1` on all flex items, which makes the items grow and shrink equally to fill all the available space
- Frequently, this is not the desired effect. Flex is also very useful for arranging items that hve a specific size

## Alrightment
- See example1

- Add `flex: 1` ~ it evens the growth out
- Makes each of the items grow to fill the available space
    - What if we wanted to them stay the same width, but distribute themselves differently inside the container?

    - Remove `flex: 1` from `item`
    - add `justfiy-content: space-between` to `.container`

- `justify-content` aligns items across the **main axis**
    - Couple of values you can use here but try `center`
- To change the placement of items along the **cross axis**, use `align-items`
    - add `align-items: center` to `.container`

- Because `justify-content` and `align-items` are based on the main and cross axis of your container, the behvaior changes when you change the flex-direction of a flex-container
    - Ex: when you change `flex-direction` to `column`, `justify-content` aligns vertically and `align-items` aligns horizontally
    - Most common behavior it eh default `justify-content` aligns items horizontally (the main axis defaultws to the horizontal)
    - `align-items` aligns them vertically
    - **Confusion to beginners**

---
## Gap

- A useful feature of flex is `gap` property. Setting `gap` on a flex container adds a specified space between flex items ~ similar to adding margin to the items themselves
- `gap` is a *new* property so it doesn't show up in many resources yet, but it works reliable in all modern browsers