# Lessons learnt

This is the first practical usage of the CSS grid. IN this lesson we learnt how to create a someone grid album layout.

## Get responsive behavior without lots of media queries

The two main elements we used when creating this grid layout to get the responsive behavior was auto-fit and minmax.

```css
.albums {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 20px;
}
```

## When working with images ensure that the image is 100% of the container all things will start to get ropey

This is also the case when working with flexbox.

## Only one fixed width item

A common use case when creating layouts is having one section such as a image needing a set width and the rest of the content spanning the remaining space. This can be done by `grid-template-columns: 150px 1fr;`
