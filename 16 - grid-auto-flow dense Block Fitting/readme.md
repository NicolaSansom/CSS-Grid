# Lessons learnt

When we put something like `grid-column: span 6;` the browser checks to see if their are 6 slots available on the current line if there is not it will drop onto a new line. This creates gaps in the grid for example if there was only 5 slots available then the item would drop to the next line.

`grid-auto-flow: dense;` fills these gaps with items that will fit into that space instead of leaving empty spaces. In the context of the example 6 would dropdown to a new line but 7, 8, 9, 10 & 11 would be moved up to the top line where as before there would just gaps.

Its worth mentioning that using dense changes the order in which the elements appear visually i.e it does not match the order they have within the dom.
