## Lessons learnt

The repeat functions take two parems firstly how many times you want to repeat it and what you would like to repeat!

For example
` grid-template-columns:  repeat(4, 1fr)` is the equivalent of  `grid-template-columns:  1fr 1fr 1fr 1fr;`

Whats cool is that you can also pass multiple values as  the second parem

For example
` grid-template-columns:  repeat(4, 1fr 2fr);`  is the equivalent of  `grid-template-columns:  1fr 2fr 1fr 2fr  1fr 2fr  1fr 2fr ;`

It copies the values in the order to write them 4 times resulting in 4 1fr 2fr. Basically taking whatever you have in the second parem and repeating it

You can mixin and match it up with regular values aswell so:
` grid-template-columns: auto  repeat(4, 1fr) 100px;`  is the equivalent of `grid-template-columns: auto 1fr 1fr 1fr 1fr 100px`
