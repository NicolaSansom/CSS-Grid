## Lessons learnt

You can use other values aside from pxs when defining grids.

# Percentages

`grid-template-columns: 25% 25% 25% 25%;`
`grid-gap: 20px` 

This would be result in there being horizontal scroll because the grid-gap is factored resulting in an overflow of 60px. It is best to avoid using this unit.

# FR - Fractional units

Represent the amount of space left after all elements are laid out, similar to flex-grow.

Here are a few examples:
`grid-template-columns: 200px 200px 1fr` Would result in `1fr` taking up the whole remaining free space
`grid-template-columns: 200px 1fr 1fr` Would result in the free space being split between these two columns
`grid-template-columns: 200px 2fr 1fr` Would result in `2fr` taking up two thirds of the free space and `1fr` taking up one thrid of the remaing space in a grid.
`grid-template-columns: 200px 2fr 1fr 1fr`Would result `2fr` taking up 50% of the free space, and the remaining two `1frs` taking up 25% of the free space.

# Row height
Like in flex box the height by default is determined by the height of the content. Default is as wide as the wrapper/ viewport. 

If you were to give the grid a height of 600px and then add `grid-template-rows: 1fr 10fr 1fr 1fr` , the third row  would be ten times as big as the other rows, so in context of the example  `385.5 px`,  the other three rows would have a height of `51.5px ` - all together adding up to 540px plus the 20px grid gap times by three which works out to at 600px, FR takes into account the grid-gap where as percentages does not.

# Difference between using FR units and auto

Auto stretches to the content width, all of the columns resizing to the upmost of width for example, instead of each column being a different width depending on content. See the result of of

`grid-template-columns: auto 1fr auto 1fr;` 

The first column is small because the 13 is determined the width where as the third column is larger because 'Wes Bos is Cool is determined the width "

To see this in action check out the completed file
