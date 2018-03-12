# Lessons learnt

## Minmax `minmax(min, max)`

Minmax is responsive be nature and useful to replace media queries.
It takes two parems, quilt simply the minimum and maximum width each column can be.

When the container when there is no enough space to allow each column to be the  minimum width they will stack on top of each and span the width of the container.

Auto fit stretch's the span and the container and aut-fill create an implicit grid after the explicit grid

### Fit content `fit-content(100px)`

Fit content take one param the maximum width the item can be it will, Wes said this not often used but could come in handy in edge cases.
