# Lessons learnt

This was a practical example of using grid to create a codepen like layout. There was not complex use cases here more just nesting grids within each other to quicky create a layout.

For the main three sections(header, code & site header) I did

```css
.codepen {
  display: grid;
  grid-template-rows: auto 1fr 1fr auto;
  height: 100vh;
}
```

The first & last column use the space they need for the content and the remaining space is split between the two middle columns

Get three columns that are all the same width I used:

```css
  display: grid;
  grid-template-columns: repeat(3, 1fr);
```
