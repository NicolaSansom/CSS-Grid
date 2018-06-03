# Lessons learnt

Display grid could be applied to a element, which is then split into sections(rows & columns) varying in size.  Items are then placed within the different sections of the grid. Items can span over multiple sections if needed.

The same concept as flexbox is used when applying `display: grid` to a parent all of the children become grid items

After applying grid the next step is split the items up into sections there are varying ways this can be done.


## Explicitly stating how big you want each of the sections of grid to be

`grid-template-columns: 100px 100px 100px;` Takes the direct children of the parent(grid items) and puts them within three columns each a 100px wide , automatically creating a new row for additional elements once again with three columns each a 100px.

Each single item takes up a column. If there is a odd number it will drop onto a new row. The number of columns and the size of each can vary for example you could do `grid-template-columns: 50px 400px 300px 200px;` this would create four columns the first being 50px wide, second 400px wide and so forth. This would repeat again onto a new row if there were more then four items, so the 5th element would be 50px wide, the 6th 400px.

The same concepts described prior can also be applied to rows using `grid-template-rows: ;`

You can pass in different units to these attributes such vh and rem.

You can use both `grid-template-columns` and `grid-template-rows` simultaneously.

## Auto
Using auto to define one of the tracks will span out into the remaining space calculated on the size of the other columns and width of the wrapper itself. A use case for this could be a fixed sidebar of 200px and the remainer space being the main section `grid-template-columns: 200px auto;

## Spacing
`grid-gap` Simply adds spacing between tracks(columns and rows), kind of like adding margins, it however is smarter and only adds it when it is needed, so there is no need to use last and child to cancel spacing on the column or last row!

## Repeat function 
`grid-template-columns: repeat(5, 100px);` You pass the number of times the value need to be repeated and the value itself, this example would create 5 columns each 100px and be the same as writing `grid-template-columns: repeat(100px, 100px, 100px, 100px, 100px);`
