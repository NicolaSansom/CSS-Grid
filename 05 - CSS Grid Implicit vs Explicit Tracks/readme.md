# Lessons learnt

## Explicit  and implicit

Explicit is when you explicitly define what the tracks values will be.

`grid-template-columns:200px 400px;` Is an example of this, columns are explicit but the rows implicit

Implicit is when you do not define values for a track. For example if you considered the prior example, the first column is 200px and the second 400px. If there were 2 more items added, this pattern would repeat, the third item being 200px and the forth item being 400px and so on and so forth, implicit rows  being created every time a row has more than two columns.

`grid-auto-rows/columsn: value`
To control size of implicit tracks you can do:

This will mean any new rows/columns that are implicit will be 300px.

## Firefox dev tools

-Explicit lines are dashed.
-Implicit lines are faded and dashed
-Start and finish of a explicit track is solid
