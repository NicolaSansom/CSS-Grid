###  Lessons learnt

## Sizing items within a grid

If you add width to an item within a grid the whole of that column will how the same width.

Of course this not always desired sometimes we want just a items to have a different width not the while column to do this instead of using fixed widths on items we can use:


## Spanning 
`grid-column: span 2;`
This covers multiple slots within the grid

In the video we added: `grid-column: span 3;` onto item 9 of a 5 row grid, this causes the item to go onto the next column and leave a blink space, this happens because it displays the item in one column but on the second column there was only space to cover 2 slots so it moves onto the next column.  You can get similar effect if you wanted a item to span multiple rows by doing `grid-row: span 2`

If we were to span more then the columns we had it would create new ones these additional columns would be implicit
