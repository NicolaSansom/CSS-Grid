# Lessons learnt

Grid templates allow us to assign names to different area of a grid these typically the areasyou create when you put:
 `grid-template-columns: 1fr 500px 1fr;`

## Define grid areas

 To assign a name to area an of the grid you put:
 `grid-template-areas: "sidebar-1 content sidebar-2";`

 The example corresponds to the areas defined in the previous statement.

 If wanted to define more areas names we could do:

```css
grid-template-areas:
 "sidebar-1 content sidebar-2"
 "sidebar-1 content sidebar-2"
 "footer footer footer";
 ```

To take the statement more readable we have put each row onto a new line. If we did not want to name a area we could just put a `.`

When all are areas names are defined we can go in and start assigning classes to areas of example:
`grid-area: footer;`

**Redefine areas based on screensize**

Often when the available space gets smaller we will want to reconfigure the areas for example we may want the areas to visually stack. In the context of the example we can do this by:

```css
grid-template-areas:
  "content content content"
  "sidebar-1 sidebar-1 sidebar-1"
  "footer footer footer";
```

### Grid area lines

Previously when positioning items within grid areas we did:
`grid-column: 2 / 5;`

When using named grid areas we are able to instead use the line names based off the areas in context of the example this would be:
`grid-column: 🦄-start/ 👻-end;`
