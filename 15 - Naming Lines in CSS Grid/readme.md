# Lessons learnt

## Naming lines

It is possible to name lines within a grid, lines are not the columns/row themselves they go in between the rows/columns.

### Defining the names

Without names

```css
grid-template-columns: 1fr 500px 1fr;
grid-template-rows: repeat(10, auto);
```

With names

```css
grid-template-columns: [site-left] 1fr [content-start] 500px [content-end] 1fr [side-right];
grid-template-row: [content-top] repeat(10, auto) [content-bottom];
```

It is useful to do this when you plan on changing placements at later stage.

### Using the names

```css
grid-column: 2;
grid-column: content-start;

grid-row: 1 / 10;
grid-row: content-top / content-bottom;
```

You can assign multiple names to one lines.
