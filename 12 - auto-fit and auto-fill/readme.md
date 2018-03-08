###  Lessons learnt

## Auto fill
Auto fill figures out how many columns to create based off how much content is in each item and how many can fit within the grid.

This is awesome because has the grid width changes the items drop onto new columns when they are is not enough space, very responsive!

Auto fill is useful if you want one of your items to be placed at the end of the grid for example:
`grid-column: auto / -1` this is not doable when using auto fit

## Auto fit
The difference is between this and auto fill is that auto fit ends the grid based on the number of items where as auto fill carries on adding additional columns to the explicit grid if there is space to do so.
