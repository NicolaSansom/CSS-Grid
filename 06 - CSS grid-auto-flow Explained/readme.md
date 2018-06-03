# Lessons learnt

`grid-auto-flow` will determine if to implicitly  create new rows or place the item on the same row.

## Rows - `grid-auto-flow: row;`

This will create new rows when the explicit declaration needs to be repeated, for example if there were three items in a div with `display: grid;` on it and  `grid-template-columns: 400px 200px;`. Using `grid-auto-flow: rows;` would main the third item would be a 200px column a new row.

## Columns - `grid-auto-flow: column;`

`grid-auto-flow: columns;` Would instead create a new row, add the third item to the same row(an additional 400px column). These will not wrap onto a row and instead will cause horizontal scroll.

To stop the explicit columns from repeating the pattern you could put:
`grid-auto-columns: 200px;`, this would be the third item would be 200px instead of 400px

Not a common use case.
