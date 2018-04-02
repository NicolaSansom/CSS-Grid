# Lessons learnt

[CSS grid cheatsheet](https://css-tricks.com/snippets/css/complete-guide-grid/)

This episode focuses on how to center and align items within a grid. All of the properties are very familiar as they are used within flexbox.

**Justify** on the row axis

**Align** on the column axis

Wes mentioned that he prefers doing simple alignment such as text centering with `display: grid` because of the addition of `justify self` which flex does not offer.

## Items

The default for an item if not defined is `justify-items: stretch` if we changes this to `justify-items: center` the width of items becomes as big as the content is. We can also use `end` & `start` the behavior is similar to how it was in flex.

The same values are also aviable for `align` accept it will be on the column axis. Items would be added onto the class where the grid is defined.

### Column and row shorthand

If wanted to define both values on one line we could use `place-items`. This property is not supported on all browsers however so it worth autoprefixing these with single align and justify properties.

## Content

Justify and align content allows us to position the grid items if they do not fill the whole grid. So for example if the total width of all grid items was 1200px  and the remaining space in the grid was  200px, we could center these items so the whitespace would be even each side, in the prior example 100px left and right if centered. `justify-content: start` is the default.

Space-around & between are also available these have the same behavior has on flex.

The same values are also aviable for `align` accept it will be on the column axis. Items would be added onto the class where the grid is defined.

## Self

The self properties are applied onto the items themselves. These are some useful in instances where one item needs to have a different positioning then the others. The same properties are available as items.
