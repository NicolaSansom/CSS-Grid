# Lessons learnt

This lesson covers how to set up a bootsrap like layout using grid. Wes mentions having uniform grid instead of designing something that flex is not always the best but there are valid use cases for this.

Basic set up, there a big which requires setting min width of 0

```css
    .grid {
      display: grid;
      grid-template-columns: repeat(12, minmax(0, 1fr));
      grid-gap: 20px;
    }

    .item {
      width: 100%;
    }
```

In the video we used css variables to pass it custom sizes of css instead of classes, so we had variable called span like so:

```css
  --span: 1;
  grid-column: span var(--span);
```

You could then overide these values be passing inline style `styles="--span: 7"`

Css variables also allow for a fallback value in case unset `var(--span, 1)`
