# Lessons learnt

In this lesson we compare flexbox and grid and how to do things in grid that would would normally do in flexbox, when to use one of the other and how to use them both together.

## Advantages of flexbox

Better browser support
Quicker to use if you know the syntax
The flex properties can be transitioned

## Advantages of CSS grid

Behavior is more consistent across different browsers(less bugs)

## Changing access in CSS grid

```css
  .flipper {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
  }

  .flipper.flip {
    grid-template-columns: 1fr;
  }
```

Row reverse and column reverse are not possible in grid. It also have the option to switch to columns of two.

## Space between(text on the left / button on the right)

```css
  .track {
    grid-template-columns: 1fr;
    display: grid;
    grid-auto-flow: column;
  }
```

## Flex on item

If we have items that we want to grow the remaiming space for example the scrubber on video player it easier to do this with flexbox using `flex: 1;` on the item flex.

## Center text with grid

When are two items that need to be vertically centered we should use `align-content` instead of `align-items` to stop the row from stretching. However it is only an extra line to do that same thing in flexbox.

### Grid is good when we need to algin items to different corners of a box

```css
  .corners {
    display: grid;
    height: 200px;
    width: 200px;
    border: 10px solid var(--yellow);
    grid-template: 1fr 1fr / 1fr 1fr;
    align-items: end;
    justify-items: end;
  }

  .corner:nth-child(1),
  .corner:nth-child(2) {
    align-self: start;
  }

  .corner:nth-child(1),
  .corner:nth-child(3) {
    justify-self: start;
  }
```

If we know how many columns need but do not want to have set sizes for the content we can do:

```css
  .known {
    margin: 100px 0;
    display: grid;
    grid-template-columns: repear(5, auto);
    justify-content: center;
    grid-gap: 20px;
  }
```

## Unknown number of items

Grid is also handy when the number of items within a grid is unknown.

```css
 .unknown {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
  grid-gap: 20px;
 }
```

This is probably one of the feature of grid I could see myself using a lot

```css
  .unknown {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(50px, 1fr));
    grid-gap: 20px;
  }
```

## The takeway

When approaching a layout try it using both grid & flexbox and see which one works the best
