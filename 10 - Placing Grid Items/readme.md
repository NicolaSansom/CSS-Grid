# Lessons learnt

grid-column is shorthand for two properties:
`grid-column-start` & `grid-column-end`

It is of course an option to define the start and end values in code, so:
`grid-column-start: 2` `grid-column-end: 4` would mean that the item spans 3 tracks(rows) starting on row 2. Like in the last lesson if there is not enough space on the current column it move to the next one and leave blink spaces

shorthand for this is `grid-column: 2  / 4;`

You can combine this with spanning so `grid-column: span 3 / 5` would span three slots in the end grid but end at track 5 and can do the same thing the other way around `grid-column: 2 / span 4`

## Unknown amount of rows

If we have an item we would like to start a specific place and span the whole of the remaning space on that column we can use:
`grid-column: 1 / -1;` // item 100% of a column

Increasing the negative number would end off that many from the last item so `-2` would end one from the end item on the column

### For negatives number to work as expected ensure we have a explicit guide

Negative numbers will only however go to the bottom of the explicit grid not that implicit grid
